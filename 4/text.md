## **UNIT IV**

---

# Strategic-Level Software Design

## 4.1. Strategic-Level Attribute-Driven Design

### 4.1.1. Design Purpose

<p align=justify> El propósito del sistema es desarrollar una aplicación web que facilite la interconexión entre empresas especializadas en diseño de interiores y potenciales clientes interesados en solicitar dichos servicios. Con este objetivo en mente, se ha concebido una aplicación que proporciona funcionalidades específicas para cumplir con esta finalidad.

### 4.1.2. Attribute-Driven Design Inputs

##### 4.1.2.1. Primary Functionality (Primary User Stories)

<p align=justify> En esta sección se especifica los Epics o User stories que tienen mayor relevancia en términos de requisitos funcionales y que tienen impacto sobre la arquitectura de la solución. La sección inicia con una introducción que resume los requisitos seleccionados y a continuación se detalla los mismos utilizando el siguiente cuadro.

| User Story ID | Título                                                       | Descripción                                                                                                                                                             | Criterios de Aceptación                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ------------- | ------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| US01          |<p align=justify> Visualizar las empresas de remodelación                      |<p align=justify> Como visitante, quiero ver un catálogo de empresas de remodelación disponibles en mi área.                                                                            | <p align=justify> **Escenario 1:** Verificación de la lista de empresas de remodelación disponibles <br>- El visitante visualiza una lista de 10 empresas de remodelación registradas disponibles. <br> **Escenario 2:** Verificación de la funcionalidad de búsqueda avanzada. <br>- El visitante puede aplicar una búsqueda avanzada y ver una lista de empresas de remodelación avanzada.                                                                                                                                                                         |
| US02          |<p align=justify> Registro en la aplicación                                    |<p align=justify> Como usuario, quiero crearme una cuenta para tener acceso a las funcionalidades y servicios del sitio web.                                                              |<p align=justify> **Escenario 1:** Usuario se registra exitosamente <br>- El usuario completa el registro con éxito y ve la página principal. <br> **Escenario 2:** Intento de registro de usuario fallido <br>- El usuario recibe un mensaje de error si hay un error en al menos uno de los campos.                                                                                                                                                                                                                                                                |
| US03          |<p align=justify> Acceso al perfil empresa                                     |<p align=justify> Como representante de la empresa, quiero crear un perfil empresa para acceder a funciones adicionales.                                                                |<p align=justify> **Escenario 1:** Crear un perfil empresa <br>- El representante paga el plan de suscripción seleccionado y ve su perfil de empresa. <br> **Escenario 2:** Intento fallido en la creación de perfil de empresa <br>- El representante recibe un mensaje de error de pago si el pago es rechazado.                                                                                                                                                                                                                                                   |
| US04          |<p align=justify> Publicación de proyectos realizados                          |<p align=justify> Como representante de la empresa, quiero publicar fotos y descripciones sobre proyectos realizados.                                                                  |<p align=justify> **Escenario 1:** La empresa sube sus proyectos pasados <br>- El representante publica fotos y descripciones de proyectos y ve un mensaje de éxito. <br> **Escenario 2:** Los proyectos de la empresa son visitados <br>- Otros usuarios pueden ver los proyectos publicados en el perfil de la empresa.                                                                                                                                                                                                                                            |
| US05          |<p align=justify> Envío de formulario de reclamo                               |<p align=justify> Como cliente, quiero subir un reclamo en línea si no estoy satisfecho con el servicio recibido.                                                                       |<p align=justify> **Escenario 1:** Formulario de reclamo enviado exitosamente <br>- El cliente completa y envía el formulario de reclamo con éxito. <br> **Escenario 2:** Error al enviar el formulario de reclamo <br>- El cliente recibe un mensaje de error si no completa todos los campos requeridos.                                                                                                                                                                                                                                                           |
| US06          |<p align=justify> Visualizar los comentarios de otros clientes                 |<p align=justify> Como cliente, quiero leer las reseñas que otros usuarios han publicado.                                                                                               |<p align=justify> **Escenario 1:** El cliente visualiza los comentarios de otros clientes <br>- El cliente puede ver una lista de comentarios sobre la empresa seleccionada. <br> **Escenario 2:** El cliente no visualiza los comentarios de otros clientes <br>- El cliente ve una lista de comentarios de la empresa seleccionada vacía con un mensaje.                                                                                                                                                                                                           |
| US07          |<p align=justify> Enviar una petición a una empresa                            |<p align=justify> Como cliente, quiero enviar una solicitud de servicio a una empresa para obtener servicios específicos que necesito.                                                    |<p align=justify> **Escenario 1:** Generando una solicitud de servicio a la empresa seleccionada <br>- El cliente completa el formulario de solicitud correctamente y lo envía con éxito. <br> **Escenario 2:** Fallo en la generación de solicitud de servicio a la empresa seleccionada <br>- El cliente recibe un mensaje de error si no completa correctamente el formulario. <br> **Escenario 3:** Opción de generar una solicitud de servicio a la empresa seleccionada bloqueada <br>- El visitante debe iniciar sesión antes de poder generar una solicitud. |
| US08          |<p align=justify> Poder recibir, aceptar o denegar los pedidos de mis clientes |<p align=justify> Como representante de la empresa, quiero recibir, aceptar o denegar las solicitudes de servicio de mis posibles clientes.                                             |<p align=justify> **Escenario 1:** Recibir solicitudes de servicio de remodelación <br>- El representante puede visualizar el detalle de las solicitudes de servicio recibidas. <br> **Escenario 2:** Aceptar solicitudes de servicio de remodelación <br>- El representante puede aceptar una solicitud y enviar una notificación. <br> **Escenario 3:** Denegar solicitudes de servicio de remodelación <br>- El representante puede denegar una solicitud y enviar una notificación.                                                                              |
| US09          |<p align=justify> Cambiar el estado del proceso de servicio                    |<p align=justify> Como representante de la empresa, quiero cambiar el estado del proceso del proyecto para informar al cliente el avance hasta su finalización del servicio.            |<p align=justify> **Escenario 1:** Cambio de estado de proyecto exitoso <br>- El representante puede cambiar el estado del proyecto y enviar una notificación. <br> **Escenario 2:** Cambio de estado de proyecto fallido <br>- El representante recibe un mensaje de error si no tiene autorización para modificar el estado.                                                                                                                                                                                                                                       |
| US10          |<p align=justify> Recibir las notificaciones de servicio                       |<p align=justify> Como empresa o cliente, quiero recibir notificaciones para estar al tanto del proceso del proyecto y alarmarme por cualquier inconveniente.                           |<p align=justify> **Escenario 1:** Ingresa a la sección notificaciones <br>- Los usuarios pueden ver una lista de notificaciones y sus detalles. <br> **Escenario 2:** Ingresa a la sección de notificaciones vacía <br>- Los usuarios pueden ver una lista vacía de notificaciones con un mensaje.                                                                                                                                                                                                                                                                  |
| US11          |<p align=justify> Tener una sección de favoritos de mis empresas               |<p align=justify> Como cliente, quiero poder seleccionar empresas y guardarlas como favoritas para acceder más rápido a ellas en el futuro.                                             |<p align=justify> **Escenario 1:** Guarda una empresa como favorito <br>- El cliente agrega una empresa como favorita y recibe un mensaje de agregado. <br> **Escenario 2:** Remueve a una empresa como favorito <br>- El cliente elimina una empresa de su lista de favoritos y recibe un mensaje de removido.                                                                                                                                                                                                                                                      |
| US12          |<p align=justify> Visualizar mis tarjetas de pagos                             |<p align=justify> Como usuario, quiero visualizar mis tarjetas de pago donde previamente realicé un pago con esa tarjeta.                                                               |<p align=justify> **Escenario 1:** Visualiza el método de pago anteriormente ingresado <br>- El usuario puede ver su método de pago registrado. <br> **Escenario 2:** No visualiza el método de pago anteriormente ingresado <br>- El usuario no tiene un método de pago registrado y ve un mensaje.                                                                                                                                                                                                                                                                 |
| US13          |<p align=justify> Filtro en la búsqueda de empresas                            |<p align=justify> Como cliente, quiero filtrar las empresas usando ciertos criterios en mi búsqueda para encontrar rápidamente las empresas que cumplan con mis requisitos específicos. |<p align=justify> **Escenario 1:** Se usa el filtro de búsqueda para encontrar a una empresa <br>- El cliente puede filtrar la búsqueda por criterios específicos. <br> **Escenario 2:** Modifica el filtro de búsqueda para encontrar a una empresa <br>- El cliente puede modificar el filtro y ver la lista actualizada de empresas.                                                                                                                                                                                                                              |
| US14          |<p align=justify> Poder editar mi perfil empresa                               |<p align=justify> Como representante de la empresa, quiero editar los datos de mi perfil para que me puedan contactar correctamente usando los datos actualizados..                      | **Escenario 1:** Editar la empresa publicada con datos válidos <br>- El representante edita su perfil con datos válidos y ve un mensaje de edición exitosa. <br> **Escenario 2:** Editar la empresa publicada con datos inválidos <br>- El representante recibe un mensaje de error si edita con datos inválidos.                                                                                                                                                                                                                                  |
| US15          |<p align=justify> Visualizar los detalles del proceso de servicio              |<p align=justify> Como cliente, quiero visualizar los detalles completos del proceso de servicio para conocer todos los aspectos del servicio...                                          |<p align=justify> **Escenario 1:** Revisa la propuesta <br>- El cliente puede revisar la propuesta y aprobarla.                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| US16          |<p align=justify> Calificar una empresa                                        |<p align=justify> Como cliente, quiero calificar a una empresa de remodelación al finalizar el proyecto en función a mi experiencia personal.                                           |<p align=justify> **Escenario 1:** Calificar un servicio <br>- El cliente puede calificar una empresa seleccionando una cantidad de estrellas.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| US17          |<p align=justify> Seleccionar el plan de suscripción                           |<p align=justify> Como usuario, quiero seleccionar un plan de suscripción que mejor se adapte de acuerdo con mis necesidades.                                                           |<p align=justify> **Escenario 1:** Ingresa correctamente su información de pago <br>- El usuario selecciona un plan de suscripción y completa los datos de pago correctamente. <br> **Escenario 2:** Ingresa incorrectamente su información de pago <br>- El usuario recibe un mensaje de error si ingresa incorrectamente los datos de pago.                                                                                                                                                                                                                        |
| US18          |<p align=justify> Modificar el plan de suscripción                             |<p align=justify> Como usuario, quiero modificar mi plan de suscripción para que se adecúe mejor a mis necesidades y presupuesto.                                                       |<p align=justify> **Escenario 1:** Selecciona un nuevo plan de suscripción <br>- El usuario cambia su plan de suscripción y recibe una notificación de confirmación. <br> **Escenario 2:** Selecciona el mismo plan de suscripción que tiene en el presente <br>- El usuario recibe un mensaje de que debe seleccionar otro plan si elige el mismo.                                                                                                                                                                                                                  |
| US19          |<p align=justify> Gestionar el plan de suscripción                             |<p align=justify> Como usuario quiero gestionar mi plan de suscripción para estar pendiente de este y las garantías que aún tengo disponibles.                                          |<p align=justify> **Escenario 1:** Ver plan de suscripción <br>- El usuario puede ver los detalles de su plan de suscripción y el historial de pagos. <br> **Escenario 2:** Información acerca de sus servicios técnicos <br>- El usuario puede ver información sobre los servicios técnicos recibidos y disponibles.                                                                                                                                                                                                                                                |
| US20          |<p align=justify> Gestionar los dispositivos SmartHome                         |<p align=justify> Como empresa quiero tener un registro y análisis de los dispositivos SmartHome instalados.                                                                            |<p align=justify> **Escenario 1:** Ingreso a la sección de tu progreso y te muestra los gráficos respectivos <br>- La empresa puede ver gráficos de crecimiento. <br> **Escenario 2:** Ingreso a la sección de tu progreso y no se ha tenido ningún progreso <br>- La empresa recibe un aviso de continuar usando la aplicación.                                                                                                                                                                                                                                     |
| US21          |<p align=justify> Sistema de programación de luces                             |<p align=justify> Como usuario, quiero poder programar horarios específicos para el encendido y apagado de las luces de mi espacio de trabajo...                                          |<p align=justify> **Escenario 1:** Configuración de horarios de encendido y apagado <br>- El usuario puede configurar horarios para las luces. <br> **Escenario 2:** Ejecución automática de horarios programados <br>- Las luces se encienden o apagan automáticamente según la programación.                                                                                                                                                                                                                                                                       |
| US22          |<p align=justify> Sistema de Luces                                             |<p align=justify> Como usuario, quiero controlar las luces de mi hogar de forma remota a través de una aplicación en mi teléfono.                                                       |<p align=justify> **Escenario 1:** Control remoto efectivo de las luces <br>- El usuario puede encender, apagar o ajustar la intensidad de las luces de su hogar de forma remota. <br> **Escenario 2:** Encendido remoto de luces antes de llegar a casa <br>- El usuario puede encender las luces antes de llegar a casa.                                                                                                                                                                                                                                           |
| US23          |<p align=justify> Generación Rápida de Propuestas                              |<p align=justify> Como empresa, quiero que la IA sugiera automáticamente materiales y colores adecuados para un proyecto de remodelación.                                               |<p align=justify> **Escenario 1:** Sugerencias precisas de materiales y colores <br>- La IA realiza sugerencias precisas basadas en las preferencias del cliente. <br> **Escenario 2:** Personalización de sugerencias basadas en las preferencias del cliente <br>- El empleado puede personalizar las sugerencias de la IA según las preferencias del cliente.                                                                                                                                                                                                     |
| US24          |<p align=justify> Propuestas de Remodelación Instantáneas                      |<p align=justify> Como usuario cliente, quiero una herramienta en línea que me ayude a crear una lista de deseos para mi proyecto.                                                      |<p align=justify> **Escenario 1:** Actualización automática de la propuesta al realizar cambios en la lista de deseos <br>- La IA actualiza automáticamente la propuesta al realizar cambios en la lista de deseos. <br> **Escenario 2:** Visualización clara de costos y alcance en la propuesta preliminar <br>- El cliente ve los costos y el alcance del proyecto en la propuesta preliminar de manera clara y comprensible.                                                                                                                                     |
| TS01          |<p align=justify> Recopilar información de los dispositivos Smart Home         |<p align=justify> Como desarrollador, quiero poder definir un esquema de datos para almacenar los datos recopilados de los dispositivos Smart Home.                                     |<p align=justify> **Escenario 1:** Acceso a los datos recopilados de los dispositivos Smart Home <br>- Los datos recopilados se almacenan en un esquema de datos coherente y se pueden acceder de manera efectiva. <br> **Escenario 2:** Almacenamiento de los datos recopilados de los dispositivos Smart Home <br>- Los datos recopilados se almacenan correctamente en la base de datos y se pueden recuperar con precisión.                                                                                                                                      |

              4.1.2.2. Quality attribute Scenarios

