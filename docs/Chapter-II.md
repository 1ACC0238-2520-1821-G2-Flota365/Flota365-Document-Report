# Capítulo 2: Requirements Development and Software Solution Design

## 2.1. Competidores
En esta sección se presenta la identificación y descripción de los principales competidores de Flota365, tanto directos como indirectos. Estos actores del mercado cuentan con propuestas basadas en productos digitales similares o con enfoques que abordan parcialmente el mismo problema que nuestra solución. La comparación busca evidenciar las características esenciales de cada alternativa y contextualizar el entorno competitivo en el que se desarrollará Flota365.

Se han identificado los siguientes competidores directos de Flota 365, todos con presencia en el mercado latinoamericano y con soluciones digitales para la gestión de flotas:


**- RDA Mobility**

Empresa con presencia en Argentina, Colombia y Uruguay, que ofrece soluciones de renting corporativo, gestión de flotas y telemetría vehicular.

**- Geotab**

Multinacional canadiense especializada en soluciones de telemática y software de gestión de flotas, con presencia en América Latina.

**- iLab Perú**

Empresa peruana que ofrece un sistema web de gestión de flotas, con funcionalidades orientadas al monitoreo y control de vehículos.

### 2.1.1. Análisis competitivo
El análisis competitivo tiene como finalidad profundizar en el conocimiento que tiene Flota365 sobre el resto de sus competidores. Para ello, se ha elaborado un *Competitive Analysis Landscape*, el cual organiza de manera estructurada los aspectos clave de cada actor analizado, incluyendo perfil general, estrategia de marketing, características del producto, precios y canales de distribución. Finalmente, se incorpora un análisis FODA que permite visualizar de forma clara las fortalezas, debilidades, oportunidades y amenazas, tanto propias como de los competidores. 
<br>
</br>

