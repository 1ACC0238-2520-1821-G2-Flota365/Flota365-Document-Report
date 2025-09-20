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

| Story ID | User | Priority | Epic | Title | Description | Acceptance Criteria |
|----------|------|----------|------|-------|-------------|---------------------|
| US01     | Gestor | Alta     | 1    | Landing Page informativa | Como gestor, quiero ver información sobre la empresa, para decidir si la plataforma es confiable. | **Given** que soy un gestor que visita la landing page, **When** hago scroll en la página, **Then** veo secciones diferenciadas con información clara sobre la empresa (misión, visión, servicios). **Given** que soy un visitante, **When** ingreso a la página, **Then** el contenido es accesible sin necesidad de iniciar sesión. **Given** que la página carga, **When** visualizo el diseño, **Then** transmite confianza usando imágenes, testimonios y logos de clientes. |
| US02     | Gestor o Conductor | Alta | 1 | Responsive | Como gestor o conductor, quiero que la página sea responsive, para usarla cómodamente desde cualquier dispositivo. | **Given** que soy un usuario accediendo desde un dispositivo móvil, **When** abro la página, **Then** la página se adapta correctamente a móviles, tabletas y escritorio. **Given** que soy un usuario móvil, **When** navego por la página, **Then** no se presenta desplazamiento horizontal y los elementos se redistribuyen correctamente. |
| US03     | Gestor | Alta | 1 | Comparador de planes | Como gestor, deseo comparar los planes disponibles, para elegir el más adecuado para mi empresa. | **Given** que soy un gestor, **When** visualizo los planes disponibles, **Then** puedo comparar al menos 2 o más planes en una tabla o tarjeta. **Given** que elijo un plan, **When** veo el plan, **Then** incluyo detalles de precio, beneficios y condiciones. **Given** que un plan no está disponible, **When** lo visualizo, **Then** el sistema muestra una indicación (ej. desactivado). |
| US04     | Gestor o Conductor | Media | 1 | Switcher de idiomas | Como gestor o conductor, quiero poder cambiar el idioma entre español e inglés, para entender el contenido fácilmente. | **Given** que soy un usuario, **When** selecciono el botón de idioma, **Then** puedo cambiar entre español e inglés. **Given** que cambio el idioma, **When** actualizo la página, **Then** todo el contenido de texto cambia de idioma al instante. **Given** que cambio el idioma, **When** navego entre páginas, **Then** el idioma seleccionado se conserva. |
| US05     | Gestor o Conductor | Media | 1 | Tema de colores | Como gestor o conductor, deseo cambiar el tema de colores, para personalizar la interfaz a mi gusto. | **Given** que soy un usuario, **When** selecciono el tema de colores, **Then** elijo entre al menos dos temas (ej. claro y oscuro). **Given** que cambio de tema, **When** se aplica el nuevo tema, **Then** todos los elementos de la interfaz respetan el tema seleccionado. |
| US06     | Gestor | Baja | 1 | Vista de developers | Como gestor, quiero saber quiénes son los desarrolladores, para tener mayor confianza en la plataforma. | **Given** que soy un gestor en la landing page, **When** visualizo la sección de "equipo de desarrollo", **Then** veo nombres, roles y fotos (opcional) de los desarrolladores. **Given** que soy un visitante, **When** accedo a la página, **Then** la sección tiene un diseño consistente con el resto del sitio. |
| US07     | Gestor | Alta | 2 | Registro de nuevo usuario | Como gestor, quiero registrarme en la plataforma, para probar las funcionalidades y evaluar su utilidad. | **Given** que soy un nuevo usuario, **When** ingreso mis datos en el formulario, **Then** el sistema valida los campos requeridos (nombre, email, contraseña). **Given** que registro mi cuenta con éxito, **When** envío mi formulario, **Then** recibo una confirmación visual de registro exitoso. |
| US08     | Gestor o Conductor | Alta | 2 | Alerta de cerrar sesión | Como gestor o conductor, deseo recibir una alerta al cerrar sesión, para asegurarse de cerrar correctamente y evitar accesos no deseados. | **Given** que estoy por cerrar sesión, **When** confirmo mi decisión, **Then** el sistema muestra una alerta de confirmación. **Given** que confirmo cerrar sesión, **When** se cierra la sesión, **Then** se redirige a la landing page. |
| US09     | Gestor | Alta | 3 | Registro de vehículo | Como gestor, quiero registrar los vehículos para saber cuántos hay. | **Given** que soy un gestor, **When** ingreso los datos del vehículo (placa, marca, modelo, tipo), **Then** el sistema valida que la placa no esté duplicada. **Given** que el vehículo se registra exitosamente, **When** lo confirmo, **Then** el vehículo aparece en el listado automáticamente. |
| US10     | Gestor | Alta | 3 | Delegar vehículo | Como gestor, quiero delegar un vehículo a un conductor para que él pueda usarlo. | **Given** que soy un gestor, **When** selecciono un conductor y un vehículo para asignarlo, **Then** el sistema registra la asignación correctamente. **Given** que el vehículo ya está asignado, **When** intento asignarlo a otro conductor, **Then** el sistema muestra una advertencia. |
| US11     | Gestor | Baja | 1 | Footer informativo | Como gestor, quiero ver un footer con información útil, para conocer términos, contactos y redes sociales. | **Given** que soy un gestor, **When** visualizo el footer en cualquier página, **Then** el footer incluye enlaces a contacto, términos y redes sociales. **Given** que soy un usuario, **When** hago click en los enlaces, **Then** estos deben funcionar correctamente. |
| US12     | Conductor | Media | 5 | Información conductor | Como conductor quiero ver mis datos personales para saber que están correctos. | **Given** que soy un conductor, **When** accedo a mi perfil, **Then** veo mi nombre, DNI, correo y teléfono. **Given** que encuentro un error en mis datos, **When** los edito, **Then** puedo solicitar la corrección de los mismos. |
| US13     | Conductor | Alta | 4 | Reportar incidencia | Como conductor, quiero reportar un incidente durante el uso del vehículo, para notificar al gestor de cualquier problema. | **Given** que soy un conductor, **When** reporto una incidencia, **Then** el sistema registra tipo y descripción de la incidencia. **Given** que la incidencia tiene foto, **When** la adjunto, **Then** se guarda correctamente con fecha y hora. |
| US14     | Conductor | Media | 3 | Información del vehículo | Como conductor, quiero consultar el estado técnico del vehículo antes de usarlo, para asegurarme de que está en condiciones. | **Given** que soy un conductor, **When** reviso el estado técnico del vehículo, **Then** se muestra si hay alguna falla pendiente. **Given** que el estado del vehículo es actualizado, **When** se actualiza en el sistema, **Then** se muestra la nueva información de mantenimiento. |
| US15     | Conductor | Media | 5 | Registro de combustible | Como conductor, quiero registrar el combustible cargado al vehículo, para llevar control del consumo. | **Given** que soy un conductor, **When** ingreso la cantidad de combustible, **Then** el sistema guarda los detalles del combustible cargado. **Given** que subo una foto del ticket, **When** la adjunto, **Then** se guarda correctamente en el historial del vehículo. |
| US16     | Conductor | Media | 5 | Registro de pausas | Como conductor, quiero registrar descansos o pausas durante el servicio, para que queden reflejados en la asignación. | **Given** que soy un conductor, **When** indico el inicio y fin de cada pausa, **Then** la duración se calcula automáticamente. **Given** que el servicio es generado, **When** se registra la pausa, **Then** esta se refleja en el reporte del servicio. |
| US17     | Conductor | Media | 4 | Confirmación de evidencia | Como conductor, quiero recibir una confirmación cuando se registra mi evidencia de uso, para asegurarme de que fue enviada correctamente. | **Given** que soy un conductor, **When** envío la evidencia de uso, **Then** recibo una notificación con la hora y el contenido. **Given** que hay un error en el envío, **When** el sistema lo detecta, **Then** me muestra una alerta de error. |
| US18     | Gestor de flota | Alta | 3 | Ver qué vehículos están en uso | Como gestor de flota, quiero ver qué vehículos están en uso, para tomar decisiones rápidamente. | **Given** que soy un gestor, **When** visualizo la lista de vehículos, **Then** veo los vehículos activos con su conductor asignado. **Given** que un vehículo está disponible, **When** lo filtro, **Then** se marca como "Disponible". |
| US19     | Gestor de flota | Alta | 4 | Resolver incidencias | Como gestor de flota, quiero saber si hay incidencias, para resolverlas lo más rápido posible. | **Given** que soy un gestor, **When** veo la lista de incidencias, **Then** puedo ver su estado (pendiente o resuelta). **Given** que una incidencia está pendiente, **When** la selecciono, **Then** puedo asignar un técnico responsable. |
| US20     | Gestor de flota | Alta | 4 | Asignar mantenimiento | Como gestor de flota, quiero asignar mantenimiento preventivo para evitar fallas futuras. | **Given** que soy un gestor, **When** programo el mantenimiento, **Then** defino la fecha, vehículo y tipo de servicio. **Given** que el mantenimiento es programado, **When** se notifica al conductor, **Then** se registra en el historial del vehículo. |
| US21     | Gestor de flota | Media | 4 | Asignar técnico | Como gestor de flota, quiero asignar técnicos a órdenes de mantenimiento, para asegurar que las tareas se realicen a tiempo. | **Given** que soy un gestor, **When** elijo un técnico disponible, **Then** se asigna al mantenimiento correspondiente. **Given** que se asigna el técnico, **When** el sistema confirma, **Then** el técnico recibe una notificación. |
| US22     | Conductor o Gestor | Media | 2 | Cambio de contraseña | Como conductor o gestor, quiero cambiar mi contraseña, para mantener mi cuenta segura. | **Given** que soy un usuario, **When** ingreso al perfil y selecciono la opción de cambiar contraseña, **Then** se valida la contraseña actual antes de permitir el cambio. **Given** que cambio mi contraseña, **When** se confirma, **Then** el sistema muestra un mensaje de éxito. |
| US23     | Conductor | Alta | 5 | Estadísticas personales del conductor | Como conductor, quiero ver mis estadísticas de rendimiento, para mejorar mi desempeño. | **Given** que soy un conductor, **When** visualizo mis estadísticas de rendimiento, **Then** puedo ver mis viajes completados y rendimiento. **Given** que quiero filtrar los datos, **When** selecciono el período, **Then** se muestran los resultados por semana, mes o año. |
| US24     | Conductor o Gestor | Baja | 2 | Cambiar foto de perfil | Como conductor o gestor, quiero cambiar mi foto de perfil, para personalizar mi cuenta. | **Given** que soy un usuario, **When** elijo una foto, **Then** solo formatos JPG y PNG son permitidos. **Given** que subo la foto, **When** el sistema confirma, **Then** la foto es visible tanto para el gestor como para el conductor. |
| US25     | Conductor | Media | 5 | Solicitud de cambio de turno | Como conductor, quiero solicitar un cambio de turno, para organizar mejor mi jornada. | **Given** que soy un conductor, **When** ingreso la solicitud de cambio de turno, **Then** el gestor puede aceptarla o rechazarla. **Given** que la solicitud es procesada, **When** se guarda el historial de solicitudes, **Then** el estado se refleja correctamente. |
| US26     | Conductor | Media | 5 | Visualización de vehículo asignado | Como conductor, quiero ver claramente cuál es mi vehículo asignado del día, para evitar confusiones. | **Given** que soy un conductor, **When** inicio sesión, **Then** se muestra el vehículo asignado con placa, tipo y horario asignado. **Given** que no tengo asignación, **When** el sistema lo indica, **Then** me muestra un mensaje de "Sin asignación". |
| US27     | Gestor de flota | Alta | 6 | Visualización de rutas completadas vs planificadas | Como gestor, quiero ver cuántas rutas fueron completadas frente a las planificadas, para evaluar cumplimiento. | **Given** que soy un gestor, **When** visualizo las rutas, **Then** veo las planificadas y las realizadas, con porcentaje de cumplimiento. **Given** que quiero filtrar por conductor o fecha, **When** aplico el filtro, **Then** los resultados se actualizan dinámicamente. |
| US28     | Gestor de flota | Alta | 4 | Análisis predictivo con IA | Como gestor, quiero tener un análisis con IA para poder predecir posibles fallos o problemas. | **Given** que soy un gestor, **When** el sistema procesa datos históricos, **Then** muestra predicciones de fallos o problemas. **Given** que el análisis es por vehículo, **When** visualizo el resultado, **Then** se muestra información detallada por cada vehículo. |
| US29     | Gestor de flota | Media | 4 | Historial de análisis de IA | Como gestor, quiero tener un historial de los análisis hechos por la inteligencia artificial para poder ver a detalle la información. | **Given** que soy un gestor, **When** accedo al historial de análisis, **Then** puedo ver cada análisis realizado con fecha y detalles. **Given** que visualizo un análisis, **When** lo selecciono, **Then** se muestran los detalles completos. |
| US30     | Gestor de flota | Alta | 6 | Filtros de reportes | Como gestor, quiero tener filtros de reportes para poder hacer una búsqueda más rápida. | **Given** que soy un gestor, **When** filtro los reportes por fecha, vehículo o tipo de análisis, **Then** los resultados se actualizan dinámicamente. **Given** que quiero filtrar por diferentes parámetros, **When** aplico los filtros, **Then** los resultados se muestran en tiempo real. |
| US31     | Gestor de flota | Alta | 6 | Limpieza de filtros | Como gestor, quiero limpiar el filtro de reportes para poder hacer otra búsqueda por filtro. | **Given** que soy un gestor, **When** selecciono el botón de limpiar filtro, **Then** los filtros aplicados se restablecen. **Given** que limpio los filtros, **When** se restaura la vista inicial, **Then** puedo aplicar nuevos filtros sin interferencias. |
| US32     | Gestor de flota | Alta | 3 | Monitoreo de la flota | Como gestor, quiero monitorear la flota para saber el estado del vehículo. | **Given** que soy un gestor, **When** visualizo los vehículos en el sistema, **Then** puedo ver su estado actual en tiempo real, incluyendo ubicación, fallos detectados y estado operativo. **Given** que un vehículo tiene alerta, **When** lo visualizo, **Then** se destaca visualmente. |
| US33     | Gestor de flota | Media | 3 | Exportar listado de vehículos | Como gestor, quiero exportar el listado de vehículos para poder tener un reporte en físico. | **Given** que soy un gestor, **When** selecciono la opción de exportar, **Then** puedo obtener un archivo en formato PDF o Excel. **Given** que aplico filtros en el listado, **When** exporto el reporte, **Then** los filtros aplicados se respetan. |
| US34     | Desarrollador | Alta | 7 | Inicio de sesión con validación | Como desarrollador, quiero implementar una funcionalidad de inicio de sesión, para que los usuarios registrados puedan acceder de forma segura a la plataforma. | **Given** que soy un usuario, **When** ingreso mis credenciales, **Then** el sistema valida las credenciales y me redirige a la vista principal. **Given** que las credenciales son incorrectas, **When** intento iniciar sesión, **Then** se muestra un mensaje de error claro. |
| US35     | Desarrollador | Alta | 7 | Registro de usuarios | Como desarrollador, quiero implementar el endpoint de registro de usuarios, para que nuevos usuarios puedan guardar sus datos en la base de datos. | **Given** que soy un nuevo usuario, **When** envío mis datos de registro, **Then** el sistema valida los campos y los guarda correctamente. **Given** que registro un usuario, **When** el sistema responde con un ID y status 201. |
| US36     | Desarrollador | Alta | 7 | Inicio de sesión con JWT | Como desarrollador, quiero implementar un login con generación de token JWT, para autenticar correctamente a los usuarios. | **Given** que soy un usuario, **When** ingreso mis credenciales, **Then** el sistema valida las credenciales y responde con un token JWT válido. **Given** que las credenciales son incorrectas, **When** intento iniciar sesión, **Then** recibo un error 401 Unauthorized. |
| US37     | Desarrollador | Alta | 7 | Middleware de autenticación | Como desarrollador, quiero validar el token JWT en endpoints protegidos, para asegurar que solo usuarios autorizados accedan. | **Given** que soy un usuario autenticado, **When** hago una solicitud a un endpoint protegido, **Then** el sistema valida el token y permite el acceso. **Given** que el token es inválido, **When** hago la solicitud, **Then** recibo un error 403 Forbidden. |
| US38     | Desarrollador | Alta | 7 | CRUD de vehículos | Como desarrollador, quiero exponer endpoints para crear, leer, actualizar y eliminar vehículos, para permitir la gestión desde el frontend. | **Given** que soy un desarrollador, **When** llamo al endpoint CRUD de vehículos, **Then** el sistema permite crear, leer, actualizar y eliminar vehículos con validación de datos. **Given** que el vehículo es creado, **When** se guarda en la base de datos, **Then** se responde con un mensaje y código adecuado. |
| US39     | Desarrollador | Alta | 7 | Asignación de vehículo a conductor | Como desarrollador, quiero implementar la lógica de asignación de vehículos a conductores, para registrar esta relación en el sistema. | **Given** que soy un desarrollador, **When** llamo al endpoint de asignación, **Then** se guarda correctamente la asignación de conductor y vehículo. **Given** que un vehículo ya está asignado, **When** intento asignarlo, **Then** recibo una advertencia. |
| US40     | Desarrollador | Alta | 7 | Historial de incidencias | Como desarrollador, quiero permitir el registro y la consulta de incidencias, para que los conductores puedan reportar problemas y el gestor los revise. | **Given** que soy un desarrollador, **When** llamo al endpoint de incidencias, **Then** se guarda correctamente la incidencia. **Given** que el gestor consulta incidencias, **When** llama al endpoint, **Then** puede ver el historial de incidencias con filtros. |
| US41     | Desarrollador | Alta | 7 | Reporte de consumo de combustible | Como desarrollador, quiero implementar la grabación del consumo de combustible, para llevar el control por vehículo y por conductor. | **Given** que soy un desarrollador, **When** llamo al endpoint de registro de combustible, **Then** se guardan los detalles del combustible, incluyendo cantidad y ticket. **Given** que un registro es exitoso, **When** el sistema responde con los datos guardados, **Then** el gestor puede revisar el historial. |
| US42     | Desarrollador | Alta | 7 | Historial de mantenimientos | Como desarrollador, quiero implementar el historial de mantenimientos por vehículo, para que el gestor pueda revisar los servicios realizados. | **Given** que soy un desarrollador, **When** llamo al endpoint de mantenimientos, **Then** devuelve una lista detallada con tipo de servicio, fecha y técnico responsable. **Given** que el gestor consulta, **When** aplica filtros, **Then** el sistema muestra los resultados filtrados. |
| US43     | Desarrollador | Alta | 7 | Exportación de reportes | Como desarrollador, quiero generar archivos PDF o Excel con información del sistema, para que el gestor pueda descargar reportes. | **Given** que soy un desarrollador, **When** llamo al endpoint de exportación de reportes, **Then** se genera un archivo en formato PDF o Excel. **Given** que el gestor tiene filtros aplicados, **When** exporta, **Then** los filtros se respetan en el archivo exportado. |