| Atributo          | Fuente                                           | Estímulo                                            | Artefacto                                      | Entorno                                               | Respuesta                                                         | Medida                                                                                               |
| ----------------- | ------------------------------------------------ | --------------------------------------------------- | ---------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Disponibilidad    | Usuarios o clientes                              | Intento de acceso al sistema                        | Sistema de software                            | Hardware y software subyacente                        | El sistema está disponible y responde a las solicitudes           | Tiempo en línea, porcentaje de tiempo disponible, tiempo de inactividad planificado o no planificado |
| Portabilidad      | Usuarios y equipos de desarrollo                 | Intento de ejecución en diferentes plataformas      | Software o aplicación                          | Diferentes sistemas operativos o entornos de hardware | El software se ejecuta correctamente en diferentes entornos       | Número de plataformas compatibles, problemas de compatibilidad reportados                            |
| Funcionalidad     | Requisitos del cliente                           | Acciones del usuario o eventos del sistema          | Funcionalidades y características del software | Contexto de uso                                       | El software realiza las funciones especificadas                   | Requisitos funcionales cumplidos, errores funcionales, casos de uso exitosos                         |
| Confiabilidad     | Usuarios y clientes                              | Uso normal o inusual del software                   | Sistema de software                            | Condiciones operativas                                | El software se comporta de manera predecible y sin errores graves | Tiempo promedio entre fallas, tasa de errores, disponibilidad                                        |
| Seguridad         | Usuarios y equipos de seguridad                  | Intentos de acceso no autorizado o amenazas         | Sistema de seguridad y software                | Redes y sistemas de comunicación                      | Protección de datos y recursos frente a amenazas                  | Nivel de vulnerabilidades, incidentes de seguridad, políticas de acceso                              |
| Usabilidad        | Usuarios y diseñadores de experiencia de usuario | Interacción del usuario con la interfaz             | Interfaz de usuario                            | Contexto de uso                                       | Facilidad de uso, satisfacción del usuario                        | Evaluaciones de usabilidad, encuestas de satisfacción del usuario, tasa de errores de usuario        |
| Modificabilidad   | Equipos de desarrollo y mantenimiento            | Cambios en los requisitos o actualizaciones         | Código fuente y diseño del software            | Entorno de desarrollo                                 | Capacidad para realizar cambios sin introducir errores            | Tiempo y costo de implementación de cambios, estabilidad del sistema                                 |
| Interoperabilidad | Usuarios y sistemas externos                     | Intercambio de datos o servicios con otros sistemas | Interfaces de comunicación y protocolos        | Sistemas externos con los que interactúa              | Capacidad para trabajar con otros sistemas de manera efectiva     | Grado de compatibilidad con estándares, éxito en la integración con sistemas externos                |
| Rendimiento       | Usuarios y requisitos de rendimiento             | Carga de trabajo o solicitudes de usuario           | Sistema de software y hardware                 | Recursos de hardware y red                            | Capacidad de respuesta y eficiencia del software bajo carga       | Tiempo de respuesta, throughput, utilización de recursos, capacidad de escalabilidad                 |

