# 4. Product Implementation & Validation

## 4.1. Software Configuration Management
### 4.1.1. Software Development Environment Configuration
### 4.1.2. Source Code Management
### 4.1.3. Source Code Style Guide & Conventions
### 4.1.4. Software Deployment Configuration

## 4.2. Landing Page & Mobile Application Implementation
El desarrollo, testeo y despliegue de nuestra landing page es importante para que nuestros clientes puedan acceder a la información sobre nuestra empresa y producto a través de una interfaz con diseño responsivo, navegación intuitiva y solo con información relevante. Esta primera etapa nos permite crear un diseño conceptual sobre la estética que nuestra aplicación completa y lista para su uso. Estas etapas nos ayudaran a dar una primera impresión a los clientes para validar ideas e identificar problemas que se deben solucionar.  

### 4.2.1. Sprint 1

### Project Management
  * ### Meet
    Una herramienta de videoconferencias que posibilita la comunicación en tiempo real del grupo para reuniones de coordinación.
  
    Imagen de evidencia de uso
  
    ![alt text](../images/chapter-IV/GoogleMeet.png)


    ![alt text](../images/chapter-IV/MeetEvidence.png)
    
  * ### Requirement Management
    * ### Draw.io
    Se trata de una suite de herramientas que posibilita la creación colaborativa de modelos C4 para representar de forma gráfica nuestros productos.
    
    Imagen de evidencia de uso
  
    ![alt text](../images/chapter-IV/Draw.io.tool.png)
  
  * ### Product UX/UI Design
    * ### Figma
    Herramienta visual que facilita la creación de wireframes y mockups.
  
    Imagen de evidencia de uso
  
    ![alt text](../images/chapter-IV/Figma%20EVI.PNG)
  
  * ### Software Development
    * ### HTML5
    Lenguaje de etiquetado orientado a crear páginas web.
  
    Imagen de evidencia de uso
  
    ![alt text](../images/chapter-IV/HTML%20EVI.PNG)
  
    * ### CSS
    Lenguaje de diseño gráfico utilizado para dar formato al código escrito en HTML.
  
    Imagen de evidencia de uso
  
    ![alt text](../images/chapter-IV/CSS%20EVI.PNG)
  
    * ### Javascript
    Lenguaje de programación orientado a objetos dinámico que utilizamos para implementar funcionalidades en un documento HTML.
  
    Imagen de evidencia de uso
  
    ![alt text](../images/chapter-IV/JS%20EVI.PNG)
  
  * ### Software Documentation
    * ### Github
    Plataforma utilizada para el alojamiento de versiones del código fuente de un proyecto. Es una herramienta ampliamente popular en el trabajo colaborativo de programadores.  

    ![alt text](../images/chapter-IV/Github%20EVI.PNG)
  
  * ### Software Documentation
    * ### Github Pages
    Una plataforma que posibilita la realización de despliegues simples directamente desde un repositorio de GitHub.  

    ![alt text](../images/chapter-IV/githubpagess.png)
    
### 4.1.2. Source Code Management
El primer sprint es una etapa importante en nuestro marco de gestión de proyectos de metodología ágil Scrum. En este periodo, agendamos reuniones con el objetivo de conocer mejor las características de cada integrante, y delegamos tareas para materializar el diseño y funcionalidades ya establecidas, para transformarlos en un landing page funcional y que cumple las heurísticas.  

#### 4.2.1.1. Sprint Planning 1

El sprint planning es una reunion antes de cada sprint en la metodologia Scrum donde el equipo elige las user stories que va a transformar en un producto tangible. Tambien define que como se van a separar los trabajos y quien sera responsable. Nuestro objetivo sera construir un plan resolubre en un tiempo determinado que sera lo que dure el sprint, para crearlo fomentaremos la colaboracion para que todos sepan y entiendas los objetivos y prioridades.  

| Sprint #| Sprint 1|
| -- | -- |
| **Sprint Planning Background**||
| **Date**| 01/10/2025|
| **Time**| 17:00 AM|
| **Location**| Discord (Reunión virtual)|
| **Prepared By**| Torres Apolinario, Giovany Smith|
| **Attendees (to planning meeting)** | Huamani Sánchez José Diego, Llerena Delgado Renzo Miguel, Comettant Rubiños Jessica Elizabeth, Villafuerte Tapia Renzo Alonso, Torres Apolinario Giovany Smith|
| **Sprint Goal & User Stories**||
| **Sprint 1 Goal**| Nuestro enfoque está en finalizar el informe , desplegar nuestra Landing Page desde el repositorio de GitHub y avanzar bounded context del aplicativo (Tanto IAM como applications). Creemos que esto entrega una experiencia de usuario optimizada a nuestros clientes. Esto se confirmará cuando todas las tareas se muevan a la columna "Terminado" en Trello. |
| **Sprint 1 Velocity**| ------ |
| **Sum of Story Points**| 19 |  


