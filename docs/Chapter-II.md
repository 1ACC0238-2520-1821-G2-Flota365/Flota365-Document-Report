# Capítulo 2: Requirements Development and Software Solution Design

## 2.1. Competidores
### 2.1.1. Análisis competitivo
### 2.1.2. Estrategias y tácticas frente a competidores

## 2.2. Entrevistas
### 2.2.1. Diseño de entrevistas
### 2.2.2. Registro de entrevistas
### 2.2.3. Análisis de entrevistas

## 2.3. Needfinding
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
#### 2.5.3.2. Software Architecture Container Level Diagrams
#### 2.5.3.3. Software Architecture Deployment Diagrams

## 2.6. Tactical-Level Domain-Driven Design

### 2.6.1. Bounded Context

#### 2.6.1.1. Domain Layer

La capa de dominio es el núcleo de la aplicación, pues en ella se definen los modelos y reglas esenciales que conforman la lógica del negocio. Dentro de este marco, el agregado "User" se establece como la entidad principal que simboliza a los usuarios del sistema, incluyendo sus propiedades y responsabilidades. Esta capa asegura que los conceptos del negocio y sus interacciones se representen y gestionen de manera adecuada.

Propósito: Modelar las entidades del dominio, integrando tanto sus atributos como sus comportamientos, con el fin de reflejar fielmente los elementos centrales de la aplicación, como usuarios, productos, procesos comerciales, entre otros.

* Aggregate: Assignment  
**Descripción:**  El agregado "Assignment" actúa como la raíz del modelo, encapsulando los datos esenciales de la asignación de un viaje, como el vehículo, conductor, ruta, estado y fechas clave del viaje. Su representación en la base de datos se realiza mediante la tabla `assignments`, asegurando la persistencia de esta entidad clave.

| Atributo       | Tipo          | Descripción                                                                 |
|----------------|---------------|-----------------------------------------------------------------------------|
| `Id`           | `Guid`        | Identificador único de la asignación.                                        |
| `VehicleId`    | `Guid`        | Identificador único del vehículo asociado a la asignación.                  |
| `DriverId`     | `Guid`        | Identificador único del conductor asignado.                                  |
| `Route`        | `string`      | Ruta asignada al viaje (nombre o descripción de la ruta).                    |
| `Status`       | `string`      | Estado de la asignación: puede ser `PENDING`, `IN_PROGRESS` o `COMPLETED`.   |
| `AssignedAt`   | `DateTime`    | Fecha y hora en que se asignó el viaje al conductor.                         |
| `CompletedAt`  | `DateTime?`   | Fecha y hora en que se completó la asignación del viaje. Este campo es opcional (`nullable`).|


| Método                                       | Descripción                                                                                         |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------|
| `Start()`                                    | Cambia el estado de la asignación de "PENDING" a "IN_PROGRESS". Lanza una excepción si la asignación no está en estado "PENDING". |
| `Complete()`                                 | Cambia el estado de la asignación de "IN_PROGRESS" a "COMPLETED" y registra la fecha de finalización. Lanza una excepción si la asignación no está en estado "IN_PROGRESS". |

### Interfaz `IAssignmentRepository`

| Método                                       | Descripción                                                                                         |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------|
| `GetByIdAsync(Guid id)`                      | Obtiene una asignación de manera asíncrona a partir de su identificador único (`id`).               |
| `GetAllAsync()`                              | Obtiene todas las asignaciones de manera asíncrona.                                                  |
| `AddAsync(Assignment assignment)`            | Agrega una nueva asignación al repositorio de manera asíncrona.                                     |
| `UpdateAsync(Assignment assignment)`         | Actualiza una asignación existente en el repositorio de manera asíncrona.                           |



* Aggregate: User  
**Descripción:**  El agregado "Usuario" actúa como la raíz del modelo, encapsulando los datos esenciales de la cuenta y su rol dentro del sistema. Su representación en la base de datos se realiza mediante la tabla users, asegurando la persistencia de esta entidad clave.

| Atributo           | Tipo                 | Descripción                                                                                  |
|--------------------|----------------------|----------------------------------------------------------------------------------------------|
| `Id`               | `long`               | Identificador único del usuario (autogenerado).                                               |
| `Username`         | `string`             | Nombre de usuario único del sistema.                                                          |
| `Password`         | `string`             | Contraseña del usuario.                                                                       |
| `Roles`            | `HashSet<Role>`      | Conjunto de roles asociados al usuario.                                                      |
| `ProofingApoderado`| `string`             | Prueba o evidencia del usuario como apoderado (almacenada como texto).                       |
| `FirstName`        | `string`             | Primer nombre del usuario.                                                                   |
| `LastName`         | `string`             | Apellido del usuario.                                                                        |
| `FullName`         | `string`             | Nombre completo del usuario, concatenando `FirstName` y `LastName`.                           |
| `Email`            | `string`             | Correo electrónico del usuario.                                                              |
| `IsActive`         | `bool`               | Indica si el usuario está activo o no.                                                        |
| `CreatedAt`        | `DateTime`           | Fecha de creación del usuario.                                                                |
| `UpdatedAt`        | `DateTime`           | Fecha de la última actualización del usuario.                                                 |


| Método                     | Descripción                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| `UpdateProfile(string firstName, string lastName)` | Actualiza el nombre y apellido del usuario, y establece la fecha de última actualización (`UpdatedAt`). |
| `UpdateRole(string role)`   | Actualiza el rol del usuario y establece la fecha de última actualización (`UpdatedAt`).      |
| `SetActive(bool isActive)`  | Establece si el usuario está activo o no, y actualiza la fecha de última actualización (`UpdatedAt`). |
| `UpdatePassword(string passwordHash)` | Actualiza la contraseña del usuario (almacenada como hash), y establece la fecha de última actualización (`UpdatedAt`). |

### Interface `IUserRepository`

