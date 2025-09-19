## 2.1. Competidores
### 2.1.1. Análisis competitivo
### 2.1.2. Estrategias y tácticas frente a competidores

## 2.2. Entrevistas
### 2.2.1. Diseño de entrevistas
### 2.2.2. Registro de entrevistas
### 2.2.3. Análisis de entrevistas

## 2.3. Needfinding
### 2.3.1. User Personas
### 2.3.2. User Task Matrix
### 2.3.3. User Journey Mapping
### 2.3.4. Empathy Mapping
### 2.3.5. Ubiquitous Language

## 2.4. Requirements specification
### 2.4.1. User Stories
### 2.4.2. Impact Mapping
### 2.4.3. Product Backlog

## 2.5. Strategic-Level Domain-Driven Design
### 2.5.1. EventStorming
#### 2.5.1.1. Candidate Context Discovery
#### 2.5.1.2. Domain Message Flows Modeling
#### 2.5.1.3. Bounded Context Canvases
### 2.5.2. Context Mapping
### 2.5.3. Software Architecture
#### 2.5.3.1. Software Architecture Context Level Diagrams
#### 2.5.3.2. Software Architecture Container Level Diagrams
#### 2.5.3.3. Software Architecture Deployment Diagrams

## 2.6. Tactical-Level Domain-Driven Design

### 2.6.x. Bounded Context
**Nombre:** Gestión de Flotas  
**Propósito:** Modelar y automatizar la operación diaria de transporte, la trazabilidad de servicios, el control de mantenimientos y la visibilidad de desempeño de la flota.  
**Usuarios primarios:** Gestores de flota, conductores.  
**Ubiquitous language:** flota, vehículo, conductor, servicio, evidencia, mantenimiento preventivo/correctivo, ruta, alerta, reporte operativo, kilometraje, ubicación.  
**Límites explícitos:** El contexto no aborda facturación, nómina ni gestión comercial; se integra con esos contextos mediante APIs.  
**Políticas de consistencia:** Consistencia fuerte dentro del agregado Servicio al confirmar evidencias y kilometrajes; eventual para proyecciones y reportes.

---
### 2.6.x.1. Domain Layer
**Agregados y raíces**  
- Flota (raíz): id, nombre. Contiene colecciones referenciales de vehículos y conductores.  
- Vehículo (raíz): id, placa, kmActual, estadoMecánico; reglas para actualizar kilometraje, validar disponibilidad, programar mantenimiento.  
- Conductor (raíz): id, dni, nombre, licencia; reglas para habilitación y asignación a servicios.  
- Servicio (raíz): id, vehículoId, conductorId, origen, destino, fecha, kmInicio, kmFin, estadoServicio.  
- Mantenimiento (raíz): id, vehículoId, tipo, fechaProgramada, fechaEjecución, estado.

**Value Objects**  
- UbicaciónGPS (lat, lng)  
- Evidencia (url, comentario, timestamp, tipo)  
- RangoFechas (desde, hasta)  
- Placa (valor normalizado)  
- Kilometraje (valor ≥ 0)

**Servicios de dominio**  
- PlanificadorMantenimientos  
- ValidadorServicio  
- GeneradorAlertas  

**Eventos de dominio**  
- MantenimientoProgramado  
- ServicioIniciado  
- EvidenciaRegistrada  
- ServicioCompletado  

**Repositorios (interfaces)**  
- FlotaRepository  
- VehiculoRepository  
- ConductorRepository  
- ServicioRepository  
- MantenimientoRepository  

---
## 2.6.x.2. Interface Layer

**Propósito.** Exponer capacidades del bounded context *Gestión de Flotas* mediante una API HTTP/JSON estable, segura y versionada, consumida por la **Web App (Supervisores)** y la **PWA/Mobile (Conductores)**, e integrable por terceros (p. ej. proveedor GPS).

**Responsabilidades clave**
- Definir contratos públicos (endpoints, DTOs de request/response) y versiones (`/api/v1/...`).
- Validar entrada (tipos, rangos, obligatoriedad) y normalizar errores (código + `problem+json`).
- Autorización/Autenticación (OAuth2/JWT), control de acceso por rol (Supervisor, Conductor).
- Idempotencia (cabecera `Idempotency-Key` en operaciones de escritura).
- Observabilidad: correlación (`X-Correlation-Id`), métricas de latencia/errores, trazas.
- Protecciones: rate limiting, CORS, payload size limit.
- Mapeo DTO ⇄ Modelo de Aplicación (sin exponer entidades de dominio).