#### 4.2.1.2. Sprint Backlog 1

Durante el primer sprint backlog, reunimos las historias de usuario relacionadas con la página de inicio (landing page). Para facilitar su gestión y organización, las dividimos en tareas más simples y las asignamos a los integrantes del equipo de manera eficiente, utilizando la herramienta Trello. Nuestro enfoque principal fue completar estas historias de usuario en el sprint, con el propósito de desarrollar una landing page funcional, atractiva y fácil de navegar. Además, trabajamos en la elaboración del informe de entrega y en el desarrollo del front-end y back-end de los bounded context **IAM** y **Applications**. Gracias al uso de Trello, logramos una colaboración efectiva y un seguimiento claro del avance de las tareas, lo que nos permitió resolver los desafíos que surgieron durante el proceso.

![alt text](../images/chapter-IV/SprintBacklog1.PNG) 

| Sprint # | Sprint 1 |
|-----------|-----------|

| User Story |  | Work-Item / Task |  |  |  |  |  |
|-------------|--|------------------|--|--|--|--|--|
| ID | Title | ID | Title | Description | Estimation (Hours) | Assigned To | Status |
| --- | --- | --- | --- | --- | --- | --- | --- |
| US01 | Landing Page informativa | TA001 | Integración visual de landing page | Diseñar e implementar la estructura principal de la landing page informativa, incluyendo secciones de presentación y CTA. | 2 | Huamani Sánchez, José Diego | Done |
| US02 | Responsive | TA002 | Adaptación responsive del sitio | Implementar diseño responsive para dispositivos móviles y tablets, garantizando accesibilidad y buena experiencia de usuario. | 1 | Huamani Sánchez, José Diego | Done |
| US03 | Comparador de planes | TA003 | Desarrollo de módulo comparador | Crear un componente que permita comparar distintos planes o servicios mediante tablas dinámicas o tarjetas. | 4 | Torres Apolinario, Giovany Smith | Done |
| US04 | Switcher de idiomas | TA004 | Implementación de selector de idioma | Añadir un switcher que permita cambiar entre idiomas (por ejemplo, español e inglés) usando i18n o similar. | 3 | Comettant Rubiños, Jessica Elizabeth | Done |
| US05 | Tema de colores | TA005 | Configuración de paleta de colores | Definir y aplicar un sistema de temas (claro/oscuro) con variables globales de color y componentes adaptativos. | 2 | Comettant Rubiños, Jessica Elizabeth | Done |
| US06 | Vista de developers | TA006 | Construcción de vista para desarrolladores | Diseñar una vista con documentación técnica y herramientas de prueba para el equipo de desarrollo. | 3 | Torres Apolinario, Giovany Smith | Done |
| US07 | Registro de nuevo usuario | TA007 | Implementación del formulario de registro | Crear un formulario de registro con validaciones y conexión al backend para nuevos usuarios. | 3 | Renzo Miguel Llerena Delgado | Done |
| US09 | Registro de vehículo | TA008 | Formulario de registro vehicular | Desarrollar un formulario para registrar datos de vehículos con validación y confirmación visual. | 2 | Renzo Miguel Llerena Delgado | Done |
| US11 | Footer informativo | TA009 | Creación del pie de página informativo | Diseñar un footer con enlaces de contacto, políticas de privacidad y redes sociales. | 2 | Huamani Sánchez, José Diego  | Done |
| US12 | Información conductor | TA010 | Visualización de datos del conductor | Implementar componente que muestre información detallada del conductor (nombre, licencia, historial). | 1 | Renzo Alonso Villafuerte Tapia  | Done |
| US14 | Información del vehículo | TA011 | Módulo de detalles del vehículo | Crear una vista con los datos completos del vehículo: modelo, placa, estado y revisiones. | 3 | NARenzo Alonso Villafuerte Tapia ME | Done |



Link de Trello: https://trello.com/invite/b/68e3edd7fb5340b5154772f4/ATTI2ddb91b7af2a322ff81b700ac8f837b3DF4CD98A/sprint-1-flota365

#### 4.2.1.3. Development Evidence for Sprint Review
Landing Page:

