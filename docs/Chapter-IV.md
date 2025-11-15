# 4. Product Implementation & Validation

## 4.1. Software Configuration Management

La gestión de la configuración del software es fundamental para nuestro trabajo, ya que nos ayuda a controlar de manera exacta los componentes de nuestro proyecto, como el código fuente, los documentos de diseño y los recursos digitales. De esta manera, aseguramos que todos los miembros del equipo utilicen la misma versión de los archivos, lo que facilita la cooperación entre desarrolladores, diseñadores y otros profesionales involucrados.

<br>

### 4.1.1. Software Development Environment Configuration

### Project Management

  * ### Meet

    Una herramienta de videoconferencias que posibilita la comunicación en tiempo real del grupo para reuniones de coordinación.
  
    *Imagen de evidencia de uso*
  
    ![alt text](../images/chapter-IV/GoogleMeet.png)

    <br>

    ![alt text](../images/chapter-IV/MeetEvidence.png)
  
  <br>

  * ### Requirement Management

    * ### Draw.io
    Se trata de una suite de herramientas que posibilita la creación colaborativa de modelos C4 para representar de forma gráfica nuestros productos.
    
    *Imagen de evidencia de uso*
  
    ![alt text](../images/chapter-IV/Draw.io.tool.png)

    <br>
  
  * ### Product UX/UI Design

    * ### Figma

    Herramienta visual que facilita la creación de wireframes y mockups.
  
    *Imagen de evidencia de uso*
  
    ![alt text](../images/chapter-IV/Figma%20EVI.PNG)

    <br>
  
  * ### Software Development

    * ### HTML5

    Lenguaje de etiquetado orientado a crear páginas web.
  
    *Imagen de evidencia de uso*
  
    ![alt text](../images/chapter-IV/HTML%20EVI.PNG)
  
    <br>

    * ### CSS

    Lenguaje de diseño gráfico utilizado para dar formato al código escrito en HTML.
  
    *Imagen de evidencia de uso*
  
    ![alt text](../images/chapter-IV/CSS%20EVI.PNG)
  
    <br>

    * ### Javascript

    Lenguaje de programación orientado a objetos dinámico que utilizamos para implementar funcionalidades en un documento HTML.
  
    *Imagen de evidencia de uso*
  
    ![alt text](../images/chapter-IV/JS%20EVI.PNG)

   <br>
  
  * ### Software Documentation

    * ### Github

    Plataforma utilizada para el alojamiento de versiones del código fuente de un proyecto. Es una herramienta ampliamente popular en el trabajo colaborativo de programadores.  

    ![alt text](../images/chapter-IV/Github%20EVI.PNG)
  
  <br>

  * ### Software Documentation

    * ### Github Pages

    Una plataforma que posibilita la realización de despliegues simples directamente desde un repositorio de GitHub.  

    ![alt text](../images/chapter-IV/githubpagess.png)
    
  <br>

### 4.1.2. Source Code Management

* **Gitflow Implementation:**

Implementamos el flujo de trabajo gitflow para el control de versiones con branches(ramas) para trabajar paralelamente.

![alt text](../images/chapter-IV/Gitflow%20EVI.PNG)  

* **Master o Main branch:**

La rama principal de desarrollo del proyecto es la Master branch. En esta rama reside el código que actualmente se encuentra en producción.

#### Notación: master o main

* **Conventional Commits:**

"Conventional Commits" es una convención para estructurar los mensajes de confirmación (commits) en un formato estándar y semántico. Este formato ayuda a comunicar claramente los cambios realizados en el código y facilita la generación de registros de cambios automáticos. Los "Conventional Commits" suelen seguir un formato que incluye un encabezado, un cuerpo opcional y un pie de página opcional, y se utilizan para describir de manera sucinta y clara los cambios realizados en el código, lo que facilita su seguimiento y comprensión por parte de los desarrolladores y otros miembros del equipo.

<br>

La estructura de un commit debe seguir las siguientes pautas:

~~~
git commit -m “<type>[optional scope]: <title>“ -m “<description”
~~~

<br>

**Tipos De Conventional Commits**

~~~
1. feat: Used to describe a new feature or functionality added to the code.
2. fix: Indicates a bug fix or solution to a problem.
3. docs: Employed for changes or improvements in code documentation.
4. style: Describes changes related to the code's formatting, such as whitespace, indentation, etc., that do not affect its functionality.
5. refactor: Used for modifications to the code that do not fix bugs or add new features, but rather improve its structure or readability.
6. test: Indicates the addition or modification of unit tests or functional tests.
7. chore: Used for changes in the build process or maintenance tasks that are not directly related to the code itself.
8. perf: Describes performance improvements in the code.
~~~

<br>

### 4.1.3. Source Code Style Guide & Conventions

- ### HTML 

    - #### Use Lowercase Element Names:

        Es recomendable utilizar minúsculas o lowercase para los nombres de los elementos HTML.

        ~~~ 
      <body>
            <p>This is a paragraph</p>
      <body>
       ~~~

    <br>

    - #### Close All HTML Elements:

        Es recomendable cerrar todos los elementos HTML correctamente.

        ~~~ 
      <body>
            <p>This is a paragraph</p>
            <p>This is another paragraph</p>
      <body>
       ~~~

    <br>

    - #### Use Lowercase Attribute Names:

        Es recomendable utilizar minúsculas para los nombres de los atributos HTML.

      ~~~ 
      <a href="https://www.w3schools.com/html/">Visit our HTMLtutorial</a>
      ~~~

      <br>

    - #### Always Specify alt, width, and height for Images:

      Es recomendable seguir estas convenciones en caso de que la imagen no se pueda mostrar, lo que ayuda a mejorar la accesibilidad del contenido.

      ~~~ 
      <img src="html5.gif" alt="HTML5" 
      style="width:128px;height:128px">
      ~~~ 

      <br>

    - #### Spaces and Equal Signs:

      Se recomienda no utilizar espacios en blanco entre las entidades para mejorar la legibilidad.

      ~~~ 
      <link rel="stylesheet" href="styles.css">
      ~~~ 

      <br>

- ### CSS

    - #### ID and Class Naming

      Es recomendable utilizar nombres de clases e id's significativos que expresen claramente el propósito del elemento.

      ~~~ 
      #gallery {}
      #login {}
      .video {}
      ~~~

      <br>

    - #### ID and Class Name Style

      Se recomienda utilizar nombres cortos para nombrar ids o clases, pero lo suficientemente descriptivos para entender su propósito.

      ~~~ 
      #nav {}
      .author {}
      ~~~

      <br>

    - #### Shorthand Properties
    
      Se recomienda utilizar propiedades CSS de forma abreviada siempre que sea posible para hacer el código más eficiente y comprensible.

       ~~~ 
       border-top: 0;
       font: 100%/1.6 palatino, georgia, serif;
       padding: 0 1em 2em;
       ~~~

       <br>

    - #### 0 and Units

      Es recomendable evitar especificar la unidad después del valor 0 en propiedades que lo permitan, ya que esto ayuda a reducir el tamaño del código y mejora su legibilidad.

       ~~~ 
       margin: 0;
       padding: 0;
       ~~~

      <br>

     - #### Declaration Order

       Se recomienda ordenar las declaraciones en orden alfabético para facilitar el mantenimiento y la recordación del código.

       ~~~ 
        background: fuchsia;
        border: 1px solid;
        border-radius: 4px;
        color: black;
        text-align: center;
        text-indent: 2em;
       ~~~

       <br>