#### 4.1.2.3. Constraints
<table>
    <tr>
        <td colspan=5 align=center>Constraints</td>
    </tr>
    <tr>
        <td colspan=2 align=justify>Requerimiento de Suscripción</td>
        <td colspan=5 align=justify>Los usuarios empresariales deben pagar una suscripción para acceder a las funciones avanzadas de la aplicación, como la publicación de perfiles de empresa, la aceptación de solicitudes de remodelación y la visualización de proyectos pasados.</td>
    </tr>
    <tr>
        <td colspan=2 align=justify>Integración de Dispositivos Inteligentes</td>
        <td colspan=5 align=justify>Las empresas de remodelación deben ser capaces de integrar dispositivos inteligentes en los proyectos de remodelación que ofrecen. La plataforma debe ser compatible con una variedad de dispositivos y sistemas de automatización del hogar.</td>
    </tr>
    <tr>
        <td colspan=2 align=justify>Gestión de Proposals</td>
        <td colspan=5 align=justify>La aplicación debe permitir a las empresas de remodelación generar propuestas detalladas para los proyectos y rastrear el estado de esas propuestas (por ejemplo, pendiente, en proceso, cancelada o en espera).</td>
    </tr>
    <tr>
        <td colspan=2 align=justify>Elección de Remodelación</td>
        <td colspan=8 align=justify>Los clientes deben tener la opción de elegir entre una remodelación inteligente con dispositivos inteligentes o una remodelación tradicional sin estos dispositivos.</td>
    </tr>
    <tr>
        <td colspan=2 align=justify>Capacidad de Procesamiento</td>
        <td colspan=8 align=justify>La plataforma debe ser capaz de manejar un alto volumen de solicitudes de remodelación y propuestas simultáneas sin degradación significativa del rendimiento.</td>
    </tr>
    <tr>
        <td colspan=2 align=justify>Seguridad de Datos</td>
        <td colspan=8 align=justify>La seguridad de los datos personales de los usuarios debe ser una prioridad. Se deben implementar medidas de seguridad robustas para proteger la información confidencial.</td>
    </tr>
    <tr>
        <td colspan=2 align=justify>Compatibilidad Multiplataforma</td>
        <td colspan=8 align=justify>La aplicación debe ser accesible y funcional en varias plataformas, incluyendo dispositivos móviles (iOS y Android) y navegadores web, para asegurar la máxima accesibilidad para los usuarios.</td>
    </tr>
    <tr>
        <td colspan=2 align=justify>Soporte al Cliente</td>
        <td colspan=8 align=justify>Debe proporcionarse un mecanismo de soporte al cliente eficaz, como un centro de ayuda o servicio de atención al cliente, para abordar preguntas, problemas y solicitudes de asistencia de manera oportuna.</td>
    </tr>