<table border="1" cellpadding="8" cellspacing="0" style="border-collapse:collapse; width:100%; font-family:Arial, sans-serif;">
    <tr>
        <th colspan="7">Competitive Analysis Landscape</th>
    </tr>
    <tr>
        <td colspan="2" rowspan="2"><strong>¿Por qué llevar a cabo este análisis?</strong></td>
        <td colspan="5">¿Cómo se posiciona Flota 365 frente a sus competidores en cuanto a propuesta de valor, marketing, producto y estrategia?</td>
    </tr>
    <tr>
        <td colspan="5">
            Es un análisis comparativo que permite identificar fortalezas, debilidades, oportunidades y amenazas, así como entender mejor la posición del producto frente a otros actores relevantes del mercado.
        </td>
    </tr>
    <tr>
        <td colspan="3"></td>
        <td style="text-align:center;">
            <strong>Flota 365</strong><br>
            <img src="../images/chapter-II/Flota365-Branding.jpg" alt="Flota 365 Logo" style="width:100px;">
        </td>
        <td style="text-align:center;">
            <strong>RDA Mobility</strong><br>
            <img src="../images/chapter-II/rdamobility-logo.jpg" alt="RDA Mobility Logo" style="width:100px;">
        </td>
        <td style="text-align:center;">
            <strong>Geotab</strong><br>
            <img src="../images/chapter-II/geotab-logo.png" alt="Geotab Logo" style="width:100px;">
        </td>
        <td style="text-align:center;">
            <strong>iLab Perú</strong><br>
            <img src="../images/chapter-II/ilabperu_logo.png" alt="iLab Perú Logo" style="width:100px;">
        </td>
    </tr>
    <tr>
        <td rowspan="2">Perfil</td>
        <td colspan="2">Overview</td>
        <td>Plataforma de gestión de flotas orientada a pymes del Perú, con interfaz moderna, fácil de usar, y soporte técnico local.</td>
        <td>Ofrece renting vehicular corporativo, acompañado de soluciones tecnológicas para gestión de flotas.</td>
        <td>Multinacional con soluciones avanzadas de telemetría y big data para flotas.</td>
        <td>Plataforma local con enfoque básico en control y seguimiento vehicular.</td>
    </tr>
    <tr>
        <td colspan="2">Ventaja competitiva ¿Qué valor ofrece a los clientes?</td>
        <td>Simplicidad + Personalización + Costo accesible + Soporte local.</td>
        <td>Integración con renting y oferta de movilidad.</td>
        <td>Tecnología robusta, alta precisión y escalabilidad.</td>
        <td>Precio bajo y atención directa al cliente local.</td>
    </tr>
    <tr>
        <td rowspan="2">Perfil de Marketing</td>
        <td colspan="2">Mercado objetivo</td>
        <td>PYMEs de transporte, distribución y logística en Perú y LATAM.</td>
        <td>Empresas grandes y medianas con flotas corporativas.</td>
        <td>Grandes flotas, operadores logísticos y gobiernos.</td>
        <td>Pequeñas empresas con bajo presupuesto.</td>
    </tr>
    <tr>
        <td colspan="2">Estrategias de marketing</td>
        <td>Marketing digital, redes sociales, ferias del sector, alianzas con operadores.</td>
        <td>Estrategias B2B con foco en acuerdos corporativos.</td>
        <td>Alianzas internacionales y promoción en eventos tech.</td>
        <td>Venta directa, recomendaciones boca a boca.</td>
    </tr>
    <tr>
        <td rowspan="3">Perfil de Producto</td>
        <td colspan="2">Productos & Servicios</td>
        <td>Software de gestión de flotas (web/móvil), alertas, reportes, mantenimiento, rastreo.</td>
        <td>Renting + software básico de gestión.</td>
        <td>Gestión de flotas con inteligencia artificial, reportes avanzados, APIs.</td>
        <td>Plataforma de rastreo y control simple.</td>
    </tr>
    <tr>
        <td colspan="2">Precios & Costos</td>
        <td>Planes mensuales escalables según funcionalidades.</td>
        <td>Costos integrados al renting vehicular.</td>
        <td>Alto costo de entrada y por dispositivos.</td>
        <td>Muy bajo costo.</td>
    </tr>
    <tr>
        <td colspan="2">Canales de distribución (Web y/o Móvil)</td>
        <td>Web y App móvil, venta directa y distribuidores locales.</td>
        <td>Venta corporativa (B2B) con equipo comercial.</td>
        <td>Venta en línea y red global de distribuidores.</td>
        <td>Sitio web básico y atención personalizada.</td>
    </tr>
    <tr>
        <td rowspan="5">Análisis SWOT</td>
    <tr>
        <td colspan="2">Fortalezas</td>
        <td>Facilidad de uso, atención local, buen soporte, precios competitivos.</td>
        <td>Modelo integrado (renting + software), movilidad sostenible.</td>
        <td>Tecnología de punta, experiencia internacional.</td>
        <td>Costos bajos, cercanía con el cliente.</td>
    </tr>
    <tr>
        <td colspan="2">Debilidades</td>
        <td>Menor reconocimiento de marca, falta de presencia internacional.</td>
        <td>Dependencia del renting como modelo de entrada.</td>
        <td>Requiere conocimientos técnicos y gran inversión.</td>
        <td>Tecnología limitada, poca innovación.</td>
    </tr>
    <tr>
        <td colspan="2">Oportunidades</td>
        <td>Digitalización del transporte en LATAM, alianzas estratégicas.</td>
        <td>Aumento de flotas corporativas sostenibles.</td>
        <td>Expansión a nuevos mercados LATAM.</td>
        <td>Demanda de soluciones económicas en provincias.</td>
    </tr>
    <tr>
        <td colspan="2">Amenazas</td>
        <td>Ingreso de competidores internacionales, barreras regulatorias.</td>
        <td>Nuevos modelos de propiedad compartida.</td>
        <td>Startups locales con soluciones más adaptadas.</td>
        <td>Baja escalabilidad frente a otras plataformas.</td>
    </tr>