- ### JavaScript

     - #### Use expanded syntax

       Cada línea de JavaScript debería estar en una nueva línea, con la llave de apertura en la misma línea de su declaración y la llave de cierre en una nueva línea al final.

       ~~~ 
       function myFunc() {
        console.log('Hello!');
       };
       ~~~

       <br>

     - #### Variable naming

       Para el nombre de las variables, se recomienda utilizar lowerCamelCase. 

       ~~~ 
       let playerScore = 0;
       let speed = distance / time;
       ~~~

       <br>

     - #### Declaring variables

       Para la declaración de variables, es recomendable utilizar las palabras reservadas let y const en lugar de var.

       ~~~ 
       const myName = 'Chris';
       console.log(myName);
       let myAge = '40';
       myAge++;
       console.log('Happy birthday!');
       ~~~

       <br>

     - #### Function naming

       Para el nombre de las funciones, se recomienda utilizar lowerCamelCase.

       ~~~ 
       function sayHello() {
       alert('Hello!');
       };
       ~~~

       <br>

- ### Lenguaje Gherkin

    - #### Descriptive and concise titles for scenarios

      Utilizar títulos descriptivos y concisos para los escenarios.

      ~~~ 
      Feature: Login
        Scenario: Successful login
          Given a user is on the login page     
          When they enter valid credentials     
          Then they should be logged in successfully      
      ~~~

      <br>

    - #### Follow the Given-When-Then structure consistently.

      Seguir la estructura de Given-When-Then de manera consistente.

      ~~~ 
      Scenario: Adding items to the shopping cart
        Given the user is on the shopping page
        When they add an item to the cart
        Then the item should appear in the cart 
      ~~~

      <br>

    - #### Focus on business-readable language

      Centrarse en un lenguaje legible para el negocio, evitando detalles técnicos de implementación.

      ~~~ 
      Scenario: Changing user settingst
        Given the user is logged in
        When they navigate to the settings page
        Then they should be able to update their profile
      ~~~

      <br>

    - ####  Utilize Scenario Outline for scenarios with multiple similar cases.

      Utilizar Scenario Outline para escenarios con múltiples casos similares.

      ~~~ 
      Scenario Outline: Searching for products
        Given the user is on the search page
        When they search for "<product>"
        Then they should see search results for "<product>"
      
      Examples:
        | product  |
        | Laptop   |
        | Smartphone |
      ~~~

      <br>

    - #### Add comments to provide additional context

      Agregar comentarios para proporcionar contexto adicional o explicaciones cuando sea necesario.

      ~~~ 
      # This scenario checks the functionality of the logout feature
      Scenario: User logout
        Given the user is logged in
        When they click on the logout button
        Then they should be redirected to the login page      
      ~~~

      <br>

### 4.1.4. Software Deployment Configuration

En esta sección encontramos el detalle de como será el proceso de configuración de despliegue de las soluciones propuestas por Flota365. Cada una cuenta con herramientas que, por familiaridad del equipo, utilizará para dar mayor agilidad en proudcción y que nuestros usuarios lo puedan estar utilizando lo más pronto posible en sus actividades rutinarias.

A continuación comenzaremos por:

* **Landing Page:**

El landing page se desplegará como una página web estática, haciendo uso de <a href="https://docs.github.com/es/pages">Github Pages</a>. Este producto de **Github** permite alojar aplicaciones web estáticas de forma sencilla y escalable, proporcionando un entorno escalable para el Landing Page de Flota365.

<br>

**Proceso de Despliegue:**

1. En primer lugar, nos dirijimos a nuestro repostorio donde tenemos alojado nuestro *landing page* y procedemos a seleccionar la opción *Settings* de nuestro repositorio de Github.

<br>

![Settings](../images/chapter-IV/Settings_Github.png)

<br>

2. Dentro de dicho apartado, en el menú de la barra lateral procederemos a buscar la opción que tenga el nombre de *Pages*.

<br>

![Pages-option](../images/chapter-IV/Pages-Section_Github.png)

<br>

3. En el subtítulo que tenga el nombre de **Build and deployment**, en la parte de *branch*, seleccionaremos la rama que queremos desplegar nuestra solución - como nosotros usamos *conventional commits* y *conventional branches*, usamos la rama **main** como rama de despliegue a producción.
Adicional, seleccionamos a partir de que nivel de carpetas queremos que comience a monitorear Github nuestro proyecto que utilizará en el despliegue.

<br>

![brach-selected](../images/chapter-IV/Main-Branch-Selected_Github.png)

<br>

![Deployment-option](../images/chapter-IV/Deployment_Landing-Github.png)

<br>

4. Finalmente, esperamos a que nuestra configuración sea procesada y nos brinde un enlace como este:

<br>

![Final-deployment-result](../images/chapter-IV/Final-Step-to-Deploy-Github.png)

<br>

Con todos estos pasos, el despliegue de nuestra solución estará en cuestión de minutos y con la posiblidad de seguir escalando con más herramientas o servicios que nuestros amigos de **Github** tienen por ofrecernos.

<br>

## 4.2. Landing Page & Mobile Application Implementation

El desarrollo, testeo y despliegue de nuestra landing page es importante para que nuestros clientes puedan acceder a la información sobre nuestra empresa y producto a través de una interfaz con diseño responsivo, navegación intuitiva y solo con información relevante. Esta primera etapa nos permite crear un diseño conceptual sobre la estética que nuestra aplicación completa y lista para su uso. Estas etapas nos ayudaran a dar una primera impresión a los clientes para validar ideas e identificar problemas que se deben solucionar.  

<br>

### 4.2.1. Sprint 1

El primer sprint es una etapa importante en nuestro marco de gestión de proyectos de metodología ágil Scrum. En este periodo, agendamos reuniones con el objetivo de conocer mejor las características de cada integrante, y delegamos tareas para materializar el diseño y funcionalidades ya establecidas, para transformarlos en un landing page funcional y que cumple las heurísticas.  

<br>

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

<br>

#### 4.2.1.2. Sprint Backlog 1

Durante el primer sprint backlog, reunimos las historias de usuario relacionadas con la página de inicio (landing page). Para facilitar su gestión y organización, las dividimos en tareas más simples y las asignamos a los integrantes del equipo de manera eficiente, utilizando la herramienta Trello. Nuestro enfoque principal fue completar estas historias de usuario en el sprint, con el propósito de desarrollar una landing page funcional, atractiva y fácil de navegar. Además, trabajamos en la elaboración del informe de entrega y en el desarrollo del front-end y back-end de los bounded context **IAM** y **Applications**. Gracias al uso de Trello, logramos una colaboración efectiva y un seguimiento claro del avance de las tareas, lo que nos permitió resolver los desafíos que surgieron durante el proceso.

