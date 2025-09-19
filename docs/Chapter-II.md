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
**Propósito:** Modelar y automatizar la operación diaria de transporte, la trazabilidad de asignaciones (assignments), el control de mantenimientos y la visibilidad de desempeño de la flota.  
**Usuarios primarios:** Gestores de flota, conductores, administradores.  
**Ubiquitous language:** flota, vehículo, conductor, asignación, ruta, evidencia, mantenimiento preventivo/correctivo, servicio realizado, alerta, reporte, kilometraje, ubicación, estado de vehículo, licencia vigente.  
**Límites explícitos:** No cubre facturación, nómina ni CRM; se integra con dichos contextos vía APIs.  
**Políticas de consistencia:** Consistencia fuerte dentro del agregado **Asignación** al iniciar/completar y al impactar odometría; consistencia eventual para proyecciones (dashboard, reportes, listados).

---

### 2.6.x.1. Domain Layer

**Agregados y raíces**  
- **Flota (raíz):** id, nombre, métricas agregadas.  
- **Vehículo (raíz):** id, placa (VO Placa), año, kmActual (VO Kilometraje), estado (Operativo, EnMantenimiento, Inactivo), flotaId.  
- **Conductor (raíz):** id, código, nombres, apellidos, licencia (número, fechaExpiración), estado (Activo/Inactivo), flotaId.  
- **Asignación (raíz):** id (uuid), vehículoId, conductorId, ruta, estado (Pendiente, EnCurso, Completada, Cancelada), assignedAt, completedAt.  
- **Mantenimiento (raíz):** id, vehículoId, tipo (preventivo/correctivo), descripción, costo, fechas programada/ejecución, estado (Programado, EnEjecución, Completado, Vencido), notas.

**Value Objects**  
- UbicacionGPS(lat, lng)  
- Evidencia(url, comentario, timestamp, tipo)  
- RangoFechas(desde, hasta)  
- Placa(valor normalizado, único por flota)  
- Kilometraje(valor ≥ 0)

**Servicios de dominio**  
- PlanificadorMantenimientos  
- ValidadorAsignacion  
- GeneradorAlertas  

**Eventos de dominio**  
- AsignacionCreada  
- AsignacionIniciada  
- AsignacionCompletada  
- MantenimientoProgramado  
- MantenimientoCompletado  
- LicenciaPorVencerDetectada  

**Repositorios (interfaces)**  
- FlotaRepository  
- VehiculoRepository  
- ConductorRepository  
- AsignacionRepository  
- MantenimientoRepository  

**Invariantes clave**  
- Vehículo debe estar **Operativo** y conductor **Activo** con licencia vigente.  
- No se permiten dos asignaciones **EnCurso** simultáneas para el mismo vehículo o conductor.  
- `completedAt ≥ assignedAt`.  
- `kmActual` nunca decrece.

---

### 2.6.x.2. Interface Layer (HTTP/JSON)

**Propósito:** Exponer capacidades mediante una API estable, segura y versionada, consumida por supervisores (WebApp) y conductores (PWA/Mobile).  

**Responsabilidades clave**  
- Contratos públicos y versionado (`/api`).  
- Validación de entrada y normalización de errores (`problem+json`).  
- Autenticación/Autorización (OAuth2/JWT), control de acceso por rol.  
- Idempotencia en operaciones POST/PUT (`Idempotency-Key`).  
- Observabilidad: `X-Correlation-Id`, métricas y trazas.  
- Seguridad: rate limiting, CORS, límites de payload.  

**Principales endpoints (resumen)**  

| Método | Ruta                               | Caso de uso             | Request DTO                    | Response DTO              |
|--------|------------------------------------|-------------------------|--------------------------------|---------------------------|
| POST   | `/api/Assignment`                  | Crear asignación        | `{vehicleId, driverId, route}` | `AssignmentDTO`           |
| PUT    | `/api/Assignment/{id}/start`       | Iniciar asignación      | —                              | `AssignmentDTO`           |
| PUT    | `/api/Assignment/{id}/complete`    | Completar asignación    | —                              | `AssignmentDTO`           |
| GET    | `/api/Vehicle`                     | Listar vehículos        | —                              | `[VehicleDTO]`            |
| GET    | `/api/Driver`                      | Listar conductores      | —                              | `[DriverDTO]`             |
| POST   | `/api/Maintenance/records`         | Programar mantenimiento | `CreateMaintenanceRecordDTO`   | `MaintenanceRecordDTO`    |
| GET    | `/api/Dashboard/stats`             | KPIs globales           | —                              | `DashboardStatsDTO`       |
| POST   | `/api/Report`                      | Generar reporte         | `CreateReportDTO`              | `ReportDTO`               |

