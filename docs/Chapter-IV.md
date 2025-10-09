# 4. Product Implementation & Validation

## 4.1. Software Configuration Management

La gestión de la configuración del software es fundamental para nuestro trabajo, ya que nos ayuda a controlar de manera exacta los componentes de nuestro proyecto, como el código fuente, los documentos de diseño y los recursos digitales. De esta manera, aseguramos que todos los miembros del equipo utilicen la misma versión de los archivos, lo que facilita la cooperación entre desarrolladores, diseñadores y otros profesionales involucrados.

### 4.1.1. Software Development Environment Configuration

### Project Management
  * ### Meet
    Una herramienta de videoconferencias que posibilita la comunicación en tiempo real del grupo para reuniones de coordinación.
  
    Imagen de evidencia de uso
  
    ![alt text](../images/chapter-IV/Meet.png)
  
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

* ### **Gitflow Implementation:**
Implementamos el flujo de trabajo gitflow para el control de versiones con branches(ramas) para trabajar paralelamente.

![alt text](../images/chapter-IV/Gitflow%20EVI.PNG)  

### **Master o Main branch**
La rama principal de desarrollo del proyecto es la Master branch. En esta rama reside el código que actualmente se encuentra en producción.
#### Notación: master o main

### **Conventional Commits**
"Conventional Commits" es una convención para estructurar los mensajes de confirmación (commits) en un formato estándar y semántico. Este formato ayuda a comunicar claramente los cambios realizados en el código y facilita la generación de registros de cambios automáticos. Los "Conventional Commits" suelen seguir un formato que incluye un encabezado, un cuerpo opcional y un pie de página opcional, y se utilizan para describir de manera sucinta y clara los cambios realizados en el código, lo que facilita su seguimiento y comprensión por parte de los desarrolladores y otros miembros del equipo.
<br>
La estructura de un commit debe seguir las siguientes pautas:
~~~
git commit -m “<type>[optional scope]: <title>“ -m “<description”
~~~
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

### 4.1.3. Source Code Style Guide & Conventions

- ### HTML 
    - #### Use Lowercase Element Names:
        Es recomendable utilizar minúsculas o lowercase para los nombres de los elementos HTML.
        ~~~ 
      <body>
            <p>This is a paragraph</p>
      <body>
       ~~~
    - #### Close All HTML Elements:
        Es recomendable cerrar todos los elementos HTML correctamente.
        ~~~ 
      <body>
            <p>This is a paragraph</p>
            <p>This is another paragraph</p>
      <body>
       ~~~
    - #### Use Lowercase Attribute Names:
        Es recomendable utilizar minúsculas para los nombres de los atributos HTML.
      ~~~ 
      <a href="https://www.w3schools.com/html/">Visit our HTMLtutorial</a>
       ~~~
    - #### Always Specify alt, width, and height for Images:
      Es recomendable seguir estas convenciones en caso de que la imagen no se pueda mostrar, lo que ayuda a mejorar la accesibilidad del contenido.
      ~~~ 
      <img src="html5.gif" alt="HTML5" 
      style="width:128px;height:128px">
      ~~~ 
    - #### Spaces and Equal Signs:
      Se recomienda no utilizar espacios en blanco entre las entidades para mejorar la legibilidad.
      ~~~ 
      <link rel="stylesheet" href="styles.css">
      ~~~ 
- ### CSS
    - #### ID and Class Naming
      Es recomendable utilizar nombres de clases e id's significativos que expresen claramente el propósito del elemento.
      ~~~ 
      #gallery {}
      #login {}
      .video {}
       ~~~
    - #### ID and Class Name Style
      Se recomienda utilizar nombres cortos para nombrar ids o clases, pero lo suficientemente descriptivos para entender su propósito.
      ~~~ 
      #nav {}
      .author {}
      ~~~
    - #### Shorthand Properties
      Se recomienda utilizar propiedades CSS de forma abreviada siempre que sea posible para hacer el código más eficiente y comprensible.
       ~~~ 
       border-top: 0;
       font: 100%/1.6 palatino, georgia, serif;
       padding: 0 1em 2em;
       ~~~ 
    - #### 0 and Units
      Es recomendable evitar especificar la unidad después del valor 0 en propiedades que lo permitan, ya que esto ayuda a reducir el tamaño del código y mejora su legibilidad.
       ~~~ 
       margin: 0;
       padding: 0;
       ~~~
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
- ### JAVASCRIPT
     - #### Use expanded syntax
       Cada línea de JavaScript debería estar en una nueva línea, con la llave de apertura en la misma línea de su declaración y la llave de cierre en una nueva línea al final.
       ~~~ 
       function myFunc() {
        console.log('Hello!');
       };
       ~~~
     - #### Variable naming
       Para el nombre de las variables, se recomienda utilizar lowerCamelCase. 
       ~~~ 
       let playerScore = 0;
       let speed = distance / time;
       ~~~  
     - #### Declaring variables
       Para la declaración de variables, es recomendable utilizar las palabras reservadas let y const en lugar de var.
       ~~~ 
       const myName = 'Chris';
       console.log(myName);
       let myAge = '40';
       myAge++;
       console.log('Happy birthday!');
       ~~~ 
     - #### Function naming
       Para el nombre de las funciones, se recomienda utilizar lowerCamelCase.
       ~~~ 
       function sayHello() {
       alert('Hello!');
       };
       ~~~