</table>
### 4.1.3. Architectural Drivers Backlog
<table>
    <tr>
        <td colspan=2 align=center>Driver ID</td>
        <td colspan=2 align=center>Título de Driver</td>
        <td colspan=4 align=center>Descripción</td>
        <td colspan=3 align=center>Importancia para Stakeholders (High Medium, Low)</td>
        <td colspan=3 align=center>Impacto en Architecture Technical Complexity (High, Medium, Low)</td>
    </tr>
    <tr>
        <td colspan=2 align=center>ID-01</td>
        <td colspan=2 align=center>Requerimiento de Suscripción</td>
        <td colspan=4 align=justify>Este driver es fundamental ya que afecta la viabilidad del modelo de negocio. La arquitectura debe admitir la gestión de suscripciones de usuarios empresariales, incluyendo la facturación, la gestión de acceso a características avanzadas y la escalabilidad de la plataforma.</td>
        <td colspan=3 align=center>High</td>
        <td colspan=3 align=center>High</td>
    </tr>
    <tr>
        <td colspan=2 align=center>ID-02</td>
        <td colspan=2 align=center>Integración de Dispositivos Inteligentes</td>
        <td colspan=4 align=justify>Dado que la aplicación se centra en soluciones inteligentes para el hogar, esta integración es crítica. La arquitectura debe ser modular y escalable para permitir la incorporación de diferentes dispositivos y sistemas de automatización del hogar.</td>
        <td colspan=3 align=center>High</td>
        <td colspan=3 align=center>High</td>
    </tr>
    <tr>
        <td colspan=2 align=center>ID-03</td>
        <td colspan=2 align=center>Gestión de Proposals</td>
        <td colspan=4 align=justify>La gestión de propuestas es un componente central de la funcionalidad de ModelHouse. La arquitectura debe admitir la generación y seguimiento de propuestas, incluyendo estados como pendiente, en proceso, cancelada y en espera.</td>
        <td colspan=3 align=center>High</td>
        <td colspan=3 align=center>High</td>
    </tr>
    <tr>
        <td colspan=2 align=center>ID-04</td>
        <td colspan=2 align=center>Elección de Remodelación</td>
        <td colspan=4 align=justify>La capacidad de los clientes para elegir entre una remodelación inteligente o tradicional es un elemento clave de la experiencia del usuario. La arquitectura debe permitir escoger entre ambas opciones.</td>
        <td colspan=3 align=center>High</td>
        <td colspan=3 align=center>High</td>
    </tr>
    <tr>
        <td colspan=2 align=center>ID-05</td>
        <td colspan=2 align=center>Capacidad de Procesamiento</td>
        <td colspan=4 align=justify>Dada la posible carga de solicitudes y propuestas, la escalabilidad y el rendimiento de la arquitectura son esenciales. Debe garantizarse una alta capacidad de procesamiento y una baja latencia en las interacciones de la plataforma.</td>
        <td colspan=3 align=center>High</td>
        <td colspan=3 align=center>High</td>
    </tr>
    <tr>
        <td colspan=2 align=center>ID-06</td>
        <td colspan=2 align=center>Seguridad de Datos</td>
        <td colspan=4 align=justify>La seguridad de los datos es crucial para ganar la confianza de los usuarios. La arquitectura debe incluir medidas sólidas de seguridad de datos, incluyendo cifrado, autenticación y autorización adecuados, para proteger la información confidencial.</td>
        <td colspan=3 align=center>High</td>
        <td colspan=3 align=center>High</td>
    </tr>
    <tr>
        <td colspan=2 align=center>ID-07</td>
        <td colspan=2 align=center>Compatibilidad Multiplataforma</td>
        <td colspan=4 align=justify>Para llegar a un público amplio, la arquitectura debe ser compatible con múltiples plataformas, incluyendo dispositivos móviles y navegadores web. La adaptabilidad y la experiencia del usuario deben ser consistentes en todas las plataformas.</td>
        <td colspan=3 align=center>Medium</td>
        <td colspan=3 align=center>Medium</td>
    </tr>
    <tr>
        <td colspan=2 align=center>ID-08</td>
        <td colspan=2 align=center>Soporte al Cliente</td>
        <td colspan=4 align=justify>La provisión de soporte al cliente es importante para la satisfacción del usuario. La arquitectura debe permitir la implementación eficaz de un centro de ayuda o sistema de atención al cliente para abordar las necesidades y preguntas de los usuarios.</td>
        <td colspan=3 align=center>Medium</td>
        <td colspan=3 align=center>Medium</td>
    </tr>