|Repository |Branch| Commit Id | Commit Message| Commit Message Body| Date|
|----|-----|---------------------|----------------------------------------|---------------------------------------------------------|------------|
|Flota365/landing-page|develop| 2753d07           | feat(header): add the header and navigations  | the access with differents informative articles about Flota365 Startup | 05/10/2025 |
|Flota365/landing-page|develop| 184f6f5           | feat(hero): add the new version of Hero Section o n the Flota365 Landing Page         | Added hero section with headline | 05/10/2025 |
|Flota365/landing-page|develop| a831a7f           | feat(features): add the primordial features  | features of Flota365 offers our customers         | 05/10/2025 |
|Flota365/landing-page|develop| 74000b4           | feat(about): add the first vertion of About section    | Implemented company info section with team photos       | 05/10/2025 |
|Flota365/landing-page|develop| c5ab48a           | feat(contact): Add contact information | add the contact forms into the Landing Page of Flota465 | 05/10/2025 |
|Flota365/landing-page|develop| 3473e3f           | Chore(colors): update the color palette     | Implemented apply into the new navigation items  | 05/10/2025 |
|Flota365/landing-page|develop| 681332a           | feat(stats): add the stadistics   | Implemented information about the advantage to use Flota365   | 05/10/2025 |
|Flota365/landing-page|develop| 932bd47           | feat(team): add the group of developers | Implemented  team member of Flota365 into the Landing Page   | 05/10/2025 |
|Flota365/landing-page|develop| 71f42b3           | feat(footer): add Footer   | content that descripve the differents informative article about the service   | 05/10/2025 |

BackEnd: 
| Repository | Branch         | Commit Id | Commit Message                                               | Commit Message Body                                                                                                                                                                                                                                                                                                                                                                     | Date        |
|------------|---------------|-----------|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| FlotaAPI   | main          | a6f0ca4   | chore: configurar gitignore para .NET y limpiar bin/obj       | Se añadió plantilla de .gitignore para proyectos .NET a fin de excluir bin/, obj/, .vs/, archivos de usuario (*.user) y artefactos de compilación.                                                                                                                                                                                                                                         | 06/10/2025  |
| FlotaAPI   | main          | 96ab590   | docs(readme): guía de ejecución local y migraciones EF Core   | Actualización de README-BACKEND.md con pasos para: variables de entorno, dotnet run, creación de migraciones, actualización de base de datos y URLs clave.                                                                                                                                                                                                                                | 06/10/2025  |
| FlotaAPI   | main          | 54991b1   | chore: inicializar proyecto base con estructura DDD           | Se creó la estructura inicial del proyecto siguiendo Domain-Driven Design, incluyendo las carpetas para Domain, Application, Infrastructure y API. También se configuraron los archivos base de gitignore y launch settings.                                                                                                                                                             | 07/10/2025  |
| FlotaAPI   | deploy-koyeb | e0f60d3   | Update Dockerfile                                           | Actualización del archivo Dockerfile para la configuración de despliegue.                                                                                                                                                                                                                                                                                                                  | 07/10/2025  |
| FlotaAPI   | deploy-koyeb | e23ff70   | Fix Dockerfile paths and set port for Koyeb                 | Corrección de rutas en el Dockerfile y establecimiento de puerto para despliegue en Koyeb.                                                                                                                                                                                                                                                                                                 | 07/10/2025  |
| FlotaAPI   | main          | 24d6996   | chore(security): configurar CORS para frontend local         | Se habilitó CORS en Program.cs permitiendo orígenes http://localhost:5173 y http://localhost:4200, métodos comunes (GET, POST, PUT, DELETE) y cabeceras necesarias para JWT. Esto permite la integración con el frontend en desarrollo.                                                                                                                                                      | 07/10/2025  |
| FlotaAPI   | main          | 797833c   | refactor(Extensions): métodos de extensión para DI, Swagger y CORS | Se movió la configuración repetida de Program.cs a la carpeta Extensions (AddSwagger, AddCorsPolicy, AddApplicationServices). Mejora de mantenibilidad y separación de responsabilidades. Program.cs queda más limpio y declarativo.                                                                                                                                                          | 07/10/2025  |
| FlotaAPI   | main          | 3132fba   | docs(api): documentar API con Swagger/OpenAPI y ejemplos     | Se habilitó Swagger con documentación de los módulos Auth, Fleets, DriverManagement, Assignments, Maintenance, Reporting y Dashboard. Se añadieron ejemplos de request/response y descripciones de códigos de estado. Disponible en /swagger.                                                                                                                                              | 07/10/2025  |
| FlotaAPI   | main          | 6a85612   | feat(): endpoint de métricas para tablero                    | Se añadió Dashboard con un endpoint /api/dashboard/metrics que consolida KPIs de Reporting (flotas, conductores, asignaciones, MTTR de mantenimiento). Ideal para la vista analítica del frontend. Incluye caché en memoria de 60 segundos.                                                                                                                                                | 07/10/2025  |
| FlotaAPI   | main          | 648ccf6   | refactor(Management): separar contratos (DTO/Command/Query) y servicios | Se reorganizó Management para adoptar CQRS ligero: comandos y queries separados, perfiles de AutoMapper y servicios de aplicación específicos. Mejora la claridad y testabilidad de la lógica.                                                                                                                                                                                             | 07/10/2025  |