<br>

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

<br>

**Link de Trello**: https://trello.com/invite/b/68e3edd7fb5340b5154772f4/ATTI2ddb91b7af2a322ff81b700ac8f837b3DF4CD98A/sprint-1-flota365

<br>

#### 4.2.1.3. Development Evidence for Sprint Review

**Landing Page**:

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

<br>

**BackEnd**:

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

<br>

#### 4.2.1.4. Testing Suite Evidence for Sprint Review

Evidencia de prueba unitaria al Flota365-API

![unit](../images/chapter-IV/UnitTest.png)

<br>

#### 4.2.1.5. Execution Evidence for Sprint Review

En este Sprint, los miembros del equipo de desarrollo de software de Flota365 han completado y desplegado la Landing Page. A continuación, mostramos imágenes que demuestran cómo nuestra página presenta de manera clara e intuitiva la información sobre nuestro producto y nuestra empresa.

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

<br>

**Backend - Swagger:**

![alt text](../images/chapter-IV/Swagger1.PNG)
![alt text](../images/chapter-IV/Swagger2.PNG)
![alt text](../images/chapter-IV/Swagger3.PNG)

<br>

**Frontend - AndroidStudio:**  

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

<br>

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

<br>

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

<br>

#### 4.2.1.7. Software Deployment Evidence for Sprint Review

**Resumen**

Durante este Sprint, el equipo se centró en la implementación y despliegue de la landing page. Las tareas incluyeron la preparación del entorno, la configuración de recursos y la publicación inicial del sitio web. A continuación, se detalla el proceso seguido para completar el despliegue de la landing page.

<br>

## **Actividades Realizadas**

### **Creación de Cuentas y Configuración de Recursos**
- **Proveedor de Hosting:** Se seleccionó y configuró el servicio de hosting encargado de alojar la landing page.  
- **Entorno de Trabajo:** Se establecieron los entornos de desarrollo y producción para facilitar las pruebas y futuras actualizaciones.

<br>

### **Configuración de Proyectos para Integración**
- **Repositorio de Código:** Se configuró un repositorio en GitHub para gestionar versiones e integrar procesos de despliegue continuo.  
- **Automatización:** Se implementaron scripts y herramientas que permiten automatizar el proceso de despliegue, reduciendo errores manuales.

<br>

### **Despliegue de la Landing Page**
- **Carga de Archivos:** Se transfirieron los archivos y recursos necesarios al servidor de hosting.  
- **Verificación:** Se realizaron pruebas de funcionamiento para garantizar que la landing page se desplegara correctamente y estuviera accesible en la web.

<br>

**Deploy del Landing Page**

![deploy](../images/chapter-IV/Deploy%20Landing.PNG)

<br>

![deploy](../images/chapter-IV/Deployment_Landing-Github.png)

<br>

**Capturas de Pantalla**

- Repositorio de Landing Page:
  ![alt text](../images/chapter-IV/Repo%20Landingpage.PNG)

<br>

**Enlace al Repositorio**: https://github.com/1ACC0238-2520-1821-G2-Flota365/Flota365-Landing-Page

**Link deploy Landing Page:** https://1acc0238-2520-1821-g2-flota365.github.io/Flota365-Landing-Page/

<br>

#### 4.2.1.8. Team Collaboration Insights during Sprint #1

En esta sección se muestra un análisis detallado del trabajo colaborativo realizado por el equipo durante el Sprint. Las actividades se gestionaron bajo una metodología ágil, lo que facilitó una comunicación constante y una coordinación eficiente entre los integrantes. Se presentan además capturas de los analíticos de colaboración y de los commits en GitHub, que reflejan las aportaciones individuales de cada miembro.

<br>

### **Diseño y Desarrollo**

- **Frontend:** Desarrollo integral de la landing page, abarcando la creación de secciones, aplicación de estilos y adaptación responsive para distintos dispositivos.  

- **Backend:** Implementación de funcionalidades esenciales junto con la configuración inicial del servidor y los servicios requeridos.  

- **Codificación:** Ejecución de tareas de programación, pruebas funcionales y mejoras iterativas durante el proceso de desarrollo.  

<br>

### **Documentación y Despliegue**

- **Documentación:** Elaboración de documentación técnica y visual con descripciones detalladas y evidencias gráficas del proceso.  

- **Despliegue:** Configuración y puesta en marcha del entorno de pruebas, asegurando el funcionamiento integrado del frontend y backend.

<br>

**Landing Page**

![Commits](../images/chapter-IV/LandingTrab%20Evi.PNG)

<br>

**Report:**

![Commits](../images/chapter-IV/reportCommits.jpeg)

<br>

**Backend**

![Commits](../images/chapter-IV/backendCommits.jpeg)

<br>

**Mobile App**

![Commits](../images/chapter-IV/mobileCommits.jpeg)

<br>

### 4.2.2. Sprint 2

En este sprint 2 continuamos con el desarrollo del proyecto dentro del marco ágil de Scrum. Esta etapa se centró en la **implementación completa de la aplicación móvil Android**, abarcando los dos segmentos principales del sistema: **Conductores** y **Gestores de Flota**. Durante este sprint también se avanzó en la construcción de la **aplicación Flutter**, específicamente la parte destinada al **segmento de Conductores**, garantizando su integración con los servicios ya disponibles.

Las actividades del sprint incluyeron la conexión directa con el **backend totalmente desplegado**, permitiendo realizar pruebas end-to-end sobre funcionalidades críticas. Asimismo, se desarrollaron interfaces, flujos de navegación y componentes interactivos que aseguraran una experiencia de uso fluida y coherente para cada segmento. El objetivo principal fue consolidar una aplicación operativa, conectada y funcional, capaz de soportar los procesos definidos para ambos perfiles de usuario.

### 4.2.2.1. Sprint Planning 2

Durante la planificación del sprint, se priorizaron las **user stories** asociadas al desarrollo de las funcionalidades Android para Conductores y Gestores de Flota, así como los componentes iniciales de la aplicación Flutter orientada a Conductores. Se definieron tareas técnicas relacionadas con la integración con el backend, la implementación de pantallas, controladores, servicios de comunicación y manejo de estados.

El equipo alineó esfuerzos y responsabilidades, garantizando que las actividades asignadas permitieran avanzar de manera consistente hacia la entrega de una aplicación móvil estable, conectada y adecuada a las necesidades de ambos segmentos del sistema. Además, se fomentó la colaboración continua para asegurar una comprensión compartida del alcance y los objetivos del sprint.