</table>
### 4.1.4. Architectural Design Decisions
### 4.1.5. Quality Attribute Scenario Refinements
<table>
    <tr>
        <td colspan=8>Scenario Refinement for Scenario 1</td>
    <tr>
    <tr>
        <td colspan=4>Scenario(s):</td>
        <td colspan=4>Un usuario intenta acceder al sistema y el sistema está disponible.</td>
    </tr>
    <tr>
        <td colspan=4>Business Goals:</td>
        <td colspan=4>El sistema debe estar disponible para los usuarios cuando lo necesiten para que puedan realizar sus tareas.</td>
    </tr>
    <tr>
        <td colspan=4>Relevant Quality Attributes:</td>
        <td colspan=4>Disponibilidad</td>
    </tr>
    <tr>    
        <td colspan=2 rowspan=6>Scenario Components</td>
        <td colspan=2>Stimulus:</td>
        <td colspan=4>Usuarios o clientes</td>
    </tr>
    <tr>
        <td colspan=2>Stimulus Source:</td>
        <td colspan=4>Intento de acceso al sistema</td>
    </tr>
    <tr>
        <td colspan=2>Environment:</td>
        <td colspan=4>Sistema de software</td>
    </tr>
    <tr>
        <td colspan=2>Artifact (if Known)</td>
        <td colspan=4>Hardware y software subyacente</td>
    </tr>
    <tr>
        <td colspan=2>Response:</td>
        <td colspan=4>El sistema está disponible y responde a las solicitudes.</td>
    </tr>
    <tr>
        <td colspan=2>Response Measure:</td>
        <td colspan=4>Tiempo en línea, porcentaje de tiempo disponible, tiempo de inactividad planificado o no planificado</td>
    </tr>
    <tr>
        <td colspan=4>Questions:</td>
        <td colspan=4>¿El sistema está disponible el 99,9% del tiempo?</td>
    </tr>
    <tr>
        <td colspan=4>Issues:</td>
        <td colspan=4>¿El sistema responde a las solicitudes de los usuarios dentro de un tiempo razonable?</td>
    </tr>    
</table>

<table>
    <tr>
        <td colspan=8>Scenario Refinement for Scenario 2</td>
    <tr>
    <tr>
        <td colspan=4>Scenario(s):</td>
        <td colspan=4>Un usuario intenta ejecutar el software en una plataforma diferente y el software se ejecuta correctamente.</td>
    </tr>
    <tr>
        <td colspan=4>Business Goals:</td>
        <td colspan=4>El sistema debe poder ejecutarse en diferentes plataformas para que pueda ser utilizado por un público más amplio.</td>
    </tr>
    <tr>
        <td colspan=4>Relevant Quality Attributes:</td>
        <td colspan=4>Portabilidad</td>
    </tr>
    <tr>    
        <td colspan=2 rowspan=6>Scenario Components</td>
        <td colspan=2>Stimulus:</td>
        <td colspan=4>Usuarios y equipos de desarrollo</td>
    </tr>
    <tr>
        <td colspan=2>Stimulus Source:</td>
        <td colspan=4>Intento de ejecución en diferentes plataformas</td>
    </tr>
    <tr>
        <td colspan=2>Environment:</td>
        <td colspan=4>Software o aplicación</td>
    </tr>
    <tr>
        <td colspan=2>Artifact (if Known)</td>
        <td colspan=4>Diferentes sistemas operativos o entornos de hardware</td>
    </tr>
    <tr>
        <td colspan=2>Response:</td>
        <td colspan=4>El software se ejecuta correctamente en diferentes entornos.</td>
    </tr>
    <tr>
        <td colspan=2>Response Measure:</td>
        <td colspan=4>Número de plataformas compatibles, problemas de compatibilidad reportados</td>
    </tr>
    <tr>
        <td colspan=4>Questions:</td>
        <td colspan=4>¿El software es compatible con los sistemas operativos y entornos de hardware más comunes?</td>
    </tr>
    <tr>
        <td colspan=4>Issues:</td>
        <td colspan=4>¿El software se ejecuta sin problemas en diferentes entornos?</td>
    </tr>    