</table>

### 2.1.2. Estrategias y tácticas frente a competidores
Tras un análisis detallado de los principales competidores de Flota365 —AFE Logistics, RDA Mobility, Geotab e iLab Perú— se han identificado oportunidades estratégicas clave para fortalecer nuestra propuesta de valor, diferenciarnos y consolidar nuestra posición en el mercado. Las siguientes estrategias se fundamentan en las fortalezas, debilidades y amenazas encontradas, con tácticas específicas orientadas a maximizar la eficiencia y satisfacción del cliente.

**1) Estrategias basadas en fortalezas**

**- Enfoque especializado en el sector agrícola y de transporte rural**

**Estrategia:** Diferenciar a Flota365 como una plataforma desarrollada especialmente para la gestión de flotas en el sector agrícola, a diferencia de competidores más generalistas como Geotab o AFE Logistics.

**Táctica:**

Comunicar de forma clara nuestro enfoque en soluciones adaptadas al campo y a las condiciones rurales: vehículos agrícolas, motocicletas, camionetas de campo, etc.

Crear contenido segmentado por tipo de cliente (cooperativas agrarias, productores independientes, etc.) que demuestre cómo Flota365 se adapta a sus necesidades reales.

Participar en ferias y eventos del sector agroindustrial para reforzar la identidad de marca especializada.

<br>

**- Ventaja competitiva por simplicidad y personalización**

**Estrategia:** Resaltar la facilidad de uso de Flota365 frente a soluciones robustas pero más complejas como Geotab o RDA Mobility.

**Táctica:**

Desarrollar una experiencia de usuario (UX) simple e intuitiva que permita la adopción rápida por parte de conductores y personal no técnico.

Ofrecer configuraciones personalizadas y planes modulares según el tamaño y necesidades de la empresa.

Brindar soporte técnico y capacitación remota como parte del onboarding, para facilitar el uso desde el primer día.

<br>

**- Generación de alertas inteligentes y mantenimiento preventivo**

**Estrategia:** Capitalizar la funcionalidad de alertas automáticas por mantenimiento y uso del vehículo, la cual no está priorizada en soluciones como iLab Perú.

**Táctica:**

Mostrar casos de éxito donde el mantenimiento preventivo ha evitado fallas y costos adicionales.

Generar reportes automatizados que alerten sobre mantenimientos próximos y condiciones críticas de la unidad.

Integrar dashboards con indicadores clave de salud vehicular, rutas y uso.

<br>

**2) Estrategias basadas en debilidades**

**- Fortalecimiento de la cobertura de datos y actualización**

**Estrategia:** Superar la posible debilidad en la actualización de datos e información en tiempo real al integrar mejores fuentes y automatización.

**Táctica:**

Integrar sensores IoT, GPS y otros dispositivos de rastreo con compatibilidad directa con Flota365.

Implementar procesos automáticos de sincronización de datos para eliminar el error humano.

Ofrecer herramientas que permitan a los usuarios reportar incidencias o inconsistencias fácilmente.

<br>

**- Ampliación de funcionalidades para transporte urbano e híbrido**

**Estrategia:** Reducir la limitación actual del enfoque agrícola expandiendo Flota365 a flotas urbanas, logísticas y mixtas.

**Táctica:**

Iniciar un piloto con empresas de transporte urbano o de última milla que también manejen vehículos ligeros.

Incorporar nuevas funciones como optimización de rutas en zonas urbanas, integración con apps de reparto, y reportes de consumo por trayecto.

Desarrollar una versión adaptable del sistema para flotas mixtas que combinen lo rural y lo urbano.

<br>

**- Competencia con soluciones de alto presupuesto (Geotab, AFE Logistics)**