| Sprint # | Sprint 2 |
| -- | -- |
| **Sprint Planning Background** | |
| **Date** | 27/10/2025 |
| **Time** | 11:00 AM |
| **Location** | Google Meet (Reunión virtual) |
| **Prepared By** | Torres Apolinario, Giovany Smith |
| **Attendees (to planning meeting)** | Huamani Sánchez José Diego, Llerena Delgado Renzo Miguel, Villafuerte Tapia Renzo Alonso |
| **Sprint Goal & User Stories** | |
| **Sprint 2 Goal** | Mejorar los puntos de nivel de arquitectura C4 de la aplicación así como Desarrollar la aplicación Android completa para el segmento de Gestores de Flota, integrada al backend, y avanzar con el desarrollo de la app Flutter para el segmento Conductores. |
| **Sprint 2 Velocity** | 19 |
| **Sum of Story Points** | 19 |

<br>

#### 4.2.2.2. Sprint Backlog 2

El Spring Backlog 2 consolidó la evolución técnica y funcional del proyecto Flota365, enfocándose en la entrega de componentes clave para ambos segmentos de usuarios: gestores de flota y conductores. Durante esta iteración se priorizó la construcción y estabilización de las aplicaciones móviles, así como la finalización del Web Services que soporta la operación de todo el ecosistema.

En primer lugar, se desarrolló la versión actualizada de la aplicación móvil para gestores de flota, construida en Kotlin, incorporando mejoras significativas en la interfaz, navegación y usabilidad. Esta versión integró principios de UX y optimizó los flujos esenciales como asignación de vehículos, monitoreo de rutas y visualización de incidencias.

Paralelamente, se implementó la primera versión funcional de la aplicación Flutter orientada al segmento de conductores. Esta entrega incluyó las capacidades de check-in, check-out, registro de incidencias y visualización del vehículo asignado, asegurando un flujo operativo eficiente desde dispositivos móviles.

De manera complementaria, se completó el 100% del Web Services, desarrollado en C# bajo .NET 8, utilizando una arquitectura monolito modular basada en Clean Architecture y Domain-Driven Design. Esta versión final estableció los módulos, entidades y servicios necesarios para garantizar la comunicación confiable entre aplicaciones y la centralización de la lógica de negocio.

Finalmente, el sprint incluyó la corrección de observaciones del entregable anterior, así como actividades de validación con usuarios reales mediante entrevistas, pruebas de usabilidad y revisión de los flujos implementados. Esto permitió ajustar funcionalidades y asegurar que la solución responda adecuadamente a los requisitos del dominio logístico.

<br>

![alt text](../images/chapter-IV/Scrum%20Board%20-%20Sprint%202%20-%20Flota365.png) 

| Sprint # | Sprint 2 |
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
| US14 | Información del vehículo | TA011 | Módulo de detalles del vehículo | Crear una vista con los datos completos del vehículo: modelo, placa, estado y revisiones. | 3 | Renzo Alonso Villafuerte Tapia ME | Done |

<br>

**Link de Trello**: https://trello.com/invite/b/69177f6ba3ab36f73ee521a5/ATTId55d067d884ae22ef95d41c56da1386c70D00649/sprint-2-flota365

<br>

#### 4.2.2.3. Development Evidence for Sprint Review

**Mobile Application - Kotlin**:

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

<br>

**Mobile Application - Flutter**:

|Repository |Branch| Commit Id | Commit Message| Commit Message Body| Date|
|----|-----|---------------------|----------------------------------------|---------------------------------------------------------|------------|
|Flota365-mobile-application-flutter|feature/conductores| 95e004b           | feat(driver): update page  | feat(driver): update page | 14/11/2025 |
|Flota365-mobile-application-flutter|feature/conductores| 998f339           | Merge branch 'feature/conductores' of https://github.com/1ACC0238-2520-1821-G2-Flota365/Flota365-mobile-application-flutter into feature/conductores
         | merge feat/conductores | 14/11/2025 |
|Flota365-mobile-application-flutter|feature/conductores| a406749           | feat(login): update register  | feat(login): update register         | 14/11/2025 |
|Flota365-mobile-application-flutter|feature/conductores| 97128e9           | feat(driver): update presentation    | feat(driver): update presentation       | 13/11/2025 |
|Flota365-mobile-application-flutter|feature/conductores| f32a5cf           | feat(driver): update data
 | feat(driver): update data | 13/11/2025 |
|Flota365-mobile-application-flutter|feature/conductores| ebd4def           | feat(driver): add driver_mapper     | feat(driver): add driver_mapper  | 13/11/2025 |
|Flota365-mobile-application-flutter|feature/conductores| bd0ffd3           | feat(dirver): update blocs route   | feat(dirver): update blocs route   | 12/11/2025 |
|Flota365-mobile-application-flutter|feature/conductores| c59ec8b           | feat(driver): add routes page | feat(driver): add routes page   | 12/11/2025 |
|Flota365-mobile-application-flutter|feature/conductores| 9377e53           | feat(conductores): update   | feat(conductores): update   | 11/11/2025 |

<br>

**Web Service**:

| **Repository** | **Branch**      | **Commit Id** | **Commit Message**                                                | **Commit Message Body**                                                                                                                                                                                                                                                                                          | **Date**      |
|----------------|-----------------|---------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|                                                                                         
| FlotaAPI       | main            | 6a85612       | **feat():** endpoint de métricas para Dashboard                    | Creación del endpoint `/api/dashboard/metrics` consolidando KPIs de Reporting: flotas, conductores, asignaciones, MTTR. Incluye cache en memoria de 60 segundos.                                                                                                                                                | 29/10/2025    |
| FlotaAPI       | main            | 648ccf6       | **refactor(Management):** separar contratos y servicios (CQRS)     | Reorganización del módulo Management bajo un enfoque CQRS ligero: separación de Commands/Queries, perfiles de AutoMapper y servicios por caso de uso. Mejora claridad, mantenimiento y testabilidad.                                                                                                            | 29/10/2025    |

<br>

#### 4.2.2.4. Testing Suite Evidence for Sprint Review

Para el presente entregable, el equipo ha tomado la decisión estratégica de priorizar la consolidación de la funcionalidad principal de la plataforma, sentando así una línea base estable para la validación final.

El esfuerzo de este Sprint se enfocó en los siguientes objetivos críticos:

1. Finalizar la versión funcional de la aplicación de Gestores (Kotlin), asegurando que el core del producto esté completo.

2. vistas y flujos esenciales.

3. Subsanar las observaciones de la documentación de la entrega anterior.

Debido a este enfoque centrado en la construcción y la corrección, la implementación formal de scripts de pruebas (testing) fue planificada para el siguiente ciclo.

**Próximos Pasos: Fase de Pruebas**

Habiendo alcanzado una versión funcionalmente estable, el último Sprint se dedicará de manera intensiva a la fase de Aseguramiento de Calidad (QA). Se ejecutará un plan de pruebas enfocado en:

* Validar la funcionalidad integral (end-to-end) de ambos productos.

