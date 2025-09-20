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


## 2.2. Entrevistas

En esta sección se aborda la investigación tomando como base la recolección de información en base a entrevistas a representantes de los segmentos objetivo. Es decir, entrevistaremos a nuestro público objetivo para asi tener más de cerca algunos testimonios y poder trabajar en base a ellos.

### 2.2.1. Diseño de entrevistas
### 2.2.2. Registro de entrevistas
### 2.2.3. Análisis de entrevistas

## 2.3. Needfinding

En esta sección el equipo explica y presenta los artefactos resultantes del proceso de análisis de la información recolectada. Aquí se incluye secciones internas para **User Personas**, **User Task Matrix**, **User Journey Maps**, **Empathy Mapping** y **As-Is Scenario Mapping**:

En esta sección el equipo explica y presenta los artefactos resultantes del proceso de análisis de la información recolectada. Aquí se incluye secciones internas para User Personas, User Task Matrix, User Journey Maps, Empathy Mapping y As-Is Scenario Mapping:

### 2.3.1. User Personas

A partir del análisis de entrevistas y del estudio de la competencia, se identificaron los principales perfiles de usuarios que interactúan directamente con la solución Flota365. Estos perfiles representan los segmentos objetivo clave para el sistema, ya que concentran las necesidades operativas más **críticas** dentro de la gestión de flotas. La construcción de los *User Persona* permite al equipo de desarrollo entender mejor sus motivaciones, frustraciones y hábitos, lo que resulta fundamental para diseñar funcionalidades adecuadas y experiencias de usuario efectivas.

**1) Segmento 1: Gestores de flota** 

Para los gestores de flotas se elaboró el User Persona de **José Alberto Nuñez Peralta**. Se tomaron en cuenta factores clave como su edad, rol profesional, experiencia en gestión logística y toma de decisiones operativas, así como sus principales frustraciones en torno al control y monitoreo de los vehículos. También se evaluó su familiaridad con herramientas tecnológicas como hojas de cálculo, software de gestión y plataformas de análisis de datos, lo cual permitió definir un perfil completo y representativo del segmento.

<div align="center">
    <img src="../images/chapter-II/José Alberto Núñez Peralta.png" alt="User Persona gestores" width="420" height="670"/>
</div>

<br>

**2) Segmento 2: Conductores de vehículos pesados**

Para los conductores de vehículos pesados se elaboró el User Persona de **Victor Manuel Nolazco Herrera Torres**. La construcción de este perfil consideró aspectos como su rutina diaria, contexto laboral, grado de exposición a herramientas digitales, y las principales dificultades que enfrenta durante sus recorridos. Asimismo, se identificó su nivel de uso de tecnologías básicas como GPS, aplicaciones móviles y comunicación digital, lo cual fue determinante para ajustar la propuesta de valor de Flota365 a sus necesidades reales.

<div align="center">
    <img src="../images/chapter-II/Victor Manuel Nolazco Herrera.png" alt="User Persona Gestores" width="420" height="670"/>
</div>

### 2.3.2. User Task Matrix