| Método                     | Descripción                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| `GetByEmailAsync(string email)` | Obtiene un usuario de manera asíncrona a partir de su correo electrónico.                   |
| `GetByIdAsync(int id)`      | Obtiene un usuario de manera asíncrona a partir de su identificador único (`id`).           |
| `GetAllAsync()`             | Obtiene todos los usuarios de manera asíncrona.                                              |
| `AddAsync(User user)`       | Agrega un nuevo usuario al repositorio de manera asíncrona.                                  |
| `UpdateAsync(User user)`    | Actualiza un usuario en el repositorio de manera asíncrona.                                  |

* Aggregate: Driver  
**Descripción:**  El agregado "Driver" actúa como la raíz del modelo, encapsulando los datos esenciales de un conductor, incluyendo su identidad, información de licencia, contacto, estado, y su vehículo asignado. Su representación en la base de datos se realiza mediante la tabla `drivers`, asegurando la persistencia de esta entidad clave.

| Atributo             | Tipo          | Descripción                                                                 |
|----------------------|---------------|-----------------------------------------------------------------------------|
| `Id`                 | `int`         | Identificador único del conductor.                                          |
| `Code`               | `string`      | Código único del conductor.                                                  |
| `FirstName`          | `string`      | Primer nombre del conductor.                                                |
| `LastName`           | `string`      | Apellido del conductor.                                                     |
| `FullName`           | `string`      | Nombre completo del conductor (concatenando `FirstName` y `LastName`).       |
| `LicenseNumber`      | `string`      | Número de licencia del conductor.                                           |
| `LicenseExpiryDate`  | `DateTime`    | Fecha de vencimiento de la licencia del conductor.                          |
| `Phone`              | `string`      | Número de teléfono del conductor.                                           |
| `Email`              | `string`      | Correo electrónico del conductor.                                           |
| `ExperienceYears`    | `int`         | Años de experiencia del conductor.                                          |
| `Status`             | `int`         | Estado del conductor: `1` para activo y `0` para inactivo.                  |
| `StatusName`         | `string`      | Nombre del estado del conductor, basado en el valor de `Status` (`Active` o `Inactive`). |
| `AssignedVehicle`    | `string`      | Vehículo asignado al conductor.                                             |
| `IsActive`           | `bool`        | Indica si el conductor está activo (valor derivado de `Status`).            |
| `CreatedAt`          | `DateTime`    | Fecha de creación del registro del conductor.                               |
| `UpdatedAt`          | `DateTime`    | Fecha de la última actualización del registro del conductor.                |
| `IsLicenseExpiringSoon` | `bool`      | Indica si la licencia está por expirar en los próximos 30 días.             |



| Método                                   | Descripción                                                                                     |
|------------------------------------------|-------------------------------------------------------------------------------------------------|
| `UpdateStatus(int status, string statusName)` | Actualiza el estado del conductor (`Status` y `StatusName`) y establece la fecha de última actualización (`UpdatedAt`). |
| `AssignVehicle(string vehicleInfo)`      | Asigna un vehículo al conductor y actualiza la fecha de última actualización (`UpdatedAt`).       |
| `UpdatePersonalInfo(string firstName, string lastName, string phone, string email)` | Actualiza la información personal del conductor (`FirstName`, `LastName`, `Phone`, `Email`) y la fecha de última actualización (`UpdatedAt`). |
| `UpdateLicense(string licenseNumber, DateTime licenseExpiryDate)` | Actualiza la información de la licencia del conductor (`LicenseNumber`, `LicenseExpiryDate`) y la fecha de última actualización (`UpdatedAt`). |
| `UpdateExperience(int experienceYears)`  | Actualiza los años de experiencia del conductor y la fecha de última actualización (`UpdatedAt`).  |

* Aggregate: Vehicle  
**Descripción:**  El agregado "Vehicle" actúa como la raíz del modelo, encapsulando los datos esenciales de un vehículo, incluyendo su placa, marca, modelo, estado, kilometraje, y la información relacionada con su conductor y flota. Su representación en la base de datos se realiza mediante la tabla `vehicles`, asegurando la persistencia de esta entidad clave.

| Atributo            | Tipo          | Descripción                                                                 |
|---------------------|---------------|-----------------------------------------------------------------------------|
| `Id`                | `int`         | Identificador único del vehículo.                                           |
| `LicensePlate`      | `string`      | Placa del vehículo.                                                          |
| `Brand`             | `string`      | Marca del vehículo.                                                         |
| `Model`             | `string`      | Modelo del vehículo.                                                        |
| `Year`              | `int`         | Año de fabricación del vehículo.                                            |
| `Mileage`           | `int`         | Kilometraje actual del vehículo.                                            |
| `Status`            | `int`         | Estado del vehículo: `1` para activo y `0` para inactivo.                   |
| `StatusName`        | `string`      | Nombre del estado del vehículo, basado en el valor de `Status` (`Active` o `Inactive`). |
| `FleetId`           | `int`         | Identificador de la flota a la que pertenece el vehículo.                   |
| `FleetName`         | `string`      | Nombre de la flota a la que pertenece el vehículo.                          |
| `DriverId`          | `int`         | Identificador del conductor asignado al vehículo.                           |
| `DriverName`        | `string`      | Nombre del conductor asignado al vehículo.                                  |
| `LastServiceDate`   | `DateTime?`   | Fecha del último servicio realizado al vehículo. Este campo es opcional (`nullable`). |
| `NextServiceDate`   | `DateTime?`   | Fecha del próximo servicio programado para el vehículo. Este campo es opcional (`nullable`). |
| `CreatedAt`         | `DateTime`    | Fecha de creación del registro del vehículo.                                |
| `UpdatedAt`         | `DateTime`    | Fecha de la última actualización del registro del vehículo.                 |