* Identificar y corregir bugs de comportamiento.

* Revisar aspectos básicos de seguridad antes del despliegue final.

#### 4.2.2.5. Execution Evidence for Sprint Review

Para el logro de este proyecto, se realizó el despliegue tanto de la versión final de la aplicación móvil para el segmento de Gestores de Flota y se desarrolló la primera versión la aplicación móvil para el segmento de Coductores. Adicional a ello, se realizó las últimas mejoras para en su versión final el Web Service.

**Backend - Swagger:**

<a href="https://underground-tuesday-renworkplace-1e2821cb.koyeb.app/swagger/index.html">https://underground-tuesday-renworkplace-1e2821cb.koyeb.app/swagger/index.html</a>

![alt text](../images/chapter-IV/Swagger1.PNG)

<br>

![alt text](../images/chapter-IV/Swagger2.PNG) 

<br>

![alt text](../images/chapter-IV/Swagger3.PNG)

<br>

**Mobile Application - Kotlin:**

![alt text](../images/chapter-IV/Kotlin%20Execute1.jfif)

<br>

![alt text](../images/chapter-IV/Kotlin%20Execute2.jfif)

<br>

![alt text](../images/chapter-IV/Kotlin%20Execute3.jfif)

<br>

**Mobile Application - Flutter:**

![alt text](../images/chapter-IV/Flutter%20Login.jfif)

<br>

![alt text](../images/chapter-IV/Flutter%20Welcome.jfif)

<br>

![alt text](../images/chapter-IV/Flutter%20Menu.jfif)

<br>

![alt text](../images/chapter-IV/Flutter%20Routes.jfif)

<br>

#### 4.2.2.6. Services Documentation Evidence for Sprint Review

A continuación, se detalla el progreso del *Web Serivce*, presentando los endpoints que habilitan las nuevas funcionalidades desarrolladas en este Sprint.

Se incluye la validación de las operaciones CRUD (Crear, Leer, Actualizar, Borrar) mediante pruebas ejecutadas en la plataforma de **OpenAPI.** Adicionalmente, se adjunta el enlace de acceso al repositorio de la API en GitHub para la consulta del código fuente:" <a href="https://underground-tuesday-renworkplace-1e2821cb.koyeb.app/swagger/index.html">https://underground-tuesday-renworkplace-1e2821cb.koyeb.app/swagger/index.html</a>

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

<br>

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

<br>

#### 4.2.2.7. Software Deployment Evidence for Sprint Review

En esta entrega desplegamos la primera versión móvil dirigida a **gestores de flota** (Kotlin). El backend y la landing page ya estaban desplegados; la presente evidencia documenta el proceso de subida de la APK a **Firebase App Distribution** para distribución interna y pruebas.

**1. Acceso a Firebase:**

Accedí al Project Console de Firebase y verifiqué la pantalla de bienvenida del proyecto para confirmar que estoy trabajando sobre el proyecto correcto.

![Commits Web Services](../images/chapter-IV/Firebase%20Home%20-%20Deployment.jfif)

<br>

**2. Ir a App Distribution**

En el panel lateral de Firebase seleccioné "App Distribution" dentro de la sección de Release & Quality (o Distribución de apps según el idioma). Esta vista muestra las versiones publicadas y la opción para crear una nueva versión. (Insertar captura 2).

![Commits Web Services](../images/chapter-IV/Firebase%20App%20Distribution%20-%20Deployment.jfif)

<br>

**3. Generar APK desde Android Studio**

Abrí Android Studio y desde el menú Build → Generate Signed Bundle / APK inicié la construcción del artefacto. En el diálogo seleccioné APK (en lugar de Android App Bundle) y continué. (Insertar captura 3 mostrando el diálogo con la opción APK seleccionada).

![Commits Web Services](../images/chapter-IV/Generate%20APK%20File%20-%20Deployment.jfif)

<br>

![Commits Web Services](../images/chapter-IV/APK%20File%20Generated%20-%20Deployment.jfif)

* **Nota de seguridad:** la generación requiere el *keystore* y su contraseña; no incluí ningún valor secreto en las capturas. Asegúrate de difuminar/ocultar rutas o contraseñas si aparecen.

<br>

**4. Proveer KeyStore y credenciales de firma**

En el diálogo completé la ruta al KeyStore path, el KeyStore password, el key alias y su password. Confirmé y presioné Next para continuar con la firma y la generación del APK. (Insertar captura 4 que muestre el campo KeyStore path, con la ruta visible pero sin exponer contraseñas).

![Commits Web Services](../images/chapter-IV/Stablish%20secure%20key%20APK%20-%20Deployment.jfif)

* **Precaución:** nunca publicar contraseñas ni el contenido del keystore; si las capturas contienen datos sensibles, difuminarlos antes de añadirlas al informe.

<br>

**5. Selección de variante / branch y generación**

Elegí la variante de compilación release (o la variante que el equipo define para producción interna) y ejecuté la generación del APK. Verifiqué en la consola de Android Studio que la compilación finalizó correctamente y que el archivo .apk fue creado en la ruta de salida indicada. (Insertar captura 5 con la consola de Build mostrando BUILD SUCCESSFUL y la ruta del APK).

![Commits Web Services](../images/chapter-IV/Publish%20APK%20into%20a%20brach%20-%20Deployment.jfif)

<br>

**6. Subida a Firebase App Distribution**

Volví a Firebase → App Distribution y arrastré el archivo app-release.apk al área "Drag & drop APK to create new release". Completé el formulario de versión (versionName / versionCode y notas de release) y seleccioné los testers o los grupos de prueba. Inicié el proceso de publicación. (Insertar captura 6 del área de arrastre con el archivo ya cargado y la pantalla de metadata antes de publicar).

![Commits Web Services](../images/chapter-IV/Load%20APK%20File%20in%20Firebase%20-%20Deployment.jfif)

<br>

**7. Confirmación de publicación**

Una vez completada la subida, Firebase muestra un resumen de la versión publicada con su estado (por ejemplo, "Published" o "Ready") y los testers reciben la notificación. Capturé la pantalla final donde se evidencia la versión disponible y el historial de distribuciones.

<br>

#### 4.2.2.8. Team Collaboration Insights during Sprint

En este Sprint, el esfuerzo se ha centrado en la implementación simultánea de la Aplicación Móvil y el servicio Web (API) que la respalda.

Con el fin de medir y transparentar el progreso, el siguiente informe desglosa las métricas de colaboración del equipo (obtenidas de GitHub). Estos indicadores demuestran cómo la contribución individual de cada miembro se alinea con la distribución de tareas planificada, confirmando la ejecución efectiva del trabajo asignado en las distintas fases del desarrollo.

* **Web Services**

Resumen de la participación individual y la distribución del esfuerzo en el desarrollo de los Servicios Web. Estos datos muestran la contribución registrada por cada integrante para cumplir con los objetivos del Sprint.

![Commits Web Services](../images/chapter-IV/Web%20Service%20Insight%20-%20Report.png)