**Estrategia:** Enfocar la estrategia comercial de Flota365 como una alternativa accesible y eficiente frente a plataformas de alto costo.

**Táctica:**

Resaltar la relación costo-beneficio de Flota365 frente a sistemas de gran escala que suelen tener costos elevados de implementación.

Ofrecer modelos de suscripción flexibles y precios competitivos por unidad o por usuario.

Aplicar campañas publicitarias dirigidas a empresas medianas que requieren soluciones funcionales sin sobredimensionar el gasto.

<br>

**- Diferenciación frente a soluciones más tecnológicas pero menos personalizadas**

**Estrategia:** Aprovechar la cercanía con el cliente como ventaja frente a competidores como RDA Mobility o iLab Perú, que tienden a soluciones más automatizadas pero poco adaptables.

**Táctica:**

Ofrecer soporte humano en todo momento (asesoría técnica y de negocio) como parte del servicio.

Diseñar funcionalidades a medida según el giro del cliente (agrícola, carga ligera, escolar, etc.).

Mantener comunicación constante con los usuarios para evolucionar el producto según sus comentarios.

<br>

**3) Estrategias basadas en oportunidades**

**- Crecimiento del mercado de gestión de flotas en zonas rurales e interprovinciales**

**Estrategia:** Aprovechar la baja presencia de competidores en zonas rurales del Perú para posicionar a Flota365 como la opción ideal en regiones con alto crecimiento agrícola y de transporte interprovincial.

**Táctica:**

Realizar campañas de marketing regionalizadas enfocadas en cooperativas agrarias, municipalidades y empresas de transporte rural.

Establecer alianzas con asociaciones locales para impulsar la adopción del sistema.

Desarrollar funcionalidades offline o de bajo consumo de datos para operatividad en zonas con baja conectividad.

<br>

**- Tendencia creciente hacia la digitalización y control de costos en PYMEs**

**Estrategia:** Posicionar a Flota365 como una herramienta accesible y poderosa para pequeñas y medianas empresas que buscan digitalizar sus operaciones logísticas sin grandes inversiones.

**Táctica:**

Crear planes de suscripción adaptados al tamaño de la empresa, con escalabilidad garantizada.

Implementar un sistema de prueba gratuita o demos interactivos para facilitar la conversión de nuevos clientes.

Generar contenido educativo que muestre los beneficios concretos del control de flotas con ejemplos sencillos (reducción de combustible, control de mantenimiento, prevención de robos, etc.).

<br>

**- Creciente conciencia sobre sostenibilidad y eficiencia operativa**

**Estrategia:** Incorporar a Flota365 dentro del discurso de eficiencia energética y sostenibilidad que muchas empresas están adoptando.

**Táctica:**

Integrar métricas de consumo y emisiones en los reportes de uso de vehículos.

Promover prácticas como el mantenimiento preventivo y la optimización de rutas para reducir la huella de carbono.

Posicionar la plataforma como una aliada en los esfuerzos de RSE (Responsabilidad Social Empresarial) de las empresas.

<br>

**- Avance de tecnologías IoT y accesibilidad de dispositivos GPS**

**Estrategia:** Integrar nuevas tecnologías para robustecer la propuesta de valor de Flota365 con bajo costo operativo.

**Táctica:**

Facilitar la integración con diversos modelos de GPS o sensores IoT del mercado.

Establecer alianzas con proveedores de hardware para ofrecer paquetes completos a los clientes (software + GPS).

Investigar y desarrollar integraciones con dispositivos móviles para ofrecer funciones como escaneo QR o control desde smartphones.

<br>

**4) Estrategias basadas en amenazas**

**- Competencia con soluciones de alto presupuesto (Geotab, AFE Logistics)**

**Estrategia:** Enfocar la estrategia comercial de Flota365 como una alternativa accesible y eficiente frente a plataformas de alto costo.

**Táctica:**

Resaltar la relación costo-beneficio de Flota365 frente a sistemas de gran escala que suelen tener costos elevados de implementación.