<h3 id="impactMapping"> 2.4.2. Impact Mapping </h3>

<table border="1" cellpadding="6" cellspacing="0">
  <tbody>
    <tr>
      <td>Mejorar la experiencia de navegación y conversión</td>
      <td>Visitante / Gestor</td>
      <td>Comprender el valor de la plataforma y navegar desde cualquier dispositivo</td>
      <td>US01, US02, US03, US04, US05, US06, US11</td>
    </tr>
    <tr>
      <td>Facilitar el acceso a la plataforma</td>
      <td>Gestor / Conductor</td>
      <td>Registrarse, personalizar y proteger su cuenta</td>
      <td>US07, US08, US22, US24</td>
    </tr>
    <tr>
      <td>Control y delegación eficiente de vehículos</td>
      <td>Gestor</td>
      <td>Registrar vehículos, asignarlos y supervisar su estado</td>
      <td>US09, US10, US14, US18, US20, US21</td>
    </tr>
    <tr>
      <td>Gestión de incidencias en flota</td>
      <td>Gestor</td>
      <td>Detectar y atender incidencias, realizar mantenimiento preventivo</td>
      <td>US13, US17, US19, US20, US21</td>
    </tr>
    <tr>
      <td>Autonomía y eficiencia operativa del conductor</td>
      <td>Conductor</td>
      <td>Consultar información, registrar acciones y ver su desempeño</td>
      <td>US12, US15, US16, US23, US25, US26</td
    </tr>
    <tr>
      <td>Control logístico del desempeño</td>
      <td>Gestor</td>
      <td>Evaluar cumplimiento de rutas y eficiencia logística</td>
      <td>US27,US30,US31</td>
    </tr>
       <tr>
      <td>Backend API</td>
      <td>desarrollador</td>
      <td>Crear el backend y los endpoints</td>
      <td>US34,US35,US36,US37,US38,US39,US40,US41,US42,US43</td>
    </tr>
      
  </tbody>