<br>

* **Landing Page**

A través de las métricas de colaboración de GitHub - basado en el desarrollo de nuestra *Landing Page*, ofrecemos una visión transparente del esfuerzo individual y colectivo; asegurando la rendición de cuentas (accountability) y confirmar que el trabajo se alinea con los objetivos estratégicos de la iteración.

![Commits Landing Page](../images/chapter-IV/Landing%20Page%20Insight%20-%20Report.png)

<br>

**Mobile App**

Detalle de la participación y el progreso aportado por cada miembro del equipo en el desarrollo de la Aplicación Móvil. Estos indicadores reflejan cómo se distribuyó la responsabilidad de construcción del frontend y la ejecución de las tareas asignadas a cada integrante.

**1. Kotlin:**

![Commits Kotlin Mobile App](../images/chapter-IV/Kotlin%20App%20Insight%20-%20Report.png)

<br>

**2. Flutter:**

![Commits Flutter Mobile App](../images/chapter-IV/Flutter%20App%20Insight%20-%20Report.png)

<br>

## 4.3. Validation Interviews

Para validar nuestros entregables, realizaremos entrevistas con nuestros segmentos objetivos, los cuales vienen a ser: Gestores de Flota y Conductores de vehículos pesados. El propósito es recopilar su opinión sobre la utilidad, claridad y facilidad de uso de solución propuesta por el team Flota365.

Las preguntas se plantearán de forma cercana pero estructurada, buscando obtener un feedback honesto sobre aspectos como la navegación, el diseño, la funcionalidad y el valor percibido en su trabajo diario.

Es por ello que, a continuación, se detallarán las preguntas y los principales hallazgos obtenidos a partir de sus respuestas.

<br>

### 4.3.1. Diseño de Entrevistas

**Segmento encontrado:**

- Gestores de flota

- Conductores de vehículos pesados

Antes de realizar las entrevistas, consideramos necesario realizar un análisis previo que nos permita entender mejor a nuestros públicos objetivo. Para ello, hemos diseñado una serie de preguntas específicas para cada segmento (gestores de flota y conductores de vehículos pesados), con el fin de orientar nuestras entrevistas de manera más eficiente y alineada a sus realidades operativas.

En particular, previo a entrevistar a nuestro segmento principal de gestores de flota, consideramos importante contar con un primer prototipo funcional de nuestra plataforma de gestión vehicular. Este prototipo será probado por usuarios reales de ambos segmentos, y en ese contexto proponemos una batería de preguntas cualitativas orientadas a observar el uso de la solución (registro de incidencias, seguimiento de mantenimientos, disponibilidad de datos para decisiones en tiempo real), identificar posibles puntos de fricción y validar nuestras suposiciones de diseño.

Las siguientes preguntas están organizadas según los dos segmentos clave del proyecto (gestores de flota y conductores) y nos permitirán recoger percepciones reales sobre la experiencia de uso inicial, facilitando así un proceso iterativo de mejora del producto, con foco en la reducción de tiempos muertos, la prevención de fallas y la optimización del control operativo de la flota.

<br>

## Segmento 1 — Gestores de flota (uso en app)

### 1) Primera impresión y registro
- ¿Cómo describirías tu experiencia inicial al abrir la app por primera vez?
- ¿El registro de tu perfil y de la empresa fue claro desde el teléfono? ¿Qué pasos te generaron dudas?
- ¿El tour inicial o ayudas en pantalla te orientaron para empezar?

<br>

### 2) Inicio de sesión y pantalla principal
- Al iniciar sesión, ¿qué fue lo primero que notaste del **tablero** (estado de flota, alertas, mantenimientos, incidencias)?
- ¿Identificaste rápido las **prioridades del día** (vehículos con alerta, mantenimientos próximos, incidencias abiertas)?
- ¿Qué mejorarías de la pantalla principal para tomar decisiones más rápido desde el móvil?

<br>

### 3) Navegación general
- ¿Pudiste moverte por la app sin ayuda? ¿En qué momento te perdiste o no supiste qué hacer?
- ¿Qué tan fácil fue encontrar **Reportes**, **Mantenimientos**, **Incidencias** y **Conductores**?
- ¿Localizaste el **tutorial** o **centro de ayuda** dentro del menú? ¿Fue útil?

<br>

### 4) Configuración de flota en app
- ¿Cómo te fue configurando **vehículos** (placa, odómetro, póliza/seguro, vencimientos) desde el teléfono?
- ¿Fue claro **asignar conductores** a vehículos y definir **umbrales** (km/días) para mantenimiento?
- ¿Qué datos pedirías menos/antes para hacerlo más rápido en móvil?

<br>

### 5) Alta de vehículos y confirmaciones
- ¿El flujo para **agregar/editar vehículos** fue evidente y confiable?
- ¿Los **mensajes de confirmación** (guardado, cambios, errores) son claros en app?
- ¿Necesitas ver una **bitácora de cambios** en móvil para confiar en el registro?

<br>

### 6) Usabilidad y percepción general
- ¿La app se percibe **rápida, fluida y estable**? ¿En qué momento se sintió lenta?
- ¿Qué funciones te resultaron más útiles en el día a día (alertas de mantenimiento, costos, incidencias, KPIs)?
- Si pudieras **reordenar** secciones o accesos rápidos, ¿qué pondrías primero?

<br>

### 7) Seguridad y confianza
- ¿Qué te haría sentir mayor seguridad en app (roles y permisos, 2FA, registros de auditoría)?
- ¿Qué nivel de detalle necesitas en **notificaciones** (p. ej., “mantenimiento programado”, “incidencia cerrada”)?

<br>

### 8) Interés y adopción futura
- ¿La app te ayudaría a **reducir tiempos muertos, costos de mantenimiento o siniestros**? ¿Por qué?
- ¿La recomendarías a otros gestores de tu organización? ¿Qué condiciones (precio, soporte, integraciones) serían clave?

<br>

## Segmento 2 — Conductores de vehículos pesados (app)

### 1) Primera impresión y registro
- ¿Cómo describirías tu experiencia inicial al abrir la app?
- ¿El registro y la **asignación del vehículo** fueron claros desde el teléfono?
- ¿El **tour** o ejemplos (fotos de referencia, campos sugeridos) te ayudaron a empezar?

<br>

### 2) Inicio de sesión y pantalla principal
- Al iniciar sesión, ¿pudiste identificar qué hacer primero (p. ej., **checklist preoperacional**, reporte de km, cargar combustible)?
- ¿Las **alertas del vehículo** (luces de check, vencimientos) se entienden de un vistazo?

<br>

### 3) Navegación general
- ¿Pudiste moverte sin ayuda? ¿En qué punto te perdiste?
- ¿Qué tan fácil fue encontrar el botón de **Reportar incidencia**, el **Historial** y el **tutorial**?

<br>