**Principales endpoints (resumen)**
| Método | Ruta | Caso de uso | Request (DTO) | Response (DTO) | Notas |
|---|---|---|---|---|---|
| POST | `/api/v1/servicios` | Registrar servicio | `RegistrarServicioDTO` | `ServicioDTO` | Idempotencia opcional |
| POST | `/api/v1/servicios/{id}/evidencias` | Adjuntar evidencia | `RegistrarEvidenciaDTO` | `EvidenciaDTO` | Carga URL prefirmada/obj storage |
| POST | `/api/v1/servicios/{id}/completar` | Completar servicio | `CompletarServicioDTO` | `ServicioDTO` | Valida invariantes (km) |
| POST | `/api/v1/mantenimientos` | Programar mantenimiento | `ProgramarMantenimientoDTO` | `MantenimientoDTO` | Plan por km/fecha |
| GET | `/api/v1/reportes/operacion` | Reporte operativo | query: `desde`, `hasta`, `placa?`, `dni?` | `ReporteOperativoDTO` | Exportable (PDF/CSV) |
| GET | `/api/v1/vehiculos/{id}` | Consultar vehículo | — | `VehiculoDTO` | Proyección ligera |

**DTOs (ejemplos breves)**
- `RegistrarServicioDTO`: `{ vehiculoId, conductorId, origen:{lat,lng}, destino:{lat,lng}, kmInicio }`
- `RegistrarEvidenciaDTO`: `{ tipo, comentario?, url }`
- `CompletarServicioDTO`: `{ kmFin }`

**Errores comunes**
- `400` datos inválidos, `401/403` authz, `404` no existe, `409` conflicto/estado, `422` regla de dominio incumplida.

---

## 2.6.x.3. Application Layer

**Propósito.** Orquestar casos de uso atómicos, coordinando repositorios, servicios de dominio y gateways externos, aplicando reglas transaccionales y publicando eventos.

**Servicios de Aplicación**
- `RegistrarServicioService`
- `RegistrarEvidenciaService`
- `CompletarServicioService`
- `ProgramarMantenimientoService`
- `ReportesService`

**Lineamientos**
- **Transacciones** por caso de uso; consistencia con *Transactional Outbox* para integraciones/eventos.
- **Mapeo** DTO ⇄ *Command/Query* ⇄ Dominio (Assembler/Mappers).
- **Políticas** de idempotencia, retriable (exponencial backoff), compensaciones si aplica.
- **Seguridad**: verificación de claims (placa asignada, rol).
- **Observabilidad**: métrica por UC (tasa, latencia p95/p99, errores), logs estructurados.

**Flujos típicos (ejemplo — Completar Servicio)**
1. Cargar `Servicio` por ID y validar estado.
2. Aplicar `kmFin` y reglas (`kmFin ≥ kmInicio`, evidencia cargada si es requerida).
3. Persistir y emitir evento `ServicioCompletado`.
4. Notificar (si corresponde) y actualizar proyecciones/reporte.

---

## 2.6.x.4. Infrastructure Layer

**Propósito.** Implementar detalles técnicos: persistencia, integración y entrega de mensajes, ocultando tecnología al dominio.

**Componentes**
- **Repositorios** (ORM/SQL): `VehiculoRepository`, `ServicioRepository`, `MantenimientoRepository`, etc.
- **Data Source**: **Relational DB** (MySQL/PostgreSQL).
- **Object Storage**: Evidencias (fotos) con URLs prefirmadas.
- **Integraciones externas**:
  - **Auth Service** (OAuth2/JWT).
  - **GPS Provider** (webhooks de posición/odometría).
  - **Notification Service** (email/push).
- **Mensajería (opcional)**: *Outbox* + worker para entrega confiable.
- **Observabilidad**: exportadores (Prometheus/OpenTelemetry), dashboards y alertas.
- **Configuración/Secrets**: variables de entorno, vault, rotación de credenciales.

**Patrones**
- *Repository*, *Gateway*, *Outbox*, *Circuit Breaker/Retry*, *Bulkhead*, *Saga/Compensación* (si hubiese flujo multipartito).

---

## 2.6.x.5. Bounded Context Software Architecture Component Level Diagrams

**Descripción.** Vista **C4–Level 3 (Component)** del bounded context *Gestión de Flotas*: API, Application Services, Domain Model, Repositorios e integraciones.