</table>

<table>
    <tr>
        <td colspan=8>Scenario Refinement for Scenario 3</td>
    <tr>
    <tr>
        <td colspan=4>Scenario(s):</td>
        <td colspan=4>Un usuario intenta realizar una tarea y el software realiza la tarea correctamente.</td>
    </tr>
    <tr>
        <td colspan=4>Business Goals:</td>
        <td colspan=4>El sistema debe cumplir con los requisitos funcionales para que los usuarios puedan realizar sus tareas de manera eficiente.</td>
    </tr>
    <tr>
        <td colspan=4>Relevant Quality Attributes:</td>
        <td colspan=4>Funcionalidad</td>
    </tr>
    <tr>    
        <td colspan=2 rowspan=6>Scenario Components</td>
        <td colspan=2>Stimulus:</td>
        <td colspan=4>Requisitos del cliente</td>
    </tr>
    <tr>
        <td colspan=2>Stimulus Source:</td>
        <td colspan=4>Acciones del usuario o eventos del sistema</td>
    </tr>
    <tr>
        <td colspan=2>Environment:</td>
        <td colspan=4>Funcionalidades y características del software</td>
    </tr>
    <tr>
        <td colspan=2>Artifact (if Known)</td>
        <td colspan=4>Contexto de uso</td>
    </tr>
    <tr>
        <td colspan=2>Response:</td>
        <td colspan=4>El software realiza las funciones especificadas.</td>
    </tr>
    <tr>
        <td colspan=2>Response Measure:</td>
        <td colspan=4>Requisitos funcionales cumplidos, errores funcionales, casos de uso exitosos</td>
    </tr>
    <tr>
        <td colspan=4>Questions:</td>
        <td colspan=4>¿El software cumple con todos los requisitos funcionales?</td>
    </tr>
    <tr>
        <td colspan=4>Issues:</td>
        <td colspan=4>¿El software realiza todas las tareas esperadas por los usuarios?</td>
    </tr>    
</table>

<table>
    <tr>
        <td colspan=8>Scenario Refinement for Scenario 4</td>
    <tr>
    <tr>
        <td colspan=4>Scenario(s):</td>
        <td colspan=4>Un usuario intenta usar el software y el software funciona correctamente.</td>
    </tr>
    <tr>
        <td colspan=4>Business Goals:</td>
        <td colspan=4>El sistema debe ser estable y libre de errores para que los usuarios puedan confiar en él.</td>
    </tr>
    <tr>
        <td colspan=4>Relevant Quality Attributes:</td>
        <td colspan=4>Confiabilidad</td>
    </tr>
    <tr>    
        <td colspan=2 rowspan=6>Scenario Components</td>
        <td colspan=2>Stimulus:</td>
        <td colspan=4>Usuarios y clientes</td>
    </tr>
    <tr>
        <td colspan=2>Stimulus Source:</td>
        <td colspan=4>Uso normal o inusual del software</td>
    </tr>
    <tr>
        <td colspan=2>Environment:</td>
        <td colspan=4>Sistema de software</td>
    </tr>
    <tr>
        <td colspan=2>Artifact (if Known)</td>
        <td colspan=4>Condiciones operativas</td>
    </tr>
    <tr>
        <td colspan=2>Response:</td>
        <td colspan=4>El software se comporta de manera predecible y sin errores graves.</td>
    </tr>
    <tr>
        <td colspan=2>Response Measure:</td>
        <td colspan=4>Tiempo promedio entre fallas, tasa de errores, disponibilidad</td>
    </tr>
    <tr>
        <td colspan=4>Questions:</td>
        <td colspan=4>¿El software es confiable en uso normal?</td>
    </tr>
    <tr>
        <td colspan=4>Issues:</td>
        <td colspan=4>¿El software puede soportar el uso inusual?</td>
    </tr>    
</table>

<table>
    <tr>
        <td colspan=8>Scenario Refinement for Scenario 5</td>
    <tr>
    <tr>
        <td colspan=4>Scenario(s):</td>
        <td colspan=4>Un usuario intenta acceder al sistema de forma no autorizada y el sistema se protege contra el acceso no autorizado.</td>
    </tr>
    <tr>
        <td colspan=4>Business Goals:</td>
        <td colspan=4>El sistema debe proteger los datos y recursos del sistema de amenazas para que los usuarios puedan sentirse seguros al usarlo.</td>
    </tr>
    <tr>
        <td colspan=4>Relevant Quality Attributes:</td>
        <td colspan=4>Seguridad</td>
    </tr>
    <tr>    
        <td colspan=2 rowspan=6>Scenario Components</td>
        <td colspan=2>Stimulus:</td>
        <td colspan=4>Usuarios y equipos de seguridad</td>
    </tr>
    <tr>
        <td colspan=2>Stimulus Source:</td>
        <td colspan=4>Intentos de acceso no autorizado o amenazas</td>
    </tr>
    <tr>
        <td colspan=2>Environment:</td>
        <td colspan=4>Sistema de seguridad y software</td>
    </tr>
    <tr>
        <td colspan=2>Artifact (if Known)</td>
        <td colspan=4>Redes y sistemas de comunicación</td>
    </tr>
    <tr>
        <td colspan=2>Response:</td>
        <td colspan=4>Protección de datos y recursos frente a amenazas.</td>
    </tr>
    <tr>
        <td colspan=2>Response Measure:</td>
        <td colspan=4>Nivel de vulnerabilidades, incidentes de seguridad, políticas de acceso</td>
    </tr>
    <tr>
        <td colspan=4>Questions:</td>
        <td colspan=4>¿El sistema está protegido contra ataques externos?</td>
    </tr>
    <tr>
        <td colspan=4>Issues:</td>
        <td colspan=4>¿Los datos y recursos del sistema están seguros?</td>
    </tr>    