**Errores comunes**  
- `400` datos inválidos  
- `401/403` autenticación/autorización  
- `404` no encontrado  
- `409` conflicto de estado (ej. iniciar ya iniciada)  
- `422` regla de dominio incumplida  

---

### 2.6.x.3. Application Layer

**Propósito:** Orquestar casos de uso, coordinando repositorios, servicios de dominio e integraciones.  

**Servicios de aplicación**  
- CrearAsignacionService  
- IniciarAsignacionService  
- CompletarAsignacionService  
- ProgramarMantenimientoService  
- ReportesService  
- GestionVehiculosService  
- GestionConductoresService  

**Lineamientos**  
- Transacciones por caso de uso; publicación de eventos con *Transactional Outbox*.  
- Mapeo DTO ↔ Command/Query ↔ Dominio.  
- Idempotencia en POST/PUT.  
- Seguridad: validación de claims (rol, ownership).  
- Observabilidad: métricas por caso de uso y logs estructurados.  

**Flujo típico (Completar Asignación)**  
1. Cargar Asignación por ID.  
2. Validar estado y licencia del conductor.  
3. Persistir cambios y marcar `completedAt`.  
4. Emitir evento `AsignacionCompletada`.  
5. Actualizar proyecciones (Dashboard, Reportes).  

---

### 2.6.x.4. Infrastructure Layer

**Propósito:** Resolver persistencia, integración y mensajería.  

**Componentes**  
- Repositorios ORM/SQL  
- DB relacional (MySQL/PostgreSQL)  
- Object storage para evidencias  
- Integraciones externas: Auth, GPS, Notificaciones  
- Mensajería (Outbox/cola)  
- Observabilidad (Prometheus, OpenTelemetry)  

**Patrones**  
- Repository  
- Gateway  
- Outbox  
- Circuit Breaker/Retry  
- Saga/Compensación (opcional)  

---

### 2.6.x.5. Component Level Diagram (C4-L3)

**Descripción:** Vista de componentes (API, Application Services, Domain Model, Repositorios, Integraciones).  

> **Aquí la imagen C4–L3 (Component)**  
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

### 2.6.x.6.1. Domain Layer Class Diagrams

**Agregados y VO**  
- **Flota (AR):** id, nombre  
- **Vehículo (AR):** id, placa:Placa, kmActual:Kilometraje, estado, flotaId  
- **Conductor (AR):** id, code, nombres, apellidos, licencia, estado, flotaId  
- **Asignación (AR):** id, vehicleId, driverId, ruta, estado, assignedAt?, completedAt?  
- **Mantenimiento (AR):** id, vehicleId, tipo, descripción, costo, fechaProgramada, fechaEjecución?, estado  
- **VO.Placa:** valor único por flota  
- **VO.Kilometraje:** valor ≥ 0  
- **VO.UbicacionGPS:** lat, lng  
- **VO.Evidencia:** url, comentario?, timestamp, tipo  

**Asociaciones**  
- Flota 1..* Vehículo  
- Flota 1..* Conductor  
- Vehículo 1..* Mantenimiento  
- Vehículo 0..* Asignación  
- Conductor 0..* Asignación  

---

### 2.6.x.6.2. Database Design Diagram (ERD)

**Tablas principales**  
- flotas(id PK, nombre, code, type, is_active, timestamps)  
- vehiculos(id PK, license_plate UNIQUE, brand, model, year, mileage, status, fleet_id FK, driver_id FK NULL, timestamps)  
- conductores(id PK, code UNIQUE, first_name, last_name, license_number, license_expiry_date, phone, email UNIQUE, experience_years, status, flota_id FK, timestamps)  
- asignaciones(id UUID PK, vehicle_id FK, driver_id FK, route, status, assigned_at, completed_at)  
- mantenimientos(id PK, vehicle_id FK, description, type, cost, scheduled_date, completed_date, status, notes, timestamps)  
- servicios_mantenimiento(id PK, vehicle_id FK, service_type, description, cost, service_date, mileage_at_service, service_provider, timestamps)  

**Índices sugeridos**  
- vehiculos.license_plate UNIQUE  
- conductores.code UNIQUE  
- conductores.email UNIQUE  
- asignaciones(vehicle_id, status)  
- asignaciones(driver_id, status)  
- mantenimientos(vehicle_id, scheduled_date)  

**Políticas**  
- FK con `RESTRICT` en delete/update.  
- Constraint: no dos asignaciones EnCurso para el mismo vehículo/conductor.  
- Timestamps estándar, soft delete opcional.  

---