> **Inserta aquí la imagen C4–L3 (Component)**  
> `![C4 L3 – Component Diagram](flota365_c4_l3_component.png)`

**Leyenda rápida**
- **API Gateway**: control de entrada, authn/z, validación, DTOs.
- **Application Services**: orquestación de casos de uso.
- **Domain Model**: entidades, VO, servicios de dominio, invariantes.
- **Repositorios**: puertos/implementaciones hacia DB/Storage.
- **Integraciones**: Auth, GPS, Notificaciones.

---

## 2.6.x.6. Bounded Context Software Architecture Code Level Diagrams

**Descripción.** Vista **C4–Level 4 (Code)** enfocada en clases del dominio (agregados y VO).

> **Inserta aquí la imagen C4–L4 (Code / Domain Classes)**  
> `![C4 L4 – Domain Classes](flota365_c4_l4_code.png)`

**Invariantes destacadas**
- `kmFin ≥ kmInicio` al completar servicio.
- Vehículo en **estado operativo** para iniciar servicio.
- **Placa** única por flota; **DNI** único por flota (si aplica).
- **Evidencia** obligatoria para ciertos tipos de servicio (política).

---

## 2.6.x.6.1. Bounded Context Domain Layer Class Diagrams

**Agregados y VO (resumen formal)**
- **Flota (AR)**: `id`, `nombre` → agrega **Vehiculo** y **Conductor**.
- **Vehiculo (AR)**: `id`, `placa:Placa`, `kmActual:Kilometraje`, `estado`.
- **Conductor (AR)**: `id`, `dni`, `nombre`, `licencia`, `estado`.
- **Servicio (AR)**: `id`, `vehiculoId`, `conductorId`, `origen:UbicacionGPS`, `destino:UbicacionGPS`, `kmInicio:Kilometraje`, `kmFin:Kilometraje?`, `estado`, `evidencias: Evidencia[]`.
- **Mantenimiento (AR)**: `id`, `vehiculoId`, `tipo`, `fechaProgramada`, `fechaEjecucion?`, `estado`.
- **VO.Placa**: `valor` (formato y unicidad por flota).
- **VO.Kilometraje**: `valor` (≥ 0).
- **VO.UbicacionGPS**: `lat`, `lng`.
- **VO.Evidencia**: `url`, `comentario?`, `timestamp`, `tipo`.
- **Servicios de Dominio**:
  - `PlanificadorMantenimientos`: políticas por km/tiempo/uso.
  - `ValidadorServicio`: invariantes (km, estados, evidencia).
  - `GeneradorAlertas`: eventos por vencimiento/anomalías.

**Reglas de asociación**
- `Flota 1..* Vehiculo` y `Flota 1..* Conductor`.
- `Vehiculo 1..* Mantenimiento`.
- `Servicio` **usa** `Vehiculo` y `Conductor`; contiene 0..* `Evidencia`.

---

## 2.6.x.6.2. Bounded Context Database Design Diagram

**Descripción.** Diseño lógico relacional (ERD) de apoyo a los repositorios.

> **Inserta aquí la imagen ERD**  
> `![Database ERD](flota365_c4_db.png)`

**Tablas (resumen)**
- `flotas(id PK, nombre)`
- `vehiculos(id PK, placa UNIQUE, km_actual, estado, flota_id FK→flotas.id)`
- `conductores(id PK, dni UNIQUE, nombre, licencia, flota_id FK→flotas.id)`
- `servicios(id PK, vehiculo_id FK→vehiculos.id, conductor_id FK→conductores.id, origen, destino, fecha, km_inicio, km_fin, estado)`
- `evidencias(id PK, servicio_id FK→servicios.id, url, comentario, timestamp, tipo)`
- `mantenimientos(id PK, vehiculo_id FK→vehiculos.id, tipo, fecha_programada, fecha_ejecucion, estado)`

**Índices sugeridos**
- `vehiculos.placa` (UNIQUE), `conductores.dni` (UNIQUE).
- `servicios(vehiculo_id, fecha)`, `servicios(conductor_id, fecha)`.
- `mantenimientos(vehiculo_id, fecha_programada)`.
- `evidencias(servicio_id, timestamp)`.

**Integridad y políticas**
- *FK ON UPDATE/DELETE RESTRICT* para no perder trazabilidad.
- Triggers/constraints para garantizar `km_fin ≥ km_inicio`.
- Timestamps y `updated_at`/`created_at` estándar; *soft delete* opcional.

---