<table border="1" cellspacing="0" cellpadding="5" style="border-collapse: collapse; text-align: center;">
    <thead>
        <tr>
            <th rowspan="2">User Task Matrix</th>
            <th colspan="2">José Nuñez - Gestor de flota</th>
            <th colspan="2">Victor Nolazco - Conductor de vehículos pesados</th>
        </tr>
        <tr>
            <th>Frecuencia</th>
            <th>Importancia</th>
            <th>Frecuencia</th>
            <th>Importancia</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Supervisar el estado y ubicación de los vehículos</td>
            <td>3</td>
            <td>3</td>
            <td>1</td>
            <td>2</td>
        </tr>
        <tr>
            <td>Organizar rutas y asignar unidades</td>
            <td>3</td>
            <td>3</td>
            <td>2</td>
            <td>2</td>
        </tr>
        <tr>
            <td>Reportar incidentes o eventos en ruta</td>
            <td>2</td>
            <td>2</td>
            <td>3</td>
            <td>3</td>
            </tr>
        <tr>
            <td>Realizar seguimiento de mantenimiento preventivo</td>
            <td>2</td>
            <td>3</td>
            <td>1</td>
            <td>2</td>
        </tr>
        <tr>
            <td>Comunicar novedades al personal de conducción</td>
            <td>2</td>
            <td>2</td>
            <td>1</td>
            <td>1</td>
        </tr>
        <tr>
            <td>Conducir y cumplir con itinerarios asignados</td>
            <td>1</td>
            <td>2</td>
            <td>3</td>
            <td>3</td>
        </tr>
        <tr> 
            <td>Completar registros manuales de entregas o rutas</td>
            <td>1</td>
            <td>1</td>
            <td>3</td>
            <td>2</td>
        </tr>
        <tr>
            <td>Revisar reportes de desempeño o consumo de combustible</td>
            <td>3</td>
            <td>3</td>
            <td>1</td>
            <td>2</td>
        </tr>
        <tr>
            <td>Validar cumplimiento de rutas y horarios</td>
            <td>3</td>
            <td>3</td>
            <td>2</td>
            <td>2</td>
        </tr>
        <tr>
            <td>Generar informes para la gerencia</td>
            <td>2</td>
            <td>3</td>
            <td>1</td>
            <td>1</td>
        </tr>
        <tr>
            <td>Revisar alertas de eventos críticos (exceso de velocidad, paradas no autorizadas)</td>
            <td>3</td>
            <td>3</td>
            <td>2</td>
            <td>2</td>
        </tr>
        <tr>
            <td>Configurar y personalizar alertas o notificaciones</td>
            <td>2</td>
            <td>2</td>
            <td>1</td>
            <td>1</td>
        </tr>
        <tr>
            <td>Capacitar al personal en uso del sistema</td>
            <td>1</td>
            <td>2</td>
            <td>1</td>
            <td>1</td>
        </tr>
        <tr>
            <td>Revisar historial de recorridos (playback GPS)</td>
            <td>2</td>
            <td>2</td>
            <td>1</td>
            <td>1</td>
        </tr>
        <tr>
            <td>Reportar fallas del vehículo desde la app</td>
            <td>1</td>
            <td>1</td>
            <td>3</td>
            <td>3</td>
        </tr>
        <tr>
            <td>Realizar checklist antes de salir a ruta</td>
            <td>1</td>
            <td>1</td>
            <td>3</td>
            <td>3</td>
        </tr>
    </tbody>
</table>

En este cuadro se utilizan los números del uno al tres para representar cuánta importancia y frecuencia posee una actividad frente al usuario que la realiza. En el caso de la frecuencia, el uno equivale a una actividad poco frecuente; el dos, más o menos frecuente y; el tres, muy frecuente. Por otro lado, en el caso de la importancia, el uno significa que la actividad no tiene mucha importancia para el usuario; el dos, que no es tan importante y; el tres, que es una actividad de suma importancia.
<br>

### 2.3.3. User Journey Mapping

**1) Segmento 1: Gestores de flota** 

Para la elaboración del Journey Mapping, el equipo basó su análisis en las observaciones y el conocimiento adquirido a partir de los User Persona previamente creados. Se colocó al centro de cada mapa al usuario correspondiente, José Nuñez (Gestor de Flota) y Victor Nolazco (Conductor de Vehículos Pesados), y se respondió a las preguntas clave sobre su experiencia, emociones, comportamientos y necesidades a lo largo de las distintas fases de interacción con la plataforma.

<div align="center">
    <img src="../images/chapter-II/User Journey Mapping Segmento 1.png" alt="User Journey Mapping Gestores" width="auto" height="670"/>
</div>

Carlos es consciente de los problemas en la gestión logística, como la falta de integración entre sistemas y la dependencia de tareas manuales. Está buscando una solución que le permita tomar decisiones rápidas y basadas en datos en tiempo real. Se registra en la plataforma con la esperanza de optimizar el control de la flota. Aunque al principio se siente frustrado debido a la falta de integración con otros sistemas, rápidamente ajusta los procesos y empieza a ver mejoras en la eficiencia. Si la plataforma no le proporciona la visibilidad que necesita o no mejora su rendimiento, consideraría abandonarla. Su objetivo es lograr una operación más eficiente y consolidarse como un líder estratégico. <br>

**2) Segmento 2: Conductores de vehículos pesados**

<div align="center">
    <img src="../images/chapter-II/User Journey Mapping Segmento 2.png" alt="EUser Journey Mapping Conductores" width="auto" height="670"/>
</div>

Juan enfrenta problemas operativos diarios, como el uso de herramientas poco intuitivas y tareas administrativas que le quitan tiempo. Se interesa por una app que le ayude a gestionar mejor sus rutas y el estado del vehículo. Al registrarse, se siente inseguro sobre la facilidad de uso de la plataforma. A medida que la usa, experimenta frustración inicial por la falta de claridad en algunas funciones, pero empieza a ver los beneficios de recibir alertas claras sobre rutas y condiciones del vehículo. Si la app no resulta ser fácil de usar o no mejora su eficiencia, podría abandonarla. Juan busca una solución sencilla que le permita enfocarse en lo más importante: conducir de manera segura y eficiente.