### 4) Formularios del conductor
- ¿Cómo te fue con los formularios de **checklist pre y post viaje**, **odómetro**, **fotos** y **comentarios**?
- ¿Qué campos te parecieron innecesarios o repetidos?
- ¿Qué evidencias (fotos, videos, audio) te gustaría adjuntar de forma más rápida?

<br>

### 5) Reporte de incidencias y comunicación
- ¿El flujo para **enviar una incidencia** fue claro y rápido?
- ¿La **confirmación** de envío te dio confianza (número de ticket, estado, tiempo estimado)?
- ¿Cuánto tiempo sueles perder contactando a tu jefe por un problema? ¿La app lo reduce?

<br>

### 6) Usabilidad y percepción general
- ¿La app se mantuvo **rápida y usable** durante la ruta (conectividad limitada, modo offline)?
- ¿Qué funciones fueron más útiles (alertas de mantenimiento, checklist guiado, mensajería, mapas, historial)?
- ¿Qué eliminarías o simplificarías?

<br>

### 7) Seguridad y confianza
- ¿Qué te haría sentir más seguro: **confirmaciones claras**, **contacto rápido con taller/soporte**, **botón SOS**?
- ¿Cómo te sientes con el **GPS** y el registro de datos del vehículo? ¿Qué transparencia esperas sobre su uso?

<br>

### 8) Interés y uso futuro
- Si la app mostrara **estado del vehículo**, **próximo mantenimiento** y **alertas** en tiempo real, ¿la usarías a diario? ¿Por qué?
- ¿La recomendarías a otros conductores? ¿Qué la haría **imprescindible** para ti?

<br>

### 4.3.2. Registro de Entrevistas

#### Segmento Objetivo 1: Gestores de flota

##### Entrevistado 1 Segmento Objetivo 1

