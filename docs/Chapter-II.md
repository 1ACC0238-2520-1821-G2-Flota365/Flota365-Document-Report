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

El proceso de **EventStorming** permitió explorar el dominio de la startup desde un nivel estratégico, identificando los principales eventos de negocio, los bounded contexts y las interacciones entre ellos. Esta técnica visual facilitó descubrir la complejidad del sistema, fomentar el entendimiento compartido entre el equipo y establecer una base sólida para la implementación con DDD.

#### 2.5.1.1. Candidate Context Discovery

En esta etapa se identificaron los **bounded contexts** principales que conforman el dominio del sistema de gestión de flotas:

- **Fleet Management BC**: responsable del ciclo de vida de los vehículos (registro, actualización de estado, baja).
- **Driver Management BC**: gestiona la contratación de conductores, sus licencias y disponibilidad.
- **Assignments BC**: se encarga de la asignación de vehículos a conductores para la ejecución de rutas.
- **Maintenance BC**: administra órdenes de mantenimiento y servicios asociados a los vehículos.
- **Reporting BC**: genera reportes y métricas clave a partir de la información de otros contextos.
- **Management BC**: supervisa KPIs, managers y la toma de decisiones estratégicas.
- **Auth BC**: ofrece autenticación, autorización y gestión de usuarios.
- **Dashboard BC**: concentra información agregada y estadísticas operativas.
- **Health Monitoring**: provee información sobre el estado de la infraestructura.

Estos contextos encapsulan reglas de negocio específicas y reducen el acoplamiento, permitiendo escalar de forma modular.

 <img src="/images/chapter-II/structurizr-candidate_context_discovery.png" height="1440" alt="candidate_context_discovery"><br>

#### 2.5.1.2. Domain Message Flows Modeling

El modelado de **flujos de mensajes de dominio** permitió comprender cómo los bounded contexts interactúan entre sí mediante **commands** y **events**:

- **Ciclo de vida de una asignación**  
  - `CreateAssignment` → *AssignmentCreated* → notifica a Driver y Fleet.  
  - `StartAssignment` → *AssignmentStarted* → actualiza Dashboard.  
  - `CompleteAssignment` → *AssignmentCompleted* → genera reporte y puede detonar mantenimiento.

- **Ciclo de vida de mantenimiento**  
  - `CreateMaintenanceOrder` → *MaintenanceOrderCreated* → actualiza estado de vehículo en Fleet.  
  - `CloseMaintenanceOrder` → *MaintenanceClosed* → alimenta Reporting y actualiza KPIs en Management.

- **Flujo de autenticación**  
  - `RegisterUser` → *UserRegistered* → puede crear un Manager en Management.  
  - `LoginUser` → *UserLoggedIn* → emite JWT y actualiza métricas en Dashboard.  
  - Fallos de login → *LoginFailed*.

Estos flujos hacen visibles las dependencias y políticas de integración entre contextos.
 <img src="/images/chapter-II/structurizr-assignment_lifecycle.png" height="1440" alt="Assignmets-lifecycle"><br>
#### 2.5.1.3. Bounded Context Canvases

Finalmente, se desarrollaron los **Bounded Context Canvases** para detallar las responsabilidades, actores, comandos y eventos de cada contexto.  

Ejemplo para **Assignments BC**:
- **Responsabilidad**: gestionar asignaciones vehículo–conductor.  
- **Usuarios clave**: Dispatcher, Manager.  
- **Comandos**: `CreateAssignment`, `StartAssignment`, `CompleteAssignment`.  
- **Eventos**: `AssignmentCreated`, `AssignmentStarted`, `AssignmentCompleted`.  
- **Integraciones**: consulta disponibilidad de Drivers, reserva vehículos de Fleet, publica eventos hacia Reporting y Dashboard.  

Este nivel de detalle asegura claridad en la separación de responsabilidades, evita ambigüedades en los límites del dominio y facilita la implementación de la arquitectura en capas (API, Application, Domain, Infrastructure).
 <img src="/images/chapter-II/structurizr-assignments_canvas.png" height="1440" alt="assignments_canvas"><br>
### 2.5.2. Context Mapping
### 2.5.3. Software Architecture
#### 2.5.3.1. Software Architecture Context Level Diagrams
#### 2.5.3.2. Software Architecture Container Level Diagrams
#### 2.5.3.3. Software Architecture Deployment Diagrams

## 2.6. Tactical-Level Domain-Driven Design
### 2.6.x. Bounded Context: 
#### 2.6.x.1. Domain Layer
#### 2.6.x.2. Interface Layer
#### 2.6.x.3. Application Layer
#### 2.6.x.4. Infrastructure Layer
#### 2.6.x.5. Bounded Context Software Architecture Component Level Diagrams
#### 2.6.x.6. Bounded Context Software Architecture Code Level Diagrams
##### 2.6.x.6.1. Bounded Context Domain Layer Class Diagrams
##### 2.6.x.6.2. Bounded Context Database Design Diagram