</table>

<table>
    <tr>
        <td colspan=8>Scenario Refinement for Scenario 6</td>
    <tr>
    <tr>
        <td colspan=4>Scenario(s):</td>
        <td colspan=4>Un usuario intenta usar la interfaz de usuario y la interfaz de usuario es fácil de usar.</td>
    </tr>
    <tr>
        <td colspan=4>Business Goals:</td>
        <td colspan=4>La interfaz de usuario debe ser fácil de aprender y usar para que los usuarios puedan interactuar con el sistema de manera eficiente.</td>
    </tr>
    <tr>
        <td colspan=4>Relevant Quality Attributes:</td>
        <td colspan=4>Usabilidad</td>
    </tr>
    <tr>    
        <td colspan=2 rowspan=6>Scenario Components</td>
        <td colspan=2>Stimulus:</td>
        <td colspan=4>Usuarios y diseñadores de experiencia de usuario</td>
    </tr>
    <tr>
        <td colspan=2>Stimulus Source:</td>
        <td colspan=4>Interacción del usuario con la interfaz</td>
    </tr>
    <tr>
        <td colspan=2>Environment:</td>
        <td colspan=4>Interfaz de usuario</td>
    </tr>
    <tr>
        <td colspan=2>Artifact (if Known)</td>
        <td colspan=4>Contexto de uso</td>
    </tr>
    <tr>
        <td colspan=2>Response:</td>
        <td colspan=4>Facilidad de uso, satisfacción del usuario</td>
    </tr>
    <tr>
        <td colspan=2>Response Measure:</td>
        <td colspan=4>Evaluaciones de usabilidad, encuestas de satisfacción del usuario, tasa de errores de usuario</td>
    </tr>
    <tr>
        <td colspan=4>Questions:</td>
        <td colspan=4>¿La interfaz de usuario es fácil de usar?</td>
    </tr>
    <tr>
        <td colspan=4>Issues:</td>
        <td colspan=4>¿Los usuarios están satisfechos con la interfaz de usuario?</td>
    </tr>    
</table>

<table>
    <tr>
        <td colspan=8>Scenario Refinement for Scenario 7</td>
    <tr>
    <tr>
        <td colspan=4>Scenario(s):</td>
        <td colspan=4>Un equipo de desarrollo necesita cambiar el software y el software es fácil de modificar.</td>
    </tr>
    <tr>
        <td colspan=4>Business Goals:</td>
        <td colspan=4>El sistema debe ser fácil de cambiar para adaptarse a los nuevos requisitos para que pueda mantenerse actualizado y relevante.</td>
    </tr>
    <tr>
        <td colspan=4>Relevant Quality Attributes:</td>
        <td colspan=4>Modificabilidad</td>
    </tr>
    <tr>    
        <td colspan=2 rowspan=6>Scenario Components</td>
        <td colspan=2>Stimulus:</td>
        <td colspan=4>Usuarios o clientes</td>
    </tr>
    <tr>
        <td colspan=2>Stimulus Source:</td>
        <td colspan=4>Intento de acceso al sistema</td>
    </tr>
    <tr>
        <td colspan=2>Environment:</td>
        <td colspan=4>Sistema de software</td>
    </tr>
    <tr>
        <td colspan=2>Artifact (if Known)</td>
        <td colspan=4>Hardware y software subyacente</td>
    </tr>
    <tr>
        <td colspan=2>Response:</td>
        <td colspan=4>El sistema está disponible y responde a las solicitudes.</td>
    </tr>
    <tr>
        <td colspan=2>Response Measure:</td>
        <td colspan=4>Tiempo en línea, porcentaje de tiempo disponible, tiempo de inactividad planificado o no planificado</td>
    </tr>
    <tr>
        <td colspan=4>Questions:</td>
        <td colspan=4>¿El sistema está disponible el 99,9% del tiempo?</td>
    </tr>
    <tr>
        <td colspan=4>Issues:</td>
        <td colspan=4>¿El sistema responde a las solicitudes de los usuarios dentro de un tiempo razonable?</td>
    </tr>    
</table>