#### 4.2.1.4. Testing Suite Evidence for Sprint Review
Evidencia de prueba unitaria al Flota365-API

![unit](../images/chapter-IV/UnitTest.png)
<br>

#### 4.2.1.5. Execution Evidence for Sprint Review

En este Sprint, los miembros del equipo de desarrollo de software de Aventis han completado y desplegado la Landing Page. A continuación, mostramos imágenes que demuestran cómo nuestra página presenta de manera clara e intuitiva la información sobre nuestro producto y nuestra empresa.

<br>

![deploy](../images/chapter-IV/Landing%20Evi1.PNG)
<br>

![deploy](../images/chapter-IV/Landing%20Evi2.PNG)
<br>

![deploy](../images/chapter-IV/Landing%20Evi3.PNG)
<br>

![deploy](../images/chapter-IV/Landing%20Evi4.PNG)
<br>

![deploy](../images/chapter-IV/Landing%20Evi5.PNG)
<br>

![deploy](../images/chapter-IV/Landing%20Evi6.PNG)
<br>

En segundo lugar ,se avanzo el bounded context IAM y applications tanto en backend como en frontend :

Backend - Swagger:

![alt text](../images/chapter-IV/Swagger1.PNG) 
![alt text](../images/chapter-IV/Swagger2.PNG) 
![alt text](../images/chapter-IV/Swagger3.PNG) 

Frontend - AndroidStudio:  

##### Pantalla de OnBoarding
![alt text](../images/chapter-IV/OnBoarding.png)
##### Pantalla de LoginWelcome
![alt text](../images/chapter-IV/LoginWelcome.png)
##### Pantalla de LoginForm
![alt text](../images/chapter-IV/LoginForm.png)
##### Pantalla de Reportes
![alt text](../images/chapter-IV/ReportsScreen.png)
##### Pantalla de RoleSection
![alt text](../images/chapter-IV/RoleSection.png)
##### Pantalla de Dashboard
![alt text](../images/chapter-IV/Dashboard.png)
##### Pantalla de DriverFleet
![alt text](../images/chapter-IV/DriverFleet.png)
##### Pantalla de ManagerRegistration
![alt text](../images/chapter-IV/ManagerRegistration.png)

## 4.2. Landing Page & Mobile Application Implementation

En esta sección se describe de manera integral el proceso de implementación, pruebas, documentación y despliegue de los distintos componentes que conforman la solución Flota365.

Se incluye el desarrollo de la **Landing Page**, diseñada como punto de entrada y presentación del producto ante el público general, así como la implementación del **Backend** y las **aplicaciones móviles**, que constituyen el núcleo funcional de la propuesta.

A lo largo de esta sección se detalla cómo se abordó cada fase del ciclo de vida del desarrollo de software, desde la planificación inicial y el diseño, hasta la ejecución de pruebas y el despliegue en entornos de producción. Asimismo, se documentan las tecnologías empleadas, los principales desafíos enfrentados y las soluciones adoptadas para garantizar que cada componente cumpla con los requisitos establecidos y proporcione una experiencia de usuario óptima, confiable y escalable.

### 4.2.1. Sprint 1

Este archivo describe el trabajo realizado durante el Sprint 1 del proyecto Flota365. 
El enfoque principal fue el desarrollo y despliegue de la Landing Page, cuyo propósito es ofrecer una primera impresión positiva y brindar información esencial a los potenciales clientes de la plataforma.

#### 4.2.1.1. Sprint Planning 1

En esta sección, se presentará el sprint planning 1 donde se describirá de manera detallada cada una de las evidencias planificadas e implementación tanto en el *Landing Page*, *Web Service* y *Mobile Application*. Asimismo, se evidenciaron los avances del proyeto e *insights* de colaboración en equipo mediante nuestro organización de Github.