| Método                                       | Descripción                                                                                         |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------|
| `UpdateStatus(int newStatus, string statusName)` | Actualiza el estado del vehículo (`Status` y `StatusName`) y establece la fecha de última actualización (`UpdatedAt`). |
| `AssignDriver(int driverId, string driverName)`  | Asigna un conductor al vehículo (`DriverId` y `DriverName`) y actualiza la fecha de última modificación (`UpdatedAt`). |
| `UpdateMileage(int newMileage)`              | Actualiza el kilometraje del vehículo (`Mileage`) y actualiza la fecha de última modificación (`UpdatedAt`). |
| `SetServiceDates(DateTime? lastServiceDate, DateTime? nextServiceDate)` | Establece las fechas del último y próximo servicio del vehículo (`LastServiceDate`, `NextServiceDate`) y actualiza la fecha de última modificación (`UpdatedAt`). |

* Aggregate: Fleet  
**Descripción:**  El agregado "Fleet" actúa como la raíz del modelo, encapsulando los datos esenciales de una flota de vehículos, incluyendo su nombre, descripción, tipo, número de vehículos activos, en mantenimiento y el rendimiento. Su representación en la base de datos se realiza mediante la tabla `fleets`, asegurando la persistencia de esta entidad clave.

| Atributo              | Tipo            | Descripción                                                                 |
|-----------------------|-----------------|-----------------------------------------------------------------------------|
| `Id`                  | `int`           | Identificador único de la flota.                                            |
| `Code`                | `string`        | Código único asignado a la flota.                                           |
| `Name`                | `string`        | Nombre de la flota.                                                         |
| `Description`         | `string`        | Descripción de la flota.                                                    |
| `Type`                | `FleetType`     | Tipo de flota (por ejemplo, flota de vehículos ligeros, pesados, etc.).      |
| `TypeName`            | `string`        | Nombre del tipo de la flota.                                                |
| `IsActive`            | `bool`          | Indica si la flota está activa (`true`) o inactiva (`false`).               |
| `VehicleCount`        | `int`           | Número total de vehículos en la flota.                                      |
| `ActiveVehicles`      | `int`           | Número de vehículos activos en la flota.                                    |
| `InMaintenanceVehicles`| `int`          | Número de vehículos en mantenimiento en la flota.                           |
| `Performance`         | `decimal`       | Rendimiento de la flota (un valor numérico que podría indicar eficiencia).  |
| `CreatedAt`           | `DateTime`      | Fecha de creación de la flota.                                              |
| `UpdatedAt`           | `DateTime`      | Fecha de la última actualización de la flota.                               |

### Propiedades calculadas

| Propiedad               | Tipo        | Descripción                                                                 |
|-------------------------|-------------|-----------------------------------------------------------------------------|
| `PerformancePercentage`  | `decimal`   | Porcentaje de rendimiento de la flota calculado a partir del valor de `Performance`. |
| `StatusText`            | `string`    | Representación textual del estado de la flota: "Active" o "Inactive", basado en el valor de `IsActive`. |
| `VehicleUtilization`    | `decimal`   | Porcentaje de utilización de los vehículos activos respecto al total de vehículos en la flota. Calculado como `(ActiveVehicles / VehicleCount) * 100`. |


| Método                                       | Descripción                                                                                         |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------|
| `UpdateDetails(string name, string description, FleetType type)` | Actualiza los detalles de la flota, incluyendo el nombre, descripción y tipo, y genera un nuevo código para la flota. Se actualiza la fecha de última modificación (`UpdatedAt`). |
| `UpdateStatus(bool isActive)`                | Actualiza el estado de la flota (`IsActive`), indicando si está activa o no. Se actualiza la fecha de última modificación (`UpdatedAt`). |
| `UpdateVehicleStats(int vehicleCount, int activeVehicles, int inMaintenanceVehicles)` | Actualiza las estadísticas de la flota, incluyendo el número de vehículos totales, activos y en mantenimiento. Calcula el rendimiento de la flota (`Performance`) y actualiza la fecha de última modificación (`UpdatedAt`). |
| `UpdatePerformance(decimal performance)`     | Actualiza el rendimiento de la flota (`Performance`), asegurando que el valor esté entre 0 y 1, y actualiza la fecha de última modificación (`UpdatedAt`). |
| `GenerateCode(string name, FleetType type)`  | Método privado que genera un código único para la flota basado en su nombre y tipo. No está accesible fuera de la clase. |

### Interfaz `IFleetRepository`

| Método                                       | Descripción                                                                                         |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------|
| `GetByIdAsync(int id)`                       | Obtiene una flota de manera asíncrona a partir de su identificador único (`id`).                    |
| `GetAllAsync()`                              | Obtiene todas las flotas de manera asíncrona.                                                       |
| `AddAsync(Fleet fleet)`                      | Agrega una nueva flota al repositorio de manera asíncrona.                                          |
| `UpdateAsync(Fleet fleet)`                   | Actualiza una flota en el repositorio de manera asíncrona.                                           |
| `DeleteAsync(int id)`                        | Elimina una flota del repositorio a partir de su identificador único (`id`).                        |
| `ExistsAsync(int id)`                        | Verifica de manera asíncrona si una flota con el identificador dado (`id`) ya existe en el repositorio. |

* Aggregate: MaintenanceRecord  
**Descripción:**  El agregado "MaintenanceRecord" actúa como la raíz del modelo, encapsulando los datos esenciales de un registro de mantenimiento de un vehículo, incluyendo detalles sobre el vehículo, tipo de mantenimiento, costo, fechas y estado. Su representación en la base de datos se realiza mediante la tabla `maintenance_records`, asegurando la persistencia de esta entidad clave.