<table>
    <tr>
        <td colspan=8>Scenario Refinement for Scenario 8</td>
    <tr>
    <tr>
        <td colspan=4>Scenario(s):</td>
        <td colspan=4>Un equipo de desarrollo necesita realizar un cambio en el software y el software es fácil de modificar.</td>
    </tr>
    <tr>
        <td colspan=4>Business Goals:</td>
        <td colspan=4>El sistema debe ser fácil de modificar para que los equipos de desarrollo puedan realizar cambios de manera rápida y eficiente.</td>
    </tr>
    <tr>
        <td colspan=4>Relevant Quality Attributes:</td>
        <td colspan=4>Disponibilidad</td>
    </tr>
    <tr>    
        <td colspan=2 rowspan=6>Scenario Components</td>
        <td colspan=2>Stimulus:</td>
        <td colspan=4>Equipos de desarrollo y mantenimiento</td>
    </tr>
    <tr>
        <td colspan=2>Stimulus Source:</td>
        <td colspan=4>Cambios en los requisitos o actualizaciones</td>
    </tr>
    <tr>
        <td colspan=2>Environment:</td>
        <td colspan=4>Código fuente y diseño del software</td>
    </tr>
    <tr>
        <td colspan=2>Artifact (if Known)</td>
        <td colspan=4>Entorno de desarrollo</td>
    </tr>
    <tr>
        <td colspan=2>Response:</td>
        <td colspan=4>Capacidad para realizar cambios sin introducir errores</td>
    </tr>
    <tr>
        <td colspan=2>Response Measure:</td>
        <td colspan=4>Tiempo y costo de implementación de cambios, estabilidad del sistema</td>
    </tr>
    <tr>
        <td colspan=4>Questions:</td>
        <td colspan=4>¿El software es fácil de modificar?</td>
    </tr>
    <tr>
        <td colspan=4>Issues:</td>
        <td colspan=4>¿Los cambios al software son propensos a introducir errores?</td>
    </tr>    
</table>

<table>
    <tr>
        <td colspan=8>Scenario Refinement for Scenario 9</td>
    <tr>
    <tr>
        <td colspan=4>Scenario(s):</td>
        <td colspan=4>Un usuario intenta intercambiar datos o servicios con otro sistema y el software es capaz de hacerlo de manera efectiva.</td>
    </tr>
    <tr>
        <td colspan=4>Business Goals:</td>
        <td colspan=4>El sistema debe ser capaz de interactuar con otros sistemas de manera efectiva para que los usuarios puedan realizar sus tareas.</td>
    </tr>
    <tr>
        <td colspan=4>Relevant Quality Attributes:</td>
        <td colspan=4>Interoperabilidad</td>
    </tr>
    <tr>    
        <td colspan=2 rowspan=6>Scenario Components</td>
        <td colspan=2>Stimulus:</td>
        <td colspan=4>Usuarios y sistemas externos</td>
    </tr>
    <tr>
        <td colspan=2>Stimulus Source:</td>
        <td colspan=4>Intercambio de datos o servicios con otros sistemas</td>
    </tr>
    <tr>
        <td colspan=2>Environment:</td>
        <td colspan=4>Interfaces de comunicación y protocolos</td>
    </tr>
    <tr>
        <td colspan=2>Artifact (if Known)</td>
        <td colspan=4>Sistemas externos con los que interactúa</td>
    </tr>
    <tr>
        <td colspan=2>Response:</td>
        <td colspan=4>Capacidad para trabajar con otros sistemas de manera efectiva</td>
    </tr>
    <tr>
        <td colspan=2>Response Measure:</td>
        <td colspan=4>Grado de compatibilidad con estándares, éxito en la integración con sistemas externos</td>
    </tr>
    <tr>
        <td colspan=4>Questions:</td>
        <td colspan=4>¿El software puede interactuar con otros sistemas de manera efectiva?</td>
    </tr>
    <tr>
        <td colspan=4>Issues:</td>
        <td colspan=4>¿El software requiere una integración compleja con otros sistemas?</td>
    </tr>    
</table>

## 4.2 Strategic Level Domain Driver Design
### 4.2.1 EventStorming
Se identificaron los eventos y bounded context correspondientes al realizar el proceso del ventStorming
    <center>
            <img src="../images/EventStorming.png">
    </center>
### 4.2.2 Candidate Context Discovery
Al realizar el proceso de EventStorming se identificaron 11 Bounded Context. Siendo "Request Service Management" el core de negocio encontrado.

![Candidate_Context_Discovery_A](../images/Candidate_Context_Discovery_A.png)
![Candidate_Context_Discovery_B](../images/Candidate_Context_Discovery_B.png)
![Candidate_Context_Discovery_C](../images/Candidate_Context_Discovery_C.png)
![Candidate_Context_Discovery_D](../images/Candidate_Context_Discovery_D.png)

### 4.2.3 Domain Message Flows Modeling
Se identificaron los pasos o actividades que los usuarios tendrán que realizar al encontrarse con los escenarios propuestos al navegar por la aplicación.
![Domain_Message_Flows_Modeling_1](../images/Domain_Message_Flows_Modeling_1.png)
![Domain_Message_Flows_Modeling_2](../images/Domain_Message_Flows_Modeling_2.png)
![Domain_Message_Flows_Modeling_3](../images/Domain_Message_Flows_Modeling_3.png)
![Domain_Message_Flows_Modeling_4](../images/Domain_Message_Flows_Modeling_4.png)
### 4.2.4 Bounded Context Canvases
Se realizaron los siguientes canvases:
![canvas1](../images/canvas-1.png)
![canvas2](../images/canvas-2.png)
![canvas3](../images/canvas-3.png)
![canvas4](../images/canvas-4.png)
![canvas5](../images/canvas-5.png)
### 4.2.5 Context Mapping
El context mapping que se ha creado es el siguiente:
![canvas1](../images/context-mapping.png)

## 4.3 Software Architecture

### 4.3.1. Software Architecture System Landscape Diagram.

![Alt text](../images/structurizr-81539-LandScape.png "Landscape Level Diagrams")

### 4.3.2. Software Architecture Context Level Diagrams.

![Alt text](../images/structurizr-81539-Context.png "Context Level Diagrams")

### 4.3.3. Software Architecture Container Level Diagrams.

![Alt text](../images/structurizr-81539-Container.png "Container Level Diagrams")

### 4.3.4. Software Architecture Deployment Diagrams.

![Alt text](../images/deployment-diagram.png "Deployment Diagram")