Ofrecer modelos de suscripción flexibles y precios competitivos por unidad o por usuario.

Aplicar campañas publicitarias dirigidas a empresas medianas que requieren soluciones funcionales sin sobredimensionar el gasto.

<br>

**- Diferenciación frente a soluciones más tecnológicas pero menos personalizadas**

**Estrategia:** Aprovechar la cercanía con el cliente como ventaja frente a competidores como RDA Mobility o iLab Perú, que tienden a soluciones más automatizadas pero poco adaptables.

**Táctica:**

Ofrecer soporte humano en todo momento (asesoría técnica y de negocio) como parte del servicio.

Diseñar funcionalidades a medida según el giro del cliente (agrícola, carga ligera, escolar, etc.).

Mantener comunicación constante con los usuarios para evolucionar el producto según sus comentarios.


<h3 id="interviews">2.2. Entrevistas</h4>

En esta sección se aborda la investigación tomando como base la recolección de información en base a entrevistas a representantes de los segmentos objetivo. Es decir, entrevistaremos a nuestro público objetivo para asi tener más de cerca algunos testimonios y poder trabajar en base a ellos.

## 2.2. Entrevistas
### 2.2.1. Diseño de entrevistas
<h4 id="interviewDesing">Preguntas para segmento 1 - Gestores de flota:</h4>

1: ¿Cuál es tu rol actual y qué responsabilidades tienes en la gestión de la flota?

2: ¿Con cuántos vehículos y conductores trabajas actualmente?

3: ¿Qué herramientas utilizas hoy para gestionar tu flota?

4: ¿Cómo haces seguimiento a los mantenimientos y registros de cada vehículo?

5: ¿Te ha pasado que no pudiste tomar decisiones a tiempo por falta de datos?

6: ¿Qué problemas enfrentas más seguido en la gestión diaria de tus unidades?

7: ¿Has probado algún sistema de gestión de flotas antes? ¿Cuál fue tu experiencia?

8: ¿Qué funcionalidades consideras indispensables en una solución como esta?

9: ¿Qué tan importante es para ti tener reportes automáticos ?¿Pagarías por una plataforma que te de toda la información de tu flota y con ello evitar perdidas monetarias innecesarias?

<h4 id="interviewDesing">Preguntas para segmento 2 - Conductores de vehículos pesados:</h4>

1: ¿Qué tan fácil o difícil es para ti completar estos registros manualmente? ¿Qué parte del proceso te resulta más tediosa o complicada?

2: ¿Cuánto tiempo pierdes, aproximadamente, al tratar de contactar a tu jefe o al equipo para informar un problema técnico?

3: ¿Alguna vez has experimentado retrasos o problemas en tus rutas debido a la falta de información sobre el estado del vehículo?

4: ¿Te gustaría contar con una plataforma  que te permita registrar todos los detalles de manera más rápida y eficiente?

5: Si tuvieras una herramienta que te diga en qué estado está el automóvil, cuánto falta para el mantenimiento, o si hubo un problema mecánico ¿la usarías?
¿Qué herramientas usas actualmente para registrar cualquier problema o inconveniente?

6: ¿Cuál es tu mayor preocupación cuando presentas  problemas mecánicos durante el viaje? ¿Cómo una app podría ayudarte a prevenir estos problemas?

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
### 2.6.x. Bounded Context: 
#### 2.6.x.1. Domain Layer
#### 2.6.x.2. Interface Layer
#### 2.6.x.3. Application Layer
#### 2.6.x.4. Infrastructure Layer
#### 2.6.x.5. Bounded Context Software Architecture Component Level Diagrams
#### 2.6.x.6. Bounded Context Software Architecture Code Level Diagrams
##### 2.6.x.6.1. Bounded Context Domain Layer Class Diagrams
##### 2.6.x.6.2. Bounded Context Database Design Diagram