| **Campo**                | **Detalle** |
|--------------------------|-------------|
| **Nombre**               | Ariana Ramirez|
| **Entrevistador**        | Renzo Miguel Llerena Delgado |
| **Edad**                 | 28 años |
| **Distrito**             | San Juan de Miraflores|
| **Resumen**              | A Ariana le parece que a nuestra aplicacion le faltaria añadir mas interfaz visual como para una aplicacion movil ya que algunas interfaces le parecen confusas y que sigamos desarrollando la funcion de rastreo de vehiculos por medio de gps |
| **Duración de la entrevista** | 08:22 minutos |
| **URL de la entrevista** | [Ver entrevista](https://drive.google.com/file/d/1wB30wOJnFaTQuDe239yptUSicUAx_fVO/view?usp=sharing) |


| **Campo**                | **Detalle** |
|--------------------------|-------------|
| **Nombre**               | Renato Calvo|
| **Entrevistador**        | Renzo Miguel Llerena Delgado |
| **Edad**                 | 25 años |
| **Distrito**             | San Isidro|
| **Resumen**              | A Renato le parece intuitiva la aplicación y recomendaría a sus compañeros, gestores de flota, su uso. Lo único que cree que se puede mejorar es el aspecto de reportes que le parece un poco desordenado el aspecto visual|
| **Duración de la entrevista** | 07:09 minutos |
| **URL de la entrevista** | [Ver entrevista](https://drive.google.com/file/d/1UhtyC9_bsUVF8azpNJjpUdbOfvqsse6R/view?usp=sharing) |

<br>

#### Segmento Objetivo 2: Conductores de vehículos pesados

##### Entrevistado 1 Segmento Objetivo 2

| **Campo**                | **Detalle** |
|--------------------------|-------------|
| **Nombre**               | Eduard Ancasi Carrión|
| **Entrevistador**        | Renzo Miguel Llerena Delgado |
| **Edad**                 | 28 años |
| **Distrito**             | San Juan de Miraflores|
| **Resumen**              | Eduard es conductor de vehículos pesados que trabaja en Shalon, le parece a el que nuestro avance necesita implementar la funcion de inteligencia artifical de forma completa, ya que el observa que eso sería un gran cambio con respecto a como podría trabajar el en su empresa, y que habría demasiada demanda si encuentran el servicio a un precio accesible para poder usarlo. Le parece que nuestra aplicacion movil necesita tener una estructura más organizada para facilitar el uso de gente inexperta con la tecnología y también implementando la funcionalidad de la ia|
| **Tiempo que empieza**   | 0:00 minutos |
| **Duración de la entrevista** | 08:30 minutos |
| **URL de la entrevista** | [Ver entrevista](https://drive.google.com/file/d/1lUyPkyNbrGfA9RZqERBFRNFBWAkkM0x7/view?usp=sharing) |

<br>

# Conclusiones

## Conclusiones y recomendaciones

* **TB1**:

Durante este sprint se desarrollaron actividades clave para comprender a profundidad el dominio del problema y definir las bases de la solución propuesta para Flota365. A través de entrevistas, análisis de escenarios, sesiones de EventStorming y elaboración de wireframes, logramos obtener una visión clara de las necesidades de los gestores de flota y conductores, así como de los procesos operativos que se deben optimizar.

Complementariamente, construimos los primeros elementos arquitectónicos del sistema, como los context maps y los diagramas estructurados de interacción, lo cual permitió establecer los límites funcionales, las dependencias y las responsabilidades de cada módulo dentro de la plataforma. Este trabajo colaborativo no solo consolidó un entendimiento compartido entre el equipo, sino que también sentó los cimientos para un diseño escalable, alineado al negocio y centrado en el usuario.

El proceso reforzó la importancia de combinar técnicas de análisis de dominio con prácticas de diseño orientadas a la experiencia del usuario, demostrando que una solución tecnológica efectiva requiere tanto claridad en los flujos operativos como una arquitectura bien definida.

* **TP1**:

En este segundo entregable se abordó un trabajo decisivo para consolidar la arquitectura conceptual y funcional de Flota365. Se revisaron y corrigieron elementos fundamentales del análisis inicial, incluyendo el EventStorming, la definición de los Bounded Contexts y la trazabilidad del flujo de dominio. Este proceso permitió depurar inconsistencias, reforzar el entendimiento del negocio y afinar los límites de responsabilidad de cada módulo, asegurando una visión más precisa y consistente de la solución.

Sobre esta base refinada, se inició la implementación de la primera versión de la aplicación dirigida al segmento de gestores de flota. Esta versión se centró en las funcionalidades core: visualización del dashboard operativo, seguimiento de rutas, gestión de vehículos, creación de nuevos conductores y asignación de unidades. Para garantizar un desarrollo escalable y mantenible, el equipo adoptó Clean Architecture como patrón arquitectónico, una elección adecuada para entornos mobile que requieren modularidad, separación de responsabilidades y capacidad de evolución en futuras iteraciones.

* **TB2**:

En esta tercera entrega se consolidaron avances clave que marcan un punto de inflexión en el desarrollo integral de Flota365. Se completó al 100% el backend del sistema, implementado como un Web Service monolito modular, sustentado en Clean Architecture y principios de Domain-Driven Design (DDD). Esta combinación permitió estructurar una API robusta, escalable y organizada en capas independientes, preservando la separación entre dominio, aplicación e infraestructura. Gracias a ello, el equipo pudo garantizar un backend extensible y preparado para futuros módulos sin comprometer su mantenibilidad.

Paralelamente, se desplegó la primera versión de la landing page oficial de Flota365, desarrollada con tecnologías web nativas (HTML5, CSS3 y JavaScript ES6). Este sitio proporciona una presentación moderna y clara del valor de la plataforma, actuando como punto de entrada para clientes potenciales y facilitando la difusión del producto.

En cuanto al desarrollo móvil, el equipo liberó la nueva versión del módulo para gestores de flota, implementado en Kotlin, ahora con una interfaz significativamente mejorada. Esta versión incorpora principios de UX centrados en la usabilidad y claridad operativa, optimizando la visualización del estado de la flota, la asignación de vehículos y la gestión operativa diaria.

Finalmente, se lanzó la primera versión de la aplicación para conductores, desarrollada con Flutter. Este componente introduce funcionalidades esenciales como check-in y check-out, permitiendo que los conductores registren el inicio y fin de sus operaciones, la unidad asignada y las incidencias ocurridas durante el trayecto. Estas capacidades no solo fortalecen la trazabilidad operacional, sino que también habilitan un canal de comunicación directa y confiable entre el conductor y el gestor de flota.

## Video App Validation

![App Validation Background Video](../images/chapter-IV/Video%20Validate%20App.png)

* **Enlace del video:** <a href="https://www.youtube.com/watch?v=w7eizS0Nv6w">https://www.youtube.com/watch?v=w7eizS0Nv6w</a>

## Video About the product

![About the product Background Video](../images/chapter-IV/Video%20About%20The%20Product.png)

* **Enlace del video:** <a href="https://youtu.be/PgJkLZSe23Q">https://www.youtube.com/watch?v=w7eizS0Nv6w</a>


## Video About the team

![About the team Background Video](../images/chapter-IV/Video%20About%20the%20Team.png)

* **Enlace del video:** <a href="https://youtu.be/4C5rVB0vVy0">https://youtu.be/4C5rVB0vVy0</a>

# Glosario

## Dominio de Negocio - Flota365

**1. Gestor de Flota**

- Responsable de administrar vehículos, conductores, rutas y documentación. Supervisa las operaciones y toma decisiones para mantener la flota en funcionamiento óptimo.

**2. Conductor**

- Usuario encargado de ejecutar los viajes asignados. Registra actividades, kilometraje, estados y evidencias durante cada operación.

**3. Asignación de Vehículo**

- Proceso mediante el cual un vehículo es asociado de forma temporal a un conductor para realizar un viaje u operación específica.

**4. Orden de Transporte**

- Documento digital que formaliza el inicio de una operación, definiendo conductor asignado, vehículo, punto de partida, destino y tipo de carga.

**5. Inicio de Operación**

- Momento en que el conductor inicia oficialmente su recorrido, activando la trazabilidad del viaje.

**6. Cierre de Operación**

- Registro final que marca el término del recorrido. Incluye kilometraje final, entrega realizada y observaciones.

**7. Disponibilidad del Conductor**

- Estado que indica si un conductor está apto para nuevas asignaciones. Considera tiempo de descanso, suspensiones y tareas en curso.

**8. Documentación Vigente**

- Documentación legal requerida para que un vehículo pueda operar (SOAT, revisión técnica, permisos). Su vigencia condiciona las operaciones.

<br>

## Arquitectura de Software y Servicios

**9. Backend**

- Conjunto de lógica de negocio, reglas, validaciones y acceso a datos. Se ejecuta en el servidor y expone funcionalidades mediante APIs o servicios.

**10. API (Application Programming Interface)**

- Interfaz que permite la comunicación entre sistemas. En Flota365 se usa para enviar y recibir información entre las apps móviles y el servidor.

**11. Web Service**

- Servicio accesible por la web que permite intercambiar datos. Puede ser REST, SOAP u otro formato.

- Un backend contiene la lógica y un web service es solo un punto de acceso.

**12. Arquitectura C4**

- Modelo de documentación arquitectónica que describe el sistema en cuatro niveles:
Contexto → Contenedores → Componentes → Código.

**13. Bounded Context**

- Subdominio delimitado que encapsula reglas, lenguaje y procesos propios. Permite organizar el sistema por áreas funcionales claras.

**14. Event Storming**

- Metodología visual para mapear eventos, comandos, actores, reglas y procesos del negocio de forma colaborativa.

<br>

## Diseño de Interfaces (UI/UX)

**15. UI (User Interface)**

- Componentes visuales de la interfaz: botones, formularios, colores, tipografías, diagramación, etc.

**16. UX (User Experience)**

- Percepción general del usuario respecto al uso del sistema: facilidad, fluidez, tiempo de tarea y satisfacción.

**17. Prototipo de Alta Fidelidad**

- Representación visual casi idéntica a la versión final de la aplicación. Simula flujos y pantallas completas antes del desarrollo.

**18. Landing Page**

- Página web de presentación o marketing centrada en comunicar un producto o captar leads.

- No es una aplicación web funcional.

**19. Web Application**

- Aplicación interactiva con funcionalidades, procesos internos y acceso autenticado. Es dinámica y responde a la lógica del servidor.

<br>

## Conceptos Técnicos y Patrones Comunes

**20. Arquitectura Cliente-Servidor**

- Modelo donde el cliente (app móvil o web) solicita información y el servidor la procesa y responde.

**21. JSON (JavaScript Object Notation)**

- Formato estándar para enviar datos entre cliente y servidor. Se utiliza en las APIs de Flota365.

**22. Integración Continua (CI/CD)**

- Práctica que automatiza pruebas, despliegues y compilación del sistema. Asegura entregas rápidas y confiables.

**23. Token / JWT (JSON Web Token)**

- Mecanismo de autenticación que confirma la identidad del usuario en las solicitudes a la API.

**24. Repository Pattern**

- Patrón usado para gestionar el acceso a datos, separando la lógica de consulta de la lógica de negocio.

<br>

# Bibliografía

- Refactoring.Guru. (s.f.). Design patterns. <a href="https://refactoring.guru/es/design-patterns">https://refactoring.guru/es/design-patterns</a>

- Gothelf, J., & Seiden, J. (2021). Lean UX: Designing great products with agile teams (3rd ed.). O’Reilly Media.

- Evans, E. (2004). Domain-driven design: Tackling complexity in the heart of software. Addison-Wesley.

- Vernon, V. (s.f.). Domain-driven design reference: Definitions and pattern summaries. <a href="https://domainlanguage.com/ddd/reference/">https://domainlanguage.com/ddd/reference/</a>

- Martin, R. C. (2017). Clean architecture: A craftsman's guide to software structure and design. Prentice Hall.

- The C4 model for visualising software architecture. (2024). <a href="https://c4model.com/">https://c4model.com/</a>