| Atributo             | Tipo            | Descripción                                                                 |
|----------------------|-----------------|-----------------------------------------------------------------------------|
| `Id`                 | `int`           | Identificador único del registro de mantenimiento.                          |
| `VehicleId`          | `int`           | Identificador del vehículo al que se le realizó el mantenimiento.           |
| `VehicleLicensePlate`| `string`        | Placa del vehículo al que se le realizó el mantenimiento.                   |
| `VehicleModel`       | `string`        | Modelo del vehículo al que se le realizó el mantenimiento.                  |
| `Description`        | `string`        | Descripción del mantenimiento realizado.                                    |
| `Type`               | `MaintenanceType`| Tipo de mantenimiento realizado (por ejemplo, preventivo, correctivo).      |
| `TypeName`           | `string`        | Nombre del tipo de mantenimiento (`Preventive`, `Corrective`, etc.).         |
| `Cost`               | `decimal`       | Costo del mantenimiento realizado.                                          |
| `ScheduledDate`      | `DateTime`      | Fecha programada para el mantenimiento.                                     |
| `CompletedDate`      | `DateTime?`     | Fecha en que se completó el mantenimiento. Este campo es opcional (`nullable`). |
| `Status`             | `MaintenanceStatus`| Estado del mantenimiento (`Scheduled`, `InProgress`, `Completed`).         |
| `StatusName`         | `string`        | Nombre del estado del mantenimiento basado en el valor de `Status`.         |
| `Notes`              | `string`        | Notas adicionales sobre el mantenimiento realizado.                         |
| `CreatedAt`          | `DateTime`      | Fecha de creación del registro de mantenimiento.                            |
| `UpdatedAt`          | `DateTime`      | Fecha de la última actualización del registro de mantenimiento.             |

### Propiedades Calculadas

| Propiedad           | Tipo        | Descripción                                                                 |
|---------------------|-------------|-----------------------------------------------------------------------------|
| `IsOverdue`         | `bool`      | Indica si el mantenimiento está atrasado, es decir, si no se ha completado y la fecha programada ha pasado. |
| `DaysOverdue`       | `int`       | Número de días que el mantenimiento está atrasado. Si no está atrasado, es `0`. |


| Método                                         | Descripción                                                                                         |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| `UpdateDetails(string description, MaintenanceType type, decimal cost, DateTime scheduledDate, string notes)` | Actualiza los detalles del mantenimiento, incluyendo la descripción, tipo, costo, fecha programada y notas adicionales. Se actualiza la fecha de última modificación (`UpdatedAt`). |
| `UpdateStatus(MaintenanceStatus status, DateTime? completedDate = null)` | Actualiza el estado del mantenimiento (`Status` y `StatusName`). También establece la fecha de finalización del mantenimiento (`CompletedDate`) si se proporciona. Se actualiza la fecha de última modificación (`UpdatedAt`). |
| `SetVehicleInfo(string licensePlate, string model)` | Actualiza la información del vehículo asociado al mantenimiento, incluyendo la placa del vehículo y el modelo. |

* Aggregate: ServiceRecord  
**Descripción:**  El agregado "ServiceRecord" actúa como la raíz del modelo, encapsulando los datos esenciales de un registro de servicio de un vehículo, incluyendo detalles sobre el servicio realizado, costo, proveedor de servicio y kilometraje en el momento del servicio. Su representación en la base de datos se realiza mediante la tabla `service_records`, asegurando la persistencia de esta entidad clave.

| Atributo             | Tipo            | Descripción                                                                 |
|----------------------|-----------------|-----------------------------------------------------------------------------|
| `Id`                 | `int`           | Identificador único del registro de servicio.                              |
| `VehicleId`          | `int`           | Identificador del vehículo al que se le realizó el servicio.               |
| `VehicleLicensePlate`| `string`        | Placa del vehículo al que se le realizó el servicio.                       |
| `ServiceType`        | `string`        | Tipo de servicio realizado (por ejemplo, cambio de aceite, mantenimiento general). |
| `Description`        | `string`        | Descripción detallada del servicio realizado.                              |
| `Cost`               | `decimal`       | Costo del servicio realizado.                                              |
| `ServiceDate`        | `DateTime`      | Fecha en que se realizó el servicio.                                       |
| `MileageAtService`   | `int`           | Kilometraje del vehículo al momento de realizar el servicio.               |
| `ServiceProvider`    | `string`        | Nombre del proveedor o taller que realizó el servicio.                     |
| `CreatedAt`          | `DateTime`      | Fecha de creación del registro del servicio.                               |


| Método                                   | Descripción                                                                                         |
|------------------------------------------|-----------------------------------------------------------------------------------------------------|
| `SetVehicleInfo(string licensePlate)`    | Actualiza la placa del vehículo asociado al registro de servicio (`VehicleLicensePlate`). Este método no afecta la fecha de última modificación (`CreatedAt`). |

* Aggregate: Manager  
**Descripción:**  El agregado "Manager" actúa como la raíz del modelo, encapsulando los datos esenciales de un gerente, incluyendo su nombre, correo electrónico y estado. Su representación en la base de datos se realiza mediante la tabla `managers`, asegurando la persistencia de esta entidad clave.

| Atributo            | Tipo          | Descripción                                                                 |
|---------------------|---------------|-----------------------------------------------------------------------------|
| `Id`                | `Guid`        | Identificador único del gerente.                                            |
| `Name`              | `string`      | Nombre del gerente.                                                          |
| `Email`             | `string`      | Correo electrónico del gerente.                                              |
| `Status`            | `string`      | Estado del gerente: por defecto es "ACTIVE", puede ser "ACTIVE" o "INACTIVE".|


### Métodos de la interfaz `IManagerRepository`

| Método                                 | Descripción                                                                                             |
|----------------------------------------|---------------------------------------------------------------------------------------------------------|
| `GetByIdAsync(Guid id)`                | Obtiene un gerente de manera asíncrona a partir de su identificador único (`id`).                        |
| `GetAllAsync()`                        | Obtiene todos los gerentes de manera asíncrona.                                                         |
| `AddAsync(Manager manager)`            | Agrega un nuevo gerente al repositorio de manera asíncrona.                                              |


#### 2.6.1.2. Interface Layer