### 2.3.4. Empathy Mapping

Para la elaboración de los Empathy Maps, el equipo partió del conocimiento y observaciones recolectadas durante el análisis de los User Persona. Se colocó al centro de cada mapa al usuario correspondiente (Carlos Mejía y Juan Torres) y se respondieron las preguntas claves sobre su entorno, emociones, comportamientos y necesidades. 

**1) Segmento 1: Gestores de flota** 

<img src="../images/chapter-II/Empathy_Mapping_Segmento1.jpg" alt="Empathy Mapping Gestores" width="auto" height="370"/>

En este mapa, se analizó a José Nuñez, un gestor enfocado en optimizar los procesos operativos de la flota. Del cuadro, se concluye que José Nuñez es muy consciente de los problemas actuales en la gestión logística, especialmente por la falta de integración entre sistemas y la dependencia de tareas manuales. Le preocupa que los errores humanos y la información desactualizada estén afectando su rendimiento y el de su equipo. Busca una solución que le permita tomar decisiones más rápidas y acertadas basadas en datos en tiempo real. Finalmente, José Nuñez aspira a lograr una operación más eficiente, con menos margen de error, y a consolidar su rol como líder estratégico dentro de la empresa.

<br>

**2) Segmento 2: Conductores de vehículos pesados**

<img src="../images/chapter-II/Empathy_Mapping_Segmento2.jpg" alt="Empathy Mapping Conductores" width="auto" height="370"/>

En este mapa, se abordó la experiencia de Victor Nolazco, un conductor con mucha experiencia pero que enfrenta obstáculos operativos en su día a día. Del cuadro, se concluye que Victor siente frustración al lidiar con herramientas poco intuitivas y tareas administrativas que le quitan tiempo. Le preocupa no contar con un sistema práctico que le permita enfocarse en lo más importante: conducir con seguridad y eficiencia. Busca una app o sistema que simplifique sus tareas, le dé claridad sobre su ruta y le permita reportar cualquier problema de forma rápida. Finalmente, Victor aspira a sentirse valorado, respaldado tecnológicamente y a trabajar en un entorno que respete su tiempo y esfuerzo.

### 2.3.5. Ubiquitous Language

De acuerdo a lo dictaminado por Eric Evans en su libro *Domain-Driven Design: Tackling Complexity in the Heart of Software*, el startup **Flota365** estableció un lenguaje alineado al negocio y de fácil comprensión para cada uno de los miembros de equipo, asegurando una trazabilidad y mantenimiento a futuro en las funcionaliades póstumas tanto dentro de la aplicación como dentro del *core* de los procesos.

* **Fleet (Flota):** Conjunto de vehículos que una organización utiliza para realizar sus operaciones de transporte o logística.

* **Fleet Manager (Gestor de Flota):** Persona responsable de supervisar, controlar y optimizar el uso de los vehículos en la flota.

* **Driver (Conductor):** Persona encargada de operar un vehículo de la flota durante recorridos o actividades asignadas.

* **Trip (Recorrido):** Desplazamiento realizado por un vehículo desde un punto de origen hasta un destino definido, registrando tiempo, distancia y propósito.

* **Mileage (Kilometraje):** Distancia total recorrida por un vehículo, utilizada para control de mantenimiento, consumo de combustible y planificación.

* **Activity Log (Registro de Actividad):** Historial de acciones realizadas por el conductor, como inicio y fin de recorridos, paradas o incidentes.

* **Incident Report (Reporte de Incidencia):** Notificación de un evento inesperado que afecta el recorrido o el vehículo, como fallas mecánicas o accidentes.

* **Maintenance Alert (Alerta de Mantenimiento):** Notificación generada para indicar que un vehículo requiere revisión o reparación preventiva/correctiva.

* **Vehicle Assignment (Asignación de Vehículo):** Proceso mediante el cual un gestor designa un vehículo específico a un conductor para una tarea o recorrido.

* **Digital Proof (Evidencia Digital):** Documento o registro en formato digital (foto, firma o archivo) que valida la ejecución de una actividad en la aplicación.

* **Fuel Record (Registro de Combustible):** Información capturada por el conductor sobre carga de combustible, consumo y costos asociados.

* **Route Optimization (Optimización de Ruta):** Estrategia de planificación para determinar el trayecto más eficiente en términos de tiempo, distancia y consumo.

* **Downtime (Tiempo de Inactividad):** Periodo en el que un vehículo no puede ser utilizado debido a mantenimiento, avería u otras razones operativas.

* **Driver Identification (Identificación del Conductor):** Validación del perfil de un conductor en la aplicación mediante DNI, credenciales o autenticación digital.