<table>
    <thead>
        <tr>
            <th>Sprint #</th>
            <th>Sprint 1</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td colspan="2"><b>Sprint Planning Background</b></td>
        </tr>
        <tr>
            <td>Date</td>
            <td>2025/10/01</td>
        </tr>
        <tr>
            <td>Time</td>
            <td>12:28 AM</td>
        </tr>
        <tr>
            <td>Location</td>
            <td>Discord</td>
        </tr>
        <tr>
            <td>Prepared by</td>
            <td>José Diego Huamani Sánchez</td>
        </tr>
        <tr>
            <td>Atendees (to planning meeting)</td>
            <td>
                Todos los miembros del equipo Flota365
            </td>
        </tr>
        <tr>
            <td>Sprint 1 Review Summary</td>
            <td>
                Dado que es el primer sprint que se está llevando a cabo, no se está considerando los <em>Review Summary</em> ya que no hemos recibido ninguno en el sprint anterior.
            </td>
        </tr>
        <tr>
            <td>Sprint 1 Retrospective Summary</td>
            <td>
                Al ser el primer Sprint, se planea el desarrollo de nuestra landing page mediante el uso de herramientas web nativas como HTML5, CSS3 y JavaScript. Adicional a ello, se tendrá la primera versión del aplicativo móvil que, meadiante el uso de tecnologías como Kotlin y Jetpack Compose, se modelará las vistas core que nuestros segmentos objetivos necesitan - tanto para los gestores de flota como los conductores; este estará conectado a un servicio web, hecho con C#12 y NET.9 donde, mediante una arquitectura Domain Driven Design, estableceremos la conexión entre nuestro servicio con nuestra interfaz móvil.
                Únicamente lo que se desplegará para este entregable es la landing page, usando Github Pages, como el servicio web usando Railways - donde cualquier usuario puede acceder al servicio y visualizar el contenido.
            </td>
        </tr>
        <tr>
            <td colspan="2"><b>Sprint Goal & User Stories</b></td>
        </tr>
        <tr>
            <td>Sprint 1 Velocity</td>
            <td>
                40
            </td>
        </tr>
        <tr>
            <td>Sum of story points</td>
            <td>
                40
            </td>
        </tr>
    </tbody>
</table>

#### 4.2.1.2. Sprint Backlog 1
#### 4.2.1.3. Development Evidence for Sprint Review
#### 4.2.1.4. Testing Suite Evidence for Sprint Review
#### 4.2.1.5. Execution Evidence for Sprint Review
#### 4.2.1.6. Services Documentation Evidence for Sprint Review

En esta sección se presentan los endpoints desarrollados en el presente sprint y se adjuntan captura de las acciones CRUD realizadas con OpenAPI.

Se ajunta el enlace del repositorio de la API en Github: <a href="https://underground-tuesday-renworkplace-1e2821cb.koyeb.app/swagger/index.html">https://underground-tuesday-renworkplace-1e2821cb.koyeb.app/swagger/index.html</a>


<table border="1" style="border-collapse: collapse; text-align: left;">
  <thead>
    <tr>
      <th>Bounded Context</th>
      <td colspan="3">Auth</td>
    </tr>
    <tr>
      <th>Entity</th>
      <th>Endpoint URL</th>
      <th>Swagger</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>User</td>
      <td>
        POST: /api/Auth/register <br>
        POST: /api/Auth/login <br>
        GET: /api/Auth/profile/{id} <br>
        PUT: /api/Auth/profile/{id} <br>
        GET: /api/Auth/profile <br>
        POST: /api/Auth/change-password/{id} <br>
        GET: /api/Auth/users <br>
        DELETE: api/Auth/users/{id} <br>
        GET: /api/Auth/health
      </td>
      <td>
        <img src="../images/chapter-IV/Auth-Endpoint-Web-Services.png" alt="Swagger API Authentication endpoints" style="width:500px;">
      </td>
    </tr>
  </tbody>
</table>

<br>

<table border="1" style="border-collapse: collapse; text-align: left;">
  <thead>
    <tr>
      <th>Bounded Context</th>
      <td colspan="3">Dashboard</td>
    </tr>
    <tr>
      <th>Entity</th>
      <th>Endpoint URL</th>
      <th>Swagger</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>User</td>
      <td>
        GET: /api/Dashboard/stats <br>
        GET: /api/Dashboard/active-vehicles <br>
        GET: /apu/Dashboard/fleet-summary
      </td>
      <td>
        <img src="../images/chapter-IV/Dashboard-Endpoint-Web-Services.png" alt="Swagger API Dashboard endpoints" style="width:500px;">
      </td>
    </tr>
  </tbody>
</table>

<br>