**Descripción**: El **Interface Layer** o capa de interfaz define cómo los usuarios o sistemas externos interactúan con el sistema. Los controladores reciben y gestionan las solicitudes HTTP, delegando las operaciones a los servicios de aplicación correspondientes. Este layer facilita la entrada y salida de datos entre el sistema y los usuarios, asegurando que las solicitudes sean procesadas correctamente y que las respuestas se entreguen de manera adecuada.

**Justificación**: Los controladores en esta capa, como `AssignmentController`, `MaintenanceController`, y `VehicleController`, manejan las solicitudes relacionadas con asignaciones de tareas, mantenimiento de vehículos y gestión de flotas. Cada uno de estos controladores se apoya en servicios específicos de la capa de aplicación, como `AssignmentCommandService`, `MaintenanceQueryService` y `VehicleCommandService`, para ejecutar las operaciones necesarias. La capa de interfaz canaliza las solicitudes, realizando las validaciones necesarias y devolviendo las respuestas apropiadas, asegurando una interacción eficiente entre los usuarios y el sistema.


- **Controlador**: AssignmentController

**Descripción**: Controlador que maneja los endpoints relacionados con las asignaciones de tareas, permitiendo la creación, inicio y finalización de las asignaciones.

| Método         | Ruta                                      | Descripción                                                                                          |
|----------------|-------------------------------------------|------------------------------------------------------------------------------------------------------|
| `createAssignment` | `POST /api/assignments`                   | Crea una nueva asignación, asignando un vehículo y un conductor a una tarea.                         |
| `startAssignment`  | `POST /api/assignments/{id}/start`        | Cambia el estado de una asignación a "IN_PROGRESS".                                                   |
| `completeAssignment` | `POST /api/assignments/{id}/complete`    | Cambia el estado de una asignación a "COMPLETED" y establece la fecha de finalización.               |

| Dependencias            | Descripción                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------|
| `AssignmentCommandService` | Servicio encargado de manejar los comandos relacionados con la creación, inicio y finalización de asignaciones. |
| `AssignmentQueryService` | Servicio encargado de manejar las consultas relacionadas con las asignaciones.               |
| `AssignmentResourceFromEntityAssembler` | Utilidad para convertir las entidades de asignaciones en recursos que se envían en la respuesta. |

---

- **Controlador**: MaintenanceController

**Descripción**: Controlador que maneja los endpoints relacionados con las órdenes de mantenimiento y los registros de servicio, permitiendo crear nuevas órdenes, realizar seguimientos y consultar registros.

| Método          | Ruta                                    | Descripción                                                                                           |
|-----------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------|
| `createMaintenanceOrder` | `POST /api/maintenance/orders`           | Crea una nueva orden de mantenimiento para un vehículo.                                                |
| `getMaintenanceRecords`  | `GET /api/maintenance/records/{id}`      | Obtiene un registro de mantenimiento específico para un vehículo.                                      |
| `getAllMaintenanceRecords`  | `GET /api/maintenance/records`           | Obtiene todos los registros de mantenimiento de vehículos.                                            |

| Dependencias                | Descripción                                                                                 |
|-----------------------------|---------------------------------------------------------------------------------------------|
| `MaintenanceOrderCommandService` | Servicio encargado de manejar los comandos relacionados con la creación de órdenes de mantenimiento. |
| `MaintenanceRecordQueryService` | Servicio encargado de manejar las consultas relacionadas con los registros de mantenimiento.      |
| `MaintenanceRecordResourceFromEntityAssembler` | Utilidad para convertir las entidades de mantenimiento en recursos que se envían en la respuesta.   |

---

- **Controlador**: VehicleController

**Descripción**: Controlador que maneja los endpoints relacionados con la gestión de vehículos, incluyendo la creación y consulta de vehículos en la flota.

| Método           | Ruta                                      | Descripción                                                                                          |
|------------------|-------------------------------------------|------------------------------------------------------------------------------------------------------|
| `createVehicle`  | `POST /api/vehicles`                      | Crea un nuevo vehículo en la flota, asignando sus características como la placa, marca y modelo.     |
| `getVehicle`     | `GET /api/vehicles/{id}`                  | Obtiene un vehículo específico a partir de su ID.                                                     |
| `getAllVehicles` | `GET /api/vehicles`                       | Obtiene todos los vehículos registrados en la flota.                                                 |

| Dependencias              | Descripción                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------|
| `VehicleCommandService`    | Servicio encargado de manejar los comandos relacionados con la creación y gestión de vehículos. |
| `VehicleQueryService`      | Servicio encargado de manejar las consultas relacionadas con los vehículos.                    |
| `VehicleResourceFromEntityAssembler` | Utilidad para convertir las entidades de vehículos en recursos que se envían en la respuesta.  |


#### 2.6.1.3. Application Layer

### Application Layer

**Descripción**: El **Application Layer** orquesta las operaciones que deben ejecutarse para cumplir con las necesidades del usuario, coordinando diferentes servicios y repositorios del sistema. Contiene la lógica específica de las acciones que no necesariamente forman parte del dominio principal, pero son esenciales para el funcionamiento de los sistemas de gestión de asignaciones, mantenimiento, vehículos y flotas. Este layer se encarga de coordinar las actividades entre los controladores y el dominio, garantizando que las solicitudes del usuario sean procesadas correctamente.

**Justificación**: En este contexto, los servicios `AssignmentCommandService`, `MaintenanceOrderCommandService`, `VehicleCommandService`, y `FleetCommandService` gestionan las reglas de negocio relacionadas con las asignaciones de tareas, órdenes de mantenimiento, vehículos y flotas. Estos servicios se encargan de ejecutar los comandos y consultas relacionadas con la creación, actualización, inicio y finalización de tareas, mantenimiento y gestión de vehículos. La capa de aplicación se comunica con sus respectivos repositorios (`AssignmentRepository`, `MaintenanceOrderRepository`, `VehicleRepository`, `FleetRepository`), asegurando que la lógica de negocio esté correctamente aplicada y que las interacciones con el dominio se realicen de manera eficiente.