</table>


<h3 id="impactMapping"> 2.4.3. Product Backlog </h3>
# Product Backlog

| #  | User Story ID | Título                                   | Descripción                                                                                                                                     | Story Points | Prioridad |
|----|---------------|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------|-----------|
| 1  | US09          | Registro de vehículo                     | Como gestor quiero registrar los vehículos para llevar un control de la flota.                                                                  | 5            | Alta      |
| 2  | US18          | Ver vehículos en uso                     | Como gestor de flota, quiero ver qué vehículos están en uso para tomar decisiones rápidamente.                                                   | 5            | Alta      |
| 3  | US19          | Resolver incidencias                     | Como gestor de flota, quiero saber si hay incidencias, para resolverlas lo más rápido posible.                                                   | 5            | Alta      |
| 4  | US10          | Delegar vehículo                         | Como gestor quiero delegar un vehículo a un conductor para que él pueda usarlo.                                                                  | 5            | Alta      |
| 5  | US32          | Monitoreo de la flota                    | Como gestor, quiero monitorear la flota para saber el estado del vehículo.                                                                        | 5            | Alta      |
| 6  | US14          | Información del vehículo                 | Como conductor, quiero consultar el estado técnico del vehículo antes de usarlo, para asegurarme de que está en condiciones.                      | 3            | Alta      |
| 7  | US16          | Registro de pausas                       | Como conductor, quiero registrar descansos o pausas durante el servicio, para que queden reflejados en la asignación.                             | 2            | Media     |
| 8  | US17          | Confirmación de evidencia                | Como conductor, quiero recibir una confirmación cuando se registre mi evidencia de uso, para asegurarme de que fue enviada correctamente.        | 2            | Alta      |
| 9  | US13          | Reportar incidencia                      | Como conductor, quiero reportar una incidencia durante el uso del vehículo, para notificar al gestor de cualquier problema.                        | 5            | Alta      |
| 10 | US15          | Registro de combustible                   | Como conductor, quiero registrar el combustible cargado al vehículo, para llevar control del consumo.                                            | 5            | Alta      |
| 11 | US01          | Landing Page informativa                 | Como gestor, quiero ver información sobre la empresa, para decidir si la plataforma es confiable.                                                 | 2            | Baja      |
| 12 | US04          | Switcher de idiomas                      | Como gestor o conductor, quiero poder cambiar el idioma entre español e inglés para entender el contenido fácilmente.                           | 3            | Alta      |
| 13 | US02          | Responsive                               | Como gestor o conductor, quiero que la página sea responsive, para usarla cómodamente desde cualquier dispositivo móvil.                          | 3            | Alta      |
| 14 | US12          | Información del conductor                | Como conductor, quiero ver mis datos personales para saber que están correctos.                                                                  | 2            | Alta      |
| 15 | US05          | Tema de colores                          | Como gestor o conductor, deseo cambiar el tema de colores de la interfaz, para personalizar mi experiencia.                                       | 2            | Media     |
| 16 | US08          | Alerta de cerrar sesión                  | Como gestor o conductor, deseo recibir una alerta al cerrar sesión para confirmar que se cierra correctamente.                                 | 2            | Media     |
| 17 | US07          | Registro de nuevo usuario                | Como gestor, quiero registrarme en la plataforma, para probar las funcionalidades y evaluar su utilidad.                                          | 3            | Alta      |
| 18 | US06          | Vista de developers                      | Como gestor, quiero saber quiénes son los desarrolladores, para tener mayor confianza en la plataforma.                                           | 1            | Baja      |
| 19 | US11          | Footer informativo                       | Como gestor, quiero ver un footer con información útil como contacto, términos, y redes sociales.                                               | 1            | Baja      |
| 20 | US21          | Asignar técnico                          | Como gestor de flota, quiero asignar técnicos a las órdenes de mantenimiento, para asegurar que las tareas se realicen a tiempo.                   | 2            | Baja      |
| 21 | US22          | Cambio de contraseña                     | Como conductor o gestor, quiero cambiar mi contraseña para mantener la seguridad de mi cuenta.                                                   | 2            | Baja      |
| 22 | US23          | Estadísticas del conductor               | Como conductor, quiero ver mis estadísticas de rendimiento para mejorar mi desempeño.                                                            | 3            | Media     |
| 23 | US24          | Cambiar foto de perfil                   | Como conductor o gestor, quiero cambiar mi foto de perfil para personalizar mi cuenta.                                                           | 1            | Baja      |
| 24 | US25          | Solicitud de cambio de turno             | Como conductor, quiero solicitar un cambio de turno para organizar mejor mi jornada.                                                             | 2            | Media     |
| 25 | US26          | Visualización de vehículo asignado       | Como conductor, quiero ver claramente cuál es mi vehículo asignado del día para evitar confusiones.                                                | 2            | Alta      |
| 26 | US27          | Rutas completadas vs planificadas        | Como gestor, quiero ver cuántas rutas fueron completadas frente a las planificadas, para evaluar el cumplimiento de los objetivos.               | 5            | Alta      |
| 27 | US28          | Análisis predictivo con IA               | Como gestor, quiero recibir predicciones basadas en IA sobre el estado de los vehículos, para prevenir posibles fallas durante el servicio.       | 8            | Alta      |
| 28 | US29          | Historial de análisis de IA              | Como gestor quiero un historial de los análisis hechos por la inteligencia artificial para poder ver a detalle la información.                    | 3            | Media     |
| 29 | US30          | Filtros de reportes                      | Como gestor, quiero tener filtros de reportes para poder hacer una búsqueda más rápida.                                                          | 5            | Alta      |
| 30 | US31          | Limpieza de filtros                      | Como gestor, quiero limpiar los filtros aplicados, para hacer otra búsqueda por filtro.                                                          | 2            | Media     |
| 31 | US33          | Exportar reporte                         | Como gestor, quiero exportar el listado de vehículos para tener un reporte en físico.                                                            | 5            | Baja      |
| 32 | US39          | Asignación de vehículo a conductor       | Como desarrollador, quiero guardar la relación entre conductor y vehículo en el sistema.                                                          | 5            | Alta      |
| 33 | US38          | CRUD de vehículos                        | Como desarrollador, quiero exponer endpoints para crear, leer, actualizar y eliminar vehículos para permitir la gestión desde el frontend.         | 8            | Alta      |
| 34 | US40          | Historial de incidencias                 | Como desarrollador, quiero registrar incidencias para que los conductores puedan reportar problemas y el gestor pueda revisarlos.                 | 5            | Alta      |
| 35 | US41          | Reporte de consumo de combustible        | Como desarrollador, quiero registrar el consumo de combustible para llevar el control por vehículo y por conductor.                                | 5            | Alta      |
| 36 | US42          | Historial de mantenimientos              | Como desarrollador, quiero listar los mantenimientos realizados a los vehículos con filtros.                                                     | 5            | Alta      |
| 37 | US43          | Exportación de reportes (Excel o PDF)    | Como desarrollador, quiero permitir la exportación de reportes en Excel o PDF para que los gestores puedan descargar los reportes generados.       | 5            | Alta      |
| 38 | US20          | Validación de datos de pausas            | Como desarrollador, quiero validar los datos de pausas ingresados por el conductor para asegurar que sean correctos.                              | 3            | Media     |
| 39 | US15          | Registro de combustible                   | Como conductor, quiero registrar el combustible cargado al vehículo, para llevar control del consumo.                                            | 5            | Alta      |
| 40 | US22          | Cambio de contraseña                     | Como conductor o gestor, quiero cambiar mi contraseña para mantener la seguridad de mi cuenta.                                                   | 2            | Baja      |
| 41 | US24          | Cambiar foto de perfil                   | Como conductor o gestor, quiero cambiar mi foto de perfil para personalizar mi cuenta.                                                           | 1            | Baja      |
| 42 | US25          | Solicitud de cambio de turno             | Como conductor, quiero solicitar un cambio de turno para organizar mejor mi jornada.                                                             | 2            | Baja      |
| 43 | US37          | Middleware de autenticación              | Como desarrollador, quiero validar el token JWT en endpoints protegidos, para asegurar que solo usuarios autorizados accedan.                    | 5            | Alta      | 


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