<table border="1" style="border-collapse: collapse; text-align: left;">
  <thead>
    <tr>
      <th>Bounded Context</th>
      <td colspan="3">Driver</td>
    </tr>
    <tr>
      <th>Entity</th>
      <th>Endpoint URL</th>
      <th>Swagger</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>User</td>
      <td>
        POST: /api/Drivers <br>
        GET: /api/Driver <br>
        GET: /api/Driver/{id} <br>
        PUT: /api/Driver/{id} <br>
        DELETE: /api/Driver/{id} <br>
        GET: /api/Driver/stats
      </td>
      <td>
        <img src="../images/chapter-IV/Driver-Endpoint-Web-Services.png" alt="Swagger API Drivers endpoints" style="width:500px;">
      </td>
    </tr>
  </tbody>
</table>

<br>

<table border="1" style="border-collapse: collapse; text-align: left;">
  <thead>
    <tr>
      <th>Bounded Context</th>
      <td colspan="3">Vehicle</td>
    </tr>
    <tr>
      <th>Entity</th>
      <th>Endpoint URL</th>
      <th>Swagger</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>User</td>
      <td>
        POST: /api/Vehicle <br>
        GET: /api/Vehice <br>
        GET: /api/Vehicle/{id} <br>
        PUT: /api/Vehicle/{id} <br>
        DELETE: /api/Vehicle/{id}
      </td>
      <td>
        <img src="../images/chapter-IV/Vehicle-Endpoint-Web-Services.png" alt="Swagger API Vehicles endpoints" style="width:500px;">
      </td>
    </tr>
  </tbody>
</table>

<br>

<table border="1" style="border-collapse: collapse; text-align: left;">
  <thead>
    <tr>
      <th>Bounded Context</th>
      <td colspan="3">Fleets</td>
    </tr>
    <tr>
      <th>Entity</th>
      <th>Endpoint URL</th>
      <th>Swagger</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>User</td>
      <td>
        GET: /api/Fleets <br>
        POST: /api/Fleets <br>
        GET: /api/Fleets/{id} <br>
        PUT: /api/Fleets/{id} <br>
        DELETE: /api/Fleets/{id} <br>
      </td>
      <td>
        <img src="../images/chapter-IV/Fleets-Endpoint-Web-Services.png" alt="Swagger API Fleets endpoints" style="width:500px;">
      </td>
    </tr>
  </tbody>
</table>

<br>

<table border="1" style="border-collapse: collapse; text-align: left;">
  <thead>
    <tr>
      <th>Bounded Context</th>
      <td colspan="3">Maintenance</td>
    </tr>
    <tr>
      <th>Entity</th>
      <th>Endpoint URL</th>
      <th>Swagger</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>User</td>
      <td>
        GET: /api/Maintenance/records <br>
        POST: /api/Maintenance/records <br>
        GET: /api/Maintenance/records/{id} <br>
        PUT: /api/Maintenance/records/{id} <br>
        DELETE: /api/Maintenance/records/{id} <br>
        GET: /api/Maintenance/records/{id} <br>
        GET: /api/Maintenance/records/vehicles/{vehicleId} <br>
        GET: /api/Maintenance/records/overdue <br>
        GET: /api/Maintenance/services <br>
        POST: /api/Maintenance/services <br>
        GET: /api/Maintenance/services/{id} <br>
        DELETE: /api/Maintenance/services/{id} <br>
        GET: /api/Maintenance/services/vehicle/{vehicleId} <br>
      </td>
      <td>
        <img src="../images/chapter-IV/Maintenance-Endpoint-Web-Services.png" alt="Swagger API Maintenance endpoints" style="width:500px;">
      </td>
    </tr>
  </tbody>
</table>

<br>

<table border="1" style="border-collapse: collapse; text-align: left;">
  <thead>
    <tr>
      <th>Bounded Context</th>
      <td colspan="3">Manager</td>
    </tr>
    <tr>
      <th>Entity</th>
      <th>Endpoint URL</th>
      <th>Swagger</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>User</td>
      <td>
        POST: /api/Manager <br>
        GET: /api/Manager
      </td>
      <td>
        <img src="../images/chapter-IV/Manager-Endpoint-Web-Services.png" alt="Swagger API Manager endpoints" style="width:500px;">
      </td>
    </tr>
  </tbody>
</table>

<br>