### Servicio: AssignmentService
**Descripción**: Implementación del servicio encargado de gestionar las asignaciones de tareas, permitiendo su creación, inicio y finalización.

| Método                                         | Descripción                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| `Create(Guid vehicleId, Guid driverId, string route)` | Crea una nueva asignación para un vehículo y un conductor, asignándolos a una ruta específica.         |
| `GetAll()`                                     | Obtiene todas las asignaciones existentes en el sistema.                                              |
| `Start(Guid id)`                               | Inicia una asignación existente, cambiando su estado a "IN_PROGRESS".                                 |
| `Complete(Guid id)`                            | Completa una asignación existente, cambiando su estado a "COMPLETED" y estableciendo la fecha de finalización. |

### Dependencias

| Dependencia                     | Descripción                                                                                 |
|----------------------------------|---------------------------------------------------------------------------------------------|
| `IAssignmentRepository`          | Repositorio encargado de manejar la persistencia de las asignaciones.                        |
| `Assignment`                     | Entidad que representa una asignación de tarea en el dominio.                               |
| `AssignmentDto`                  | DTO (Data Transfer Object) que representa una asignación para la respuesta.                 |
| `AssignmentCommandService`       | Servicio que maneja la lógica de negocio asociada con la creación, inicio y finalización de asignaciones. |

### Servicio: MaintenanceService
**Descripción**: Implementación del servicio encargado de gestionar los registros de mantenimiento y servicio de vehículos, permitiendo la creación, obtención, actualización y eliminación de registros de mantenimiento y servicio.

| Método                                         | Descripción                                                                                           |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| `CreateMaintenanceRecord(CreateMaintenanceRecordRequest request)` | Crea un nuevo registro de mantenimiento para un vehículo, asignando los detalles de mantenimiento como la descripción, tipo, costo, etc. |
| `GetAllMaintenanceRecords()`                   | Obtiene todos los registros de mantenimiento de vehículos existentes en el sistema.                  |
| `GetMaintenanceRecordById(int id)`             | Obtiene un registro específico de mantenimiento a partir de su ID.                                      |
| `GetMaintenanceRecordsByVehicle(int vehicleId)`| Obtiene todos los registros de mantenimiento asociados a un vehículo específico.                      |
| `GetOverdueMaintenanceRecords()`               | Obtiene todos los registros de mantenimiento que están atrasados.                                      |
| `UpdateMaintenanceRecord(int id, UpdateMaintenanceRecordRequest request)` | Actualiza los detalles de un registro de mantenimiento existente.                                      |
| `DeleteMaintenanceRecord(int id)`              | Elimina un registro de mantenimiento, marcándolo como inactivo (soft delete).                          |

### Dependencias

| Dependencia                         | Descripción                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------|
| `IMaintenanceRecordRepository`       | Repositorio encargado de manejar la persistencia de los registros de mantenimiento.         |
| `MaintenanceRecordDto`               | DTO (Data Transfer Object) que representa un registro de mantenimiento para la respuesta.   |
| `MaintenanceOrderCommandService`     | Servicio encargado de la lógica de negocio relacionada con las órdenes de mantenimiento.     |
| `MaintenanceRecord`                  | Entidad que representa un registro de mantenimiento de vehículo en el dominio.              |

### Servicio: VehicleService

**Descripción**: Implementación del servicio encargado de gestionar los vehículos, permitiendo su registro, obtención, actualización, eliminación y asignación de conductores.

| Método                                   | Descripción                                                                                             |
|------------------------------------------|---------------------------------------------------------------------------------------------------------|
| `RegisterVehicleAsync(CreateVehicleDto createDto)` | Registra un nuevo vehículo en el sistema, asignando su placa, marca, modelo y otros detalles.          |
| `GetAllVehiclesAsync()`                  | Obtiene todos los vehículos registrados en el sistema.                                                  |
| `GetVehicleByIdAsync(int id)`            | Obtiene un vehículo específico por su ID.                                                               |
| `UpdateVehicleAsync(int id, UpdateVehicleDto updateDto)` | Actualiza un vehículo existente con nueva información, como kilometraje, fechas de servicio, conductor y estado. |
| `DeleteVehicleAsync(int id)`             | Elimina un vehículo marcándolo como inactivo en lugar de eliminarlo físicamente.                        |

### Dependencias

| Dependencia                   | Descripción                                                                                 |
|--------------------------------|---------------------------------------------------------------------------------------------|
| `IVehicleRepository`           | Repositorio encargado de manejar la persistencia de los vehículos.                           |
| `VehicleDto`                   | DTO (Data Transfer Object) que representa un vehículo para la respuesta.                    |
| `VehicleCommandService`        | Servicio encargado de la lógica de negocio relacionada con la creación, actualización y gestión de vehículos. |

---

### Servicio: DriverService

**Descripción**: Implementación del servicio encargado de gestionar los conductores, permitiendo su registro, obtención, actualización, eliminación y asignación de vehículos.

| Método                                   | Descripción                                                                                             |
|------------------------------------------|---------------------------------------------------------------------------------------------------------|
| `RegisterDriverAsync(CreateDriverDto createDto)` | Registra un nuevo conductor en el sistema, asignando los detalles proporcionados como código, nombre, licencia, etc. |
| `GetAllDriversAsync()`                   | Obtiene todos los conductores registrados en el sistema.                                                |
| `GetDriverByIdAsync(int id)`             | Obtiene un conductor específico por su ID.                                                              |
| `UpdateDriverAsync(int id, UpdateDriverDto updateDto)` | Actualiza la información de un conductor existente, como nombre, licencia, vehículo asignado y estado. |
| `DeleteDriverAsync(int id)`              | Elimina un conductor del sistema, marcándolo como inactivo (soft delete).                             |
| `GetDriverStatsAsync()`                  | Obtiene estadísticas sobre los conductores, como total de conductores, conductores activos, inactivos, con licencias expiradas, etc. |

### Dependencias