- ### LENGUAJE GHERKIN
    - #### Descriptive and concise titles for scenarios
      Utilizar títulos descriptivos y concisos para los escenarios.
      ~~~ 
      Feature: Login
        Scenario: Successful login
          Given a user is on the login page     
          When they enter valid credentials     
          Then they should be logged in successfully      
      ~~~
    - #### Follow the Given-When-Then structure consistently.
      Seguir la estructura de Given-When-Then de manera consistente.
      ~~~ 
      Scenario: Adding items to the shopping cart
        Given the user is on the shopping page
        When they add an item to the cart
        Then the item should appear in the cart 
      ~~~
    - #### Focus on business-readable language
      Centrarse en un lenguaje legible para el negocio, evitando detalles técnicos de implementación.
      ~~~ 
      Scenario: Changing user settingst
        Given the user is logged in
        When they navigate to the settings page
        Then they should be able to update their profile
      ~~~
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
    - #### Add comments to provide additional context
      Agregar comentarios para proporcionar contexto adicional o explicaciones cuando sea necesario.
      ~~~ 
      # This scenario checks the functionality of the logout feature
      Scenario: User logout
        Given the user is logged in
        When they click on the logout button
        Then they should be redirected to the login page      
      ~~~
      
### 4.1.4. Software Deployment Configuration

En esta sección encontramos el detalle de como será el proceso de configuración de despliegue de las soluciones propuestas por Flota365. Cada una cuenta con herramientas que, por familiaridad del equipo, utilizará para dar mayor agilidad en proudcción y que nuestros usuarios lo puedan estar utilizando lo más pronto posible en sus actividades rutinarias.

A continuación comenzaremos por:

**Landing Page**

El landing page se desplegará como una página web estática, haciendo uso de <a href="https://docs.github.com/es/pages">Github Pages</a>. Este producto de **Github** permite alojar aplicaciones web estáticas de forma sencilla y escalable, proporcionando un entorno escalable para el Landing Page de Flota365.

* Proceso de Despliegue:

1. En primer lugar, nos dirijimos a nuestro repostorio donde tenemos alojado nuestro *landing page* y procedemos a seleccionar la opción *Settings* de nuestro repositorio de Github.

![Settings](../images/chapter-IV/Settings_Github.png)

2. Dentro de dicho apartado, en el menú de la barra lateral procederemos a buscar la opción que tenga el nombre de *Pages*.

![Pages-option](../images/chapter-IV/Pages-Section_Github.png)

3. En el subtítulo que tenga el nombre de **Build and deployment**, en la parte de *branch*, seleccionaremos la rama que queremos desplegar nuestra solución - como nosotros usamos *conventional commits* y *conventional branches*, usamos la rama **main** como rama de despliegue a producción.
Adicional, seleccionamos a partir de que nivel de carpetas queremos que comience a monitorear Github nuestro proyecto que utilizará en el despliegue.

![brach-selected](../images/chapter-IV/Main-Branch-Selected_Github.png)

<br>

![Deployment-option](../images/chapter-IV/Deployment_Landing-Github.png)

4. Finalmente, esperamos a que nuestra configuración sea procesada y nos brinde un enlace como este:

![Final-deployment-result](../images/chapter-IV/Final-Step-to-Deploy-Github.png)

Con todos estos pasos, el despliegue de nuestra solución estará en cuestión de minutos y con la posiblidad de seguir escalando con más herramientas o servicios que nuestros amigos de **Github** tienen por ofrecernos.

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