<table border="1" style="border-collapse: collapse; text-align: left;">
  <thead>
    <tr>
      <th>Bounded Context</th>
      <td colspan="3">Report</td>
    </tr>
    <tr>
      <th>Entity</th>
      <th>Endpoint URL</th>
      <th>Swagger</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>User</td>
      <td>
        POST: /api/Report <br>
        GET: /api/Report
      </td>
      <td>
        <img src="../images/chapter-IV/Report-Endpoint-Web-Services.png" alt="Swagger API Report endpoints" style="width:500px;">
      </td>
    </tr>
  </tbody>
</table>

<br>

<table border="1" style="border-collapse: collapse; text-align: left;">
  <thead>
    <tr>
      <th>Bounded Context</th>
      <td colspan="3">Health</td>
    </tr>
    <tr>
      <th>Entity</th>
      <th>Endpoint URL</th>
      <th>Swagger</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>User</td>
      <td>
        GET: /api/Health <br>
        GET: /api/Health/info
      </td>
      <td>
        <img src="../images/chapter-IV/Health-Endpoint-Web-Services.png" alt="Swagger API Health endpoints" style="width:500px;">
      </td>
    </tr>
  </tbody>
</table>

<table border="1" style="border-collapse: collapse; text-align: left;">
  <thead>
    <tr>
      <th>Bounded Context</th>
      <td colspan="3">Assignment</td>
    </tr>
    <tr>
      <th>Entity</th>
      <th>Endpoint URL</th>
      <th>Swagger</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>User</td>
      <td>
        POST: /api/Assignment <br>
        GET: /api/Assignment <br>
        PUT: /api/Assignment/{id}/start <br>
        PUT: /api/Assignment/{ID}/complete
      </td>
      <td>
        <img src="../images/chapter-IV/Assignment-Endpoint-Web-Services.png" alt="Swagger API Assignment endpoints" style="width:500px;">
      </td>
    </tr>
  </tbody>
</table>

#### 4.2.1.7. Software Deployment Evidence for Sprint Review



#### 4.2.1.8. Team Collaboration Insights during Sprint

Para esta sección del documentos, añadimos los insights realizados durante el sprint, tanto de la realización de la aplicación web, como el landing page:

Insight del Static Web App, donde se muestran los commits realizados en el ultimo mes del repositorio de

**Resumen**

Durante este Sprint, el equipo se centró en la implementación y despliegue de la landing page. Las tareas incluyeron la preparación del entorno, la configuración de recursos y la publicación inicial del sitio web. A continuación, se detalla el proceso seguido para completar el despliegue de la landing page.

---

## **Actividades Realizadas**

### **Creación de Cuentas y Configuración de Recursos**
- **Proveedor de Hosting:** Se seleccionó y configuró el servicio de hosting encargado de alojar la landing page.  
- **Entorno de Trabajo:** Se establecieron los entornos de desarrollo y producción para facilitar las pruebas y futuras actualizaciones.

### **Configuración de Proyectos para Integración**
- **Repositorio de Código:** Se configuró un repositorio en GitHub para gestionar versiones e integrar procesos de despliegue continuo.  
- **Automatización:** Se implementaron scripts y herramientas que permiten automatizar el proceso de despliegue, reduciendo errores manuales.

### **Despliegue de la Landing Page**
- **Carga de Archivos:** Se transfirieron los archivos y recursos necesarios al servidor de hosting.  
- **Verificación:** Se realizaron pruebas de funcionamiento para garantizar que la landing page se desplegara correctamente y estuviera accesible en la web.


**Deploy del Landing Page**
![deploy](../images/chapter-IV/Deploy%20Landing.PNG)
<br>

![deploy](../images/chapter-IV/Deployment_Landing-Github.png)
**Capturas de Pantalla**

- Repositorio de Landing Page:
  ![alt text](../images/chapter-IV/Repo%20Landingpage.PNG)

**Enlace al Repositorio**: https://github.com/1ACC0238-2520-1821-G2-Flota365/Flota365-Landing-Page

**Link deploy Landing Page:** https://1acc0238-2520-1821-g2-flota365.github.io/Flota365-Landing-Page/

#### 4.2.1.8. Team Collaboration Insights during Sprint

En esta sección se muestra un análisis detallado del trabajo colaborativo realizado por el equipo durante el Sprint. Las actividades se gestionaron bajo una metodología ágil, lo que facilitó una comunicación constante y una coordinación eficiente entre los integrantes. Se presentan además capturas de los analíticos de colaboración y de los commits en GitHub, que reflejan las aportaciones individuales de cada miembro.

---

### **Diseño y Desarrollo**