| Dependencia                   | Descripción                                                                                 |
|--------------------------------|---------------------------------------------------------------------------------------------|
| `IDriverRepository`            | Repositorio encargado de manejar la persistencia de los conductores.                         |
| `DriverDto`                    | DTO (Data Transfer Object) que representa un conductor para la respuesta.                    |
| `DriverStatsDto`               | DTO que representa las estadísticas de los conductores.                                      |

---

### Servicio: AuthService

**Descripción**: Implementación del servicio encargado de gestionar la autenticación de usuarios, incluyendo el registro, inicio de sesión, actualización de perfil y cambio de contraseña.

| Método                                   | Descripción                                                                                             |
|------------------------------------------|---------------------------------------------------------------------------------------------------------|
| `Register(RegisterRequest request)`      | Registra un nuevo usuario en el sistema con la información proporcionada (nombre, correo, contraseña, rol). |
| `Login(LoginRequest request)`            | Inicia sesión de un usuario, generando un token JWT si las credenciales son correctas.               |
| `GetUserByIdAsync(int id)`               | Obtiene un usuario específico por su ID.                                                              |
| `GetUserByEmailAsync(string email)`      | Obtiene un usuario específico por su correo electrónico.                                             |
| `GetAllUsersAsync()`                     | Obtiene todos los usuarios registrados en el sistema.                                                |
| `UpdateProfileAsync(int id, UpdateProfileRequest request)` | Actualiza el perfil de un usuario específico, permitiendo cambios en su nombre y apellido.           |
| `ChangePasswordAsync(int id, ChangePasswordRequest request)` | Cambia la contraseña de un usuario verificando la contraseña actual y actualizando con una nueva.     |
| `DeactivateUserAsync(int id)`            | Desactiva un usuario, marcándolo como inactivo.                                                      |

### Dependencias

| Dependencia                   | Descripción                                                                                 |
|--------------------------------|---------------------------------------------------------------------------------------------|
| `IUserRepository`              | Repositorio encargado de manejar la persistencia de los usuarios.                            |
| `UserDto`                      | DTO (Data Transfer Object) que representa un usuario para la respuesta.                     |
| `PasswordHasher<User>`         | Utilidad para la creación y verificación de contraseñas de usuarios.                         |
| `JwtSecurityTokenHandler`      | Utilidad para la generación y manejo de tokens JWT para la autenticación.                    |



#### 2.6.1.4. Infrastructure Layer


**Descripción**: El **Infrastructure Layer** se encarga de proporcionar acceso a la base de datos, servicios externos y otros detalles técnicos relacionados con la persistencia y la infraestructura subyacente del sistema. Este layer actúa como la implementación real de la persistencia de datos, gestionando la interacción con la base de datos y otros recursos técnicos necesarios para el funcionamiento del sistema.

**Justificación**: Los diferentes repositorios, como `VehicleRepository`, `DriverRepository`, `AssignmentRepository`, y `MaintenanceRepository`, son responsables de la persistencia de los vehículos, conductores, asignaciones y registros de mantenimiento, respectivamente. Los métodos proporcionados en estos repositorios permiten interactuar directamente con la base de datos para almacenar, recuperar, actualizar y eliminar datos. Este layer asegura que los datos se gestionen correctamente desde la infraestructura subyacente, separando las preocupaciones técnicas de las reglas de negocio. La implementación en esta capa permite que la lógica de negocio en la capa de aplicación permanezca independiente de los detalles técnicos de la persistencia.

### Repositorio: **AssignmentRepository**

**Descripción**: Repositorio de acceso a datos para la entidad **Assignment**, utilizando **Entity Framework Core (EF Core)** para realizar operaciones de persistencia.

| Método                                      | Descripción                                                                                           |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------|
| `GetByIdAsync(Guid id)`                     | Busca una asignación específica por su ID.                                                           |
| `GetAllAsync()`                             | Obtiene todas las asignaciones registradas en el sistema.                                             |
| `AddAsync(Assignment assignment)`           | Agrega una nueva asignación al sistema y guarda los cambios en la base de datos.                      |
| `UpdateAsync(Assignment assignment)`        | Actualiza una asignación existente y guarda los cambios en la base de datos.                          |

### Dependencias

| Dependencia                 | Descripción                                                                                 |
|-----------------------------|---------------------------------------------------------------------------------------------|
| `AppDbContext`               | Contexto de la base de datos, utilizado para interactuar con las tablas de la base de datos. |
| `Assignment`                 | Entidad que representa una asignación en el dominio del sistema.                           |
| `Entity Framework Core`      | Framework utilizado para las operaciones de persistencia, como `FindAsync`, `ToListAsync`, `AddAsync`, y `Update`. |

### Repositorio: **UserRepository**

**Descripción**: Repositorio de acceso a datos para la entidad **User**, utilizando **Entity Framework Core (EF Core)** para realizar operaciones de persistencia.

| Método                                      | Descripción                                                                                           |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------|
| `GetByEmailAsync(string email)`             | Busca un usuario específico por su correo electrónico.                                                |
| `GetByIdAsync(int id)`                      | Busca un usuario específico por su ID.                                                                |
| `AddAsync(User user)`                       | Agrega un nuevo usuario al sistema y guarda los cambios en la base de datos.                          |
| `UpdateAsync(User user)`                    | Actualiza un usuario existente y guarda los cambios en la base de datos.                              |
| `GetAllAsync()`                             | Obtiene todos los usuarios registrados en el sistema.                                                |

### Dependencias

| Dependencia                 | Descripción                                                                                 |
|-----------------------------|---------------------------------------------------------------------------------------------|
| `AppDbContext`               | Contexto de la base de datos, utilizado para interactuar con las tablas de la base de datos. |
| `User`                       | Entidad que representa un usuario en el dominio del sistema.                                |
| `Entity Framework Core`      | Framework utilizado para las operaciones de persistencia, como `FindAsync`, `FirstOrDefaultAsync`, `AddAsync`, `Update`, y `ToListAsync`. |

