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
#### 2.6.x.2. Interface Layer
#### 2.6.x.3. Application Layer
#### 2.6.x.4. Infrastructure Layer
#### 2.6.x.5. Bounded Context Software Architecture Component Level Diagrams
#### 2.6.x.6. Bounded Context Software Architecture Code Level Diagrams
##### 2.6.x.6.1. Bounded Context Domain Layer Class Diagrams
##### 2.6.x.6.2. Bounded Context Database Design Diagram