* **Operational Report (Reporte Operativo):** Documento generado por el sistema que presenta métricas clave sobre recorridos, incidencias y desempeño de la flota.

* **Compliance Check (Verificación de Cumplimiento):** Evaluación que asegura que el conductor y el vehículo cumplen con regulaciones, permisos y normas establecidas.

* **Geolocation (Geolocalización):** Identificación de la posición en tiempo real de un vehículo o conductor mediante coordenadas GPS.

* **Notification (Notificación):** Mensaje enviado al gestor o conductor a través de la aplicación para informar sobre alertas, asignaciones o incidencias.

* **Performance Indicator (Indicador de Desempeño):** Métrica utilizada para evaluar la eficiencia de la flota, como consumo de combustible, puntualidad o disponibilidad.

* **User Role (Rol de Usuario):** Categoría asignada a cada persona dentro del sistema (ejemplo: gestor o conductor), que determina permisos y accesos en la aplicación.

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
### 2.6.1. Bounded Context: 
#### 2.6.1.1. Domain Layer

La capa de dominio es el núcleo de la aplicación, pues en ella se definen los modelos y reglas esenciales que conforman la lógica del negocio. Dentro de este marco, el agregado "User" se establece como la entidad principal que simboliza a los usuarios del sistema, incluyendo sus propiedades y responsabilidades. Esta capa asegura que los conceptos del negocio y sus interacciones se representen y gestionen de manera adecuada.

Propósito: Modelar las entidades del dominio, integrando tanto sus atributos como sus comportamientos, con el fin de reflejar fielmente los elementos centrales de la aplicación, como usuarios, productos, procesos comerciales, entre otros.

* Aggregate: User  
**Descripción:**  El agregado "Usuario" actúa como la raíz del modelo, encapsulando los datos esenciales de la cuenta y su rol dentro del sistema. Su representación en la base de datos se realiza mediante la tabla users, asegurando la persistencia de esta entidad clave.

|Atributo|Tipo|Descripción|
|:-|:-|:-|
|id|Long|Identificador único del usuario (autogenerado).|
|username|String|Nombre de usuario único del sistema.|
|password|String|Contraseña del usuario.|
|roles|Set<Role>|Conjunto de roles asociados al usuario.|
|proofingApoderado|String|Prueba o evidencia del usuario como apoderado (almacenada como texto).|
|createdAt|Date|Fecha de creación del usuario (heredado de la clase base).|
|updatedAt|Date|Fecha de la última actualización del usuario (heredado de la clase base).|

|Método|Descripción|
|:-|:-|
|addRoles(List< Role >roles)|Añade una lista de role para el usuario , retorna el usuario con su rol añadido|
|getAuthorities()|retorna el conjunto de roles (roles) del usuario, que ya implementan la interfaz GrantedAuthority. Esto permite que Spring Security utilice esta información para realizar la autorización de acceso en la aplicación.|
|isAccountNonExpired()| Indica si la cuenta del usuario no ha expirado. Devuelve true si la cuenta sigue siendo válida.|
|isAccountNonLocked()| Indica si la cuenta del usuario no está bloqueada. Devuelve true si la cuenta está desbloqueada.|
|isCredentialsNonExpired()| Indica si las credenciales del usuario (como la contraseña) no han expirado. Devuelve true si las credenciales son válidas.|
|isEnabled()| Indica si la cuenta del usuario está habilitada. Devuelve true si la cuenta está activa.|
|getId()|Retorna el id del usuario.||
|getUsername()| Devuelve el nombre de usuario del usuario (valor incrustado)|
|getEmail()| Devuelve el correo electrónico del usuario (valor incrustado)|
|getPassword()| Devuelve la contraseña del usuario (valor incrustado)|

* Value Object: EmailAddress  
**Descripción:**  Representa una dirección de correo electrónico válida como un objeto de valor embebido.

|Atributo|Tipo|Descripción|
|:-|:-|:-|
|email|String|Dirección de correo electrónico validada (no en blanco, máximo 50 caracteres, formato válido de correo).|
|Método|Descripción||
|EmailAddress(String email)|Constructor que recibe un correo electrónico y lo valida según las restricciones.||
|EmailAddress()|Constructor por defecto que inicializa con null .||

#### 2.6.1.2. Interface Layer




#### 2.6.1.3. Application Layer





#### 2.6.1.4. Infrastructure Layer
#### 2.6.1.5. Bounded Context Software Architecture Component Level Diagrams
#### 2.6.1.6. Bounded Context Software Architecture Code Level Diagrams
##### 2.6.1.6.1. Bounded Context Domain Layer Class Diagrams
##### 2.6.1.6.2. Bounded Context Database Design Diagram