### Repositorio: **DriverRepository**

**Descripción**: Repositorio de acceso a datos para la entidad **Driver**, utilizando **Entity Framework Core (EF Core)** para realizar operaciones de persistencia.

| Método                                      | Descripción                                                                                           |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------|
| `GetByIdAsync(int id)`                      | Busca un conductor específico por su ID.                                                              |
| `GetAllAsync()`                             | Obtiene todos los conductores registrados en el sistema.                                              |
| `AddAsync(Driver driver)`                   | Agrega un nuevo conductor al sistema y guarda los cambios en la base de datos.                        |
| `UpdateAsync(Driver driver)`                | Actualiza un conductor existente y guarda los cambios en la base de datos.                            |

### Dependencias

| Dependencia                 | Descripción                                                                                 |
|-----------------------------|---------------------------------------------------------------------------------------------|
| `AppDbContext`               | Contexto de la base de datos, utilizado para interactuar con las tablas de la base de datos. |
| `Driver`                     | Entidad que representa un conductor en el dominio del sistema.                              |
| `Entity Framework Core`      | Framework utilizado para las operaciones de persistencia, como `FindAsync`, `ToListAsync`, `AddAsync` y `Update`. |

### Repositorio: **VehicleRepository**

**Descripción**: Repositorio de acceso a datos para la entidad **Vehicle**, utilizando **Entity Framework Core (EF Core)** para realizar operaciones de persistencia.

| Método                                      | Descripción                                                                                           |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------|
| `GetByIdAsync(int id)`                      | Busca un vehículo específico por su ID.                                                                |
| `AddAsync(Vehicle vehicle)`                 | Agrega un nuevo vehículo al sistema y guarda los cambios en la base de datos.                          |
| `UpdateAsync(Vehicle vehicle)`              | Actualiza un vehículo existente y guarda los cambios en la base de datos.                              |
| `GetAllAsync()`                             | Obtiene todos los vehículos registrados en el sistema.                                                |

### Dependencias

| Dependencia                 | Descripción                                                                                 |
|-----------------------------|---------------------------------------------------------------------------------------------|
| `AppDbContext`               | Contexto de la base de datos, utilizado para interactuar con las tablas de la base de datos. |
| `Vehicle`                    | Entidad que representa un vehículo en el dominio del sistema.                               |
| `Entity Framework Core`      | Framework utilizado para las operaciones de persistencia, como `FindAsync`, `ToListAsync`, `AddAsync` y `Update`. |

### Repositorio: **FleetRepository**

**Descripción**: Repositorio de acceso a datos para la entidad **Fleet**, utilizando **Entity Framework Core (EF Core)** para realizar operaciones de persistencia.

| Método                                      | Descripción                                                                                           |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------|
| `GetByIdAsync(int id)`                      | Busca una flota específica por su ID.                                                                |
| `GetAllAsync()`                             | Obtiene todas las flotas registradas en el sistema, ordenadas por nombre.                             |
| `AddAsync(Fleet fleet)`                     | Agrega una nueva flota al sistema y guarda los cambios en la base de datos.                           |
| `UpdateAsync(Fleet fleet)`                  | Actualiza una flota existente y guarda los cambios en la base de datos.                               |
| `DeleteAsync(int id)`                       | Elimina una flota específica por su ID.                                                               |
| `ExistsAsync(int id)`                       | Verifica si una flota con el ID especificado existe en el sistema.                                   |

### Dependencias

| Dependencia                 | Descripción                                                                                 |
|-----------------------------|---------------------------------------------------------------------------------------------|
| `AppDbContext`               | Contexto de la base de datos, utilizado para interactuar con las tablas de la base de datos. |
| `Fleet`                      | Entidad que representa una flota en el dominio del sistema.                                 |
| `Entity Framework Core`      | Framework utilizado para las operaciones de persistencia, como `FindAsync`, `ToListAsync`, `AddAsync`, `Update`, `Remove` y `AnyAsync`. |


#### 2.6.1.5. Bounded Context Software Architecture Component Level Diagrams

Este diagrama de contenedores refleja la estructura y componentes clave de nuestro Sistema de Gestión de Flotas. En él, mostramos cómo interactúan los distintos actores, sistemas y servicios dentro de la plataforma para gestionar y optimizar las asignaciones de vehículos, conductores y mantenimientos. El administrador es el principal usuario del sistema, encargado de gestionar las asignaciones, los vehículos, los conductores y el mantenimiento de los vehículos, mientras que los diversos componentes y servicios como las APIs, servicios de comandos, repositorios y herramientas externas trabajan juntos para facilitar la creación, actualización, almacenamiento y notificación de información clave. Este diagrama nos ayuda a visualizar cómo cada parte del sistema contribuye a una experiencia fluida y eficiente para nuestros usuarios y asegura una gestión efectiva de la flota de vehículos. 


<img src="../images/chapter-II/Tactital DDD.PNG" alt="alt text" width="800"/>  


#### 2.6.1.6. Bounded Context Software Architecture Code Level Diagrams
##### 2.6.1.6.1. Bounded Context Domain Layer Class Diagrams

##### 2.6.1.6.2. Bounded Context Database Design Diagram

El diagrama de base de datos para el Bounded Context de Gestión de Flotas detalla el esquema relacional que soporta la persistencia del modelo de dominio. La tabla principal vehicles incluye columnas como id (PK, autoincremental) y campos de auditoría (created_at, updated_at). La tabla drivers contiene columnas como id (PK), first_name, last_name, license_number, entre otras.

La relación uno-a-muchos entre drivers y vehicles nos muestra que un conductor puede estar asignado a múltiples vehículos, lo que facilita la asignación de vehículos a conductores. Además, la relación entre assignments (asignaciones) y vehicles nos permite gestionar las asignaciones de vehículos a tareas, mostrando cómo cada vehículo puede ser asignado a diversas tareas a lo largo del tiempo.