- **Frontend:** Desarrollo integral de la landing page, abarcando la creación de secciones, aplicación de estilos y adaptación responsive para distintos dispositivos.  
- **Backend:** Implementación de funcionalidades esenciales junto con la configuración inicial del servidor y los servicios requeridos.  
- **Codificación:** Ejecución de tareas de programación, pruebas funcionales y mejoras iterativas durante el proceso de desarrollo.  

---

### **Documentación y Despliegue**

- **Documentación:** Elaboración de documentación técnica y visual con descripciones detalladas y evidencias gráficas del proceso.  
- **Despliegue:** Configuración y puesta en marcha del entorno de pruebas, asegurando el funcionamiento integrado del frontend y backend.  

**Landing Page**

![Commits](../images/chapter-IV/LandingTrab%20Evi.PNG)

**Report:**

## 4.3. Validation Interviews

Para validar nuestros entregables, realizaremos entrevistas con nuestros segmentos objetivos, los cuales vienen a ser: Gestores de Flota y Conductores de vehículos pesados. El propósito es recopilar su opinión sobre la utilidad, claridad y facilidad de uso de solución propuesta por el team Flota365.

Las preguntas se plantearán de forma cercana pero estructurada, buscando obtener un feedback honesto sobre aspectos como la navegación, el diseño, la funcionalidad y el valor percibido en su trabajo diario.

Es por ello que, a continuación, se detallarán las preguntas y los principales hallazgos obtenidos a partir de sus respuestas.

### 4.3.1. Diseño de Entrevistas

Para validar nuestros entregables (Landing Page y aplicación web), realizaremos entrevistas con nuestros segmentos objetivos, los cuales vienen a ser: *Gestores de Flota* y *Conductores de vehículos pesados*. El propósito es recopilar su opinión sobre la utilidad, claridad y facilidad de uso de solución propuesta por el team **VSC Visionaries**.

Las preguntas se plantearán de forma cercana pero estructurada, buscando obtener un *feedback* honesto sobre aspectos como la navegación, el diseño, la funcionalidad y el valor percibido en su trabajo diario.

Es por ello que, a continuación, se detallarán las preguntas y los principales hallazgos obtenidos a partir de sus respuestas.

<h4 id="interviewsDesingValidation">5.3.1. Diseño de Entrevistas</h4>

**Preguntas generales**:

1. ¿Qué fue lo primero que pensaste al ver la página/aplicación?

2. ¿Sientes que está claro de qué trata la herramienta? ¿Qué entendiste que hace?

3. ¿Encontraste algo confuso o que te hizo dudar? ¿Cuál parte?

4. ¿Te parece fácil de navegar? ¿Por qué sí o por qué no?

5. Si tuvieras que explicarle esta plataforma a un compañero, ¿cómo lo harías?

6. ¿Sientes que esta herramienta realmente te ayudaría en tu día a día? ¿Por qué?

7. ¿Qué te pareció el diseño visual? ¿Muy cargado, muy vacío o bien balanceado?

8. ¿Notas algo que falte o que crees que sería útil agregar?


**Preguntas para el segmento #1 - Gestores de Flota**:

1. ¿Cómo te fue registrando tus recorridos o actividades en la app? ¿Te pareció sencillo o algo complicado?

2. ¿Te sentiste cómodo tomando y subiendo una foto del kilometraje? ¿Te pareció rápido?

3. ¿Hay algo que te gustaría que la app hiciera automáticamente por ti (por ejemplo, registrar el kilometraje sin tener que escribir)?

4. ¿Cuánto tiempo te tomaría usar la app al terminar un recorrido? ¿Crees que ese tiempo está bien o debería ser menor?

5. ¿Te parece clara la forma en que se guardan o muestran tus registros?

**Preguntas para el segmento #2 - Conductores de vehículos Pesados**:

1. ¿Pudiste encontrar fácilmente los datos que buscabas (por placa, fecha, etc.)?

2. ¿Qué tan útil te parece el sistema de reportes en PDF o Excel? ¿Lo usarías frecuentemente?

3. ¿Te gustaría que los reportes fueran más visuales (gráficos, alertas, etc.)?

4. ¿Cómo compararías esta herramienta con lo que usas actualmente para llevar el control de tu flota?

5. ¿Sientes que tienes el control y visibilidad necesarios desde esta aplicación?

6. ¿Agregarías algún tipo de alerta o recordatorio automático? ¿De qué tipo?

7. ¿El flujo de filtros y búsqueda se siente natural o hubo pasos innecesarios?

**Cierre - Opinión Final**:

- ¿Te gustaría participar en futuras mejoras como tester o dando sugerencias?

### 4.3.2. Registro de Entrevistas
### 4.3.3. Evaluaciones según heurísticas
