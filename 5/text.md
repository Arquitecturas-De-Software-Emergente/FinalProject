## **UNIT V**

---

### Tactical-Level Software Design.

#### 5.1. Bounded Context: Subscription and payment

##### 5.1.1. Domain Layer

<div align = justify>

<p><b>Entidades de dominio</b></p>

<li>
    <b>Subscriptions: </b>Representa una suscripción sobre un plan de suscripción
</li>

<li>
    <b>Payments: </b>Representa un pago realizado por un usuario para una suscripción.
</li>

<li>
    <b>Plans: </b>Representa un plan de suscripción disponible para los usuarios.
</li> <br>

<p><b>Objetos de valor</b></p>

<li>
    <b>Stripe: </b>Representa un objeto de valor que contiene información sobre un pago realizado a través de Stripe.
</li> <br>

<p><b>Repositorios</b></p>

<li>
    <b>SubscriptionRepository: </b>Maneja la persistencia de las suscripciones.
</li>

<li>
    <b>Servicios de dominio</b>
</li>

<li>
    <b>PaymentRepository: </b>Maneja la persistencia de los pagos.
</li>

<li>
    <b>PlanRepository: </b>Maneja la persistencia de los planes de suscripción.
</li> <br>

</div>

##### 5.1.2. Interface Layer

<div align=justify>


<li>
    <b>PlansController: </b> Esta clase gestiona la configuración y visualización de los planes de suscripción disponibles en el sistema. Permite a los usuarios seleccionar, ver detalles y administrar la información de facturación y ciclos de pago asociados a los planes de suscripción.
</li> <br>

<li>
    <b>PaymentsController: </b>Este controlador se encarga de gestionar las operaciones relacionadas con los pagos realizados por los usuarios para suscripciones.
</li> <br>

<li>
    <b>SubscriptionsController: </b>Esta clase se encarga de gestionar las suscripciones de los usuarios. Permite a los usuarios ver sus suscripciones activas, actualizar la información de pago asociada a sus suscripciones y gestionar renovaciones automáticas o cancelaciones de suscripciones.
</li> <br>

</div>

##### 5.1.3. Application Layer

<div align = justify>

<p>En el contexto de "Subscription and Payment" en ModelHouse, el Application Layer se centra en proporcionar una interfaz de usuario empresarial y una funcionalidad de gestión de suscripciones. Permite a las empresas de remodelación suscribirse al servicio y gestionar sus pagos de manera eficiente. Los usuarios empresariales pueden crear y cancelar suscripciones a través de esta interfaz, y el Application Layer se comunica con la API de Stripe para garantizar la facturación adecuada. Además, se generan notificaciones y eventos para mantener a los usuarios informados sobre el estado de sus suscripciones.</p>

<p>
    <b>Command Handlers:</b><br>
    <li>
        <b>CreateSubscriptionCommandHandler: </b>Este Command Handler se encarga de procesar la creación de una nueva suscripción de usuario empresarial en ModelHouse. Cuando se recibe un comando para crear una suscripción, este componente interactúa con la API de Stripe para configurar el pago y, una vez confirmado, actualiza el estado de la suscripción en la base de datos.
    </li>
    <li>
        <b>CancelSubscriptionCommandHandler: </b>El Command Handler de cancelación de suscripciones se encarga de procesar las solicitudes de cancelación de suscripciones por parte de los usuarios empresariales. Trabaja en conjunto con la API de Stripe para detener los pagos recurrentes y actualiza el estado de la suscripción correspondiente.
    </li><br>
    <b>Event Handlers: </b><br><br>
    <li>
        <b>PaymentConfirmedEventHandler: </b>Este Event Handler responde a eventos que confirman el pago exitoso de una suscripción. Cuando se recibe un evento de pago confirmado, este componente actualiza el estado de la suscripción en la base de datos y genera eventos adicionales relacionados con la facturación y la gestión de suscripciones.
    </li>
    <li>
        <b>SubscriptionCancelledEventHandler: </b>El Event Handler de cancelación de suscripciones maneja eventos que indican que una suscripción ha sido cancelada. Cuando se recibe un evento de este tipo, se actualiza el estado de la suscripción en la base de datos y se emiten eventos de notificación correspondientes a los usuarios.
    </li>  <br>
</p>

</div>

##### 5.1.4. Infrastructure Layer

<div align = justify>

<p>Dentro de esta capa definimos principalmente los esquemas de las entidades de la capa de dominio para un correcto manejo de la base de datos.</p>

<p>
    <b>Integración con Proveedores de Pagos Externos: </b>Se establecerán conexiones y se implementarán adaptadores para interactuar con proveedores de servicios de pago externos, como PayPal, Visa, o cualquier otro sistema de pago utilizado por la empresa. Esto podría incluir la configuración de API, el manejo de tokens de seguridad, la gestión de transacciones y la conciliación de pagos.
</p>

<p>
    <b>Gestión de Bases de Datos: </b>Incluirá la configuración y gestión de la base de datos relacionadas con las suscripciones y pagos. Esto abarca la creación de tablas de base de datos, la implementación de almacenamiento en caché para mejorar el rendimiento y la gestión de copias de seguridad de datos sensibles.
</p>

<p>
    <b>Seguridad: </b>Esta capa se encargará de la seguridad relacionada con las transacciones de pago. Esto podría incluir la implementación de medidas de seguridad como SSL/TLS para cifrar las comunicaciones, la gestión de tokens de seguridad y la detección de fraudes.
</p>

</div>

##### 5.1.5. Bounded Context Software Architecture Component Level Diagrams
    
<center>
              <img src="../images/structurizr-86418-Subscription and Payment Component Diagram.png">
    </center>

##### 5.1.6. Bounded Context Software Architecture Code Level Diagrams

###### 5.1.6.1. Bounded Context Domain Layer Class Diagrams

<center>
              <img src="../images/payment and subscription class.png">
    </center>

###### 5.1.6.2. Bounded Context Database Design Diagram

<center>
              <img src="../images/payment db.png">
    </center>


#### 5.2. Bounded Context: Identity Access Management

##### 5.2.1. Domain Layer

<p><b>Entidades de dominio</b></p>

<li>
    <b>Account: </b>Representa una cuenta de usuario en el sistema.
</li>

<li>
    <b>UserProfile: </b>Representa un perfil de usuario en el sistema.
</li>

<li>
    <b>BusinessProfile: </b>Representa un perfil empresarial en el sistema proporcionado a rais de una suscripción.
</li>

<li>
    <b>Projects: </b>Representa un proyecto creado a partir de la conclusion de un servicio de proyecto.
</li> <br>

<p><b>Agregados</b></p>

<li>
    <b>Autenticador: </b>Maneja la autenticación de los usuarios, verificando sus credenciales y emitiendo tokens de acceso.
</li>

<li>
    <b>Autorizador: </b>Maneja la autorización de los usuarios, verificando que tienen los permisos necesarios para realizar una acción en
</li> <br>

<p><b>Repositorios</b></p>

<li>
    <b>AccountRepository: </b>Maneja la persistencia de las cuentas de usuario.
</li>

<li>
    <b>Servicios de dominio</b>
</li>

<li>
    <b>UserProfileRepository: </b>Maneja la persistencia de los perfiles de usuario.
</li>

<li>
    <b>BusinessProfileRepository: </b>Maneja la persistencia de los perfiles empresariales.
</li>

<li>
    <b>ProjectsRepository: </b>Maneja la persistencia de los proyectos realizados.
</li> <br>

##### 5.2.2. Interface Layer

<div align=justify>

<li>
    <b>AccountController: </b>El AccountController maneja las operaciones relacionadas con la gestión de cuentas de usuario, como la creación de cuentas, la autenticación y el cierre de sesiones.
</li> <br>

<li>
    <b>BusinessProfileController: </b>Esta clase se encarga de gestionar los perfiles empresariales en el contexto de Identity Access Management, lo que incluye crear y actualizar perfiles empresariales y definir roles y permisos relacionados con la empresa.
</li> <br>

<li>
    <b>ProjectController: </b>El ProjectController gestiona las operaciones relacionadas con la gestión de proyectos dentro del contexto de Identity Access Management, permitiendo a los usuarios crear, editar y administrar proyectos.
</li> <br>

<li>
    <b>UserController: </b>Esta clase maneja las operaciones de gestión de usuarios, incluyendo el registro, autenticación, actualización de perfiles y eliminación de cuentas.
</li> <br>

<li>
    <b>UserProfileController: </b>El UserProfileController está encargado de las operaciones específicas relacionadas con los perfiles de usuario, como la actualización de la información personal del usuario.
</li> <br>

</div>

##### 5.2.3. Application Layer

<p>En el contexto de "Identity Access Management," el Application Layer se enfoca en la autenticación y la autorización de usuarios. Proporciona una interfaz de inicio de sesión y registro para los usuarios, donde pueden ingresar sus credenciales de manera segura. El Application Layer verifica la identidad de los usuarios y garantiza que tengan acceso solo a las funciones y los datos apropiados según sus permisos. Además, se gestionan eventos relacionados con la autenticación, como el inicio de sesión exitoso, para proporcionar una experiencia segura y efectiva.</p>

<div align = justify>

<p><b>Command Handlers:</b></p>

<li>
    <b>RegisterUserCommandHandler: </b>Procesa la creación de nuevas cuentas de usuario en ModelHouse. Cuando un usuario se registra, este componente crea una cuenta y gestiona las credenciales asociadas.
</li>
<li>
    <b>AuthenticateUserCommandHandler: </b>Se encarga de verificar las credenciales de inicio de sesión de los usuarios. Permite el acceso a las funciones de la aplicación después de una autenticación exitosa.
</li> <br>
<p><b>Event Handlers:</b></p>
<li>
    <b>UserLoggedInEventHandler: </b>Responde a eventos que indican un inicio de sesión exitoso por parte de un usuario. Actualiza el estado de la sesión del usuario y genera eventos adicionales relacionados con la autenticación.
</li>
<li>
    <b>PermissionsUpdatedEventHandler: </b>Maneja eventos que indican cambios en los permisos de usuario. Cuando se producen cambios en los permisos, este componente actualiza el estado de la autorización y emite eventos de seguridad correspondientes.
</li> <br>

</div>

##### 5.2.4. Infrastructure Layer

<div align = justify>

<p>
    <b>Integración con Proveedores de Correo Electrónico Externos: </b>Se establecerán conexiones y se implementarán adaptadores para interactuar con proveedores de servicios de correo electrónico externos, como Gmail, Outlook o proveedores de autenticación por correo electrónico. Esto incluye la configuración de la API, la gestión de tokens de autenticación y la interacción con los servicios de envío y recepción de correos electrónicos.
</p>

</div>

##### 5.2.5. Bounded Context Software Architecture Component Level Diagrams
<center>
            <img src="../images/structurizr-86418-Identity and Access Management Component.png">
    </center>

##### 5.2.6. Bounded Context Software Architecture Code Level Diagrams



###### 5.2.6.1. Bounded Context Domain Layer Class Diagrams

<center>
            <img src="../images/Indentity mangemente class.png">
    </center>

###### 5.2.6.2. Bounded Context Database Design Diagram

<center>
            <img src="../images/identity management db.png">
    </center>


#### 5.3. Bounded Context: Request Service Management

##### 5.3.1. Domain Layer

<div align = justify>

<p><b>Entidades de dominio</b></p>

<li>
    <b>Request: </b>Representa una solicitud de servicio de remodelación.
</li>

<li>
    <b>Notification: </b>Representa una notificación enviada tras relizarse alguna interacción den solicitud, propuesta o servicio de proyecto.
</li>

<li>
    <b>Reviews: </b>Representa una reseña realizada por un usuario sobre un servicio de proyecto.
</li>

<li>
    <b>Proposals: </b>Representa una propuesta realizada por una empresa de servicios sobre una solicitud de servicio.
</li>

<li>
    <b>ServiceProject: </b>Representa un servicio de proyecto realizado por una empresa de servicios.
</li>

<li>
    <b>ProjectResource: </b>Representa un recurso o activo utilizado en un servicio de proyecto.
</li>

<li>
    <b>ProjectActivity: </b>Representa una actividad realizada en un servicio de proyecto.
</li> <br>

<p><b>Repositorios</b></p>

<li>
    <b>RequestsRepository: </b>Maneja la persistencia de las suscripciones.
</li>

<li>
    <b>Servicios de dominio</b>
</li>

<li>
    <b>NotificationRepository: </b>Maneja la persistencia de los pagos.
</li>

<li>
    <b>ReviewsRepository: </b>Maneja la persistencia de los planes de suscripción.
</li>

<li>
    <b>ProposalsRepository: </b>Maneja la persistencia de las suscripciones.
</li>

<li>
    <b>ServiceProjectRepository</b>
</li>

<li>
    <b>ProjectResourceRepository: </b>Maneja la persistencia de los pagos.
</li>

<li>
    <b>ProjectActivityRepository: </b>Maneja la persistencia de los planes de suscripción.
</li> <br>

</div>

##### 5.3.2. Interface Layer

<div align=justify> 

<li> 
    <b>NotificationController: </b>Este controlador se encarga de la gestión de notificaciones, incluyendo la creación de nuevas notificaciones, la visualización de notificaciones para un usuario específico y la marcación de notificaciones como leídas.
</li> <br>

<li> 
    <b>ReviewController : </b> El controlador de reseñas podría manejar las operaciones relacionadas con la reseña de usuarios sobre servicios de proyecto. Esto incluiría la creación de la reseña y la obtención de reseña existente.
</li> <br>

<li> 
    <b>ServiceProjectController : </b> Este controlador gestiona las operaciones relacionadas con los servicios de proyecto realizados por empresas de servicios. Esto podría incluir la creación de nuevos servicios de proyecto, la gestión de tareas y plazos.
</li> <br>

<li> 
    <b>ProjectResourceController: </b> El controlador de recursos de proyecto maneja las operaciones relacionadas con los activos o recursos utilizados en un servicio de proyecto, como la asignación de recursos a proyectos específicos y la gestión de inventario.
</li> <br>

<li> 
    <b>ProposalController: </b>Esta clase gestiona las propuestas relacionadas con proyectos o servicios, incluyendo la creación, revisión y aceptación de propuestas.
</li> <br>

<li> 
    <b>RequestController: </b>El RequestController maneja las solicitudes de servicio o proyectos, permitiendo a los usuarios crear solicitudes, realizar seguimiento y recibir respuestas de proveedores de servicios.
</li> <br>

<li>
    <b>ProjectActivityController: </b> Este controlador se encarga de las operaciones relacionadas con las actividades realizadas en un servicio de proyecto. Podría permitir la creación y programación de actividades, así como el seguimiento y la actualización del estado de las mismas.
</div>

##### 5.3.3. Application Layer

<div align =justify>

<p>Dentro del contexto de "Request Service Management," el Application Layer ofrece una interfaz para que los usuarios creen solicitudes de remodelación y realicen un seguimiento de su progreso. Los usuarios pueden enviar solicitudes y consultar el estado de las mismas a través de esta interfaz. Además, el Application Layer permite a las empresas de remodelación gestionar las solicitudes recibidas y responder a ellas. Se generan eventos y notificaciones en tiempo real para mantener a los usuarios actualizados sobre el estado de sus solicitudes.</p>

<p><b>Command Handlers:</b></p>

<li>
    <b>CreateRemodelingRequestCommandHandler: </b>Se encarga de procesar la creación de nuevas solicitudes de remodelación enviadas por los usuarios. Asigna la solicitud a una empresa de remodelación y actualiza el estado de la solicitud correspondiente.
</li>
<li>
    <b>UpdateRequestStatusCommandHandler: </b>Maneja comandos para modificar el estado de una solicitud específica. Permite que los usuarios actualicen el estado de sus solicitudes de remodelación.
</li> <br>

<p><b>Event Handlers: </b></p>

<li>
    <b>RequestCreatedEventHandler: </b>Responde a eventos que indican la creación de una nueva solicitud de remodelación. Notifica a los usuarios interesados y actualiza el estado de la solicitud en la base de datos.
</li>
<li>
    <b>RequestStatusUpdatedEventHandler: </b>Maneja eventos relacionados con cambios en el estado de una solicitud. Proporciona notificaciones en tiempo real a los usuarios y emite eventos de seguimiento para mantenerlos informados.
</li> <br>

</div>

##### 5.3.4. Infrastructure Layer

<div align = justify>

<p>
    <b>Almacenamiento de Datos: </b>Para mantener un registro de las interacciones entre las empresas y usuarios se va a incluir un sistema de almacenamiento de datos que registre los eventos, las conversaciones y cualquier información relevante para el servicio contratado. Esto es útil para fines de seguimiento y análisis.
</p>

</div>

##### 5.3.5. Bounded Context Software Architecture Component Level Diagrams
<center>
            <img src="../images/structurizr-86418-Service Management Component Diagram.png">
    </center>

##### 5.3.6. Bounded Context Software Architecture Code Level Diagrams

###### 5.3.6.1. Bounded Context Domain Layer Class Diagrams

<center>
            <img src="../images/service management class.png">
    </center>

###### 5.3.6.2. Bounded Context Database Design Diagram

<center>
            <img src="../images/service Management db.png">
    </center>

#### 5.4. Bounded Context: Smart Home Project Management

##### 5.4.1. Domain Layer

<div align = justify>

<p><b>Entidades de dominio</b></p>

<li>
    <b>Device: </b>Representa un dispositivo a partir de la instalación de un servicio de proyecto.
</li>

<li>
    <b>Routine: </b>Representa una rutina realizada por un usuario a partir de un dispositivo instalado.
</li>

<li>
    <b>Room: </b>Representa una habitación de una casa a donde está instalado el dispositivo.
</li> <br>
  

<p><b>Repositorios</b></p>

<li>
    <b>Servicios de dominio</b>
</li>

<li>
    <b>DeviceRepository: </b>Maneja la persistencia de las suscripciones.
</li>

<li>
    <b>RoutineRepository: </b>Maneja la persistencia de los pagos.
</li>

<li>
    <b>RoomRepository: </b>Maneja la persistencia de los planes de suscripción.
</li> <br>

</div>

##### 5.4.2. Interface Layer

<div align=justify>

<li>
    <b>DeviceController: </b>
El controlador de dispositivos se encargará de gestionar todas las operaciones relacionadas con los dispositivos instalados en un proyecto de Smart Home. Esto podría incluir la creación, actualización y eliminación de dispositivos, así como la configuración de sus parámetros. Además, este controlador podría manejar solicitudes relacionadas con la obtención de detalles de dispositivos y su estado.
</li> <br>

<li>
    <b>RoutineController: </b>El controlador de rutinas gestionaría las operaciones relacionadas con las rutinas realizadas por los usuarios a partir de los dispositivos instalados. Esto podría incluir la creación de rutinas, su ejecución y programación. Además, este controlador podría permitir a los usuarios ver detalles de rutinas existentes.
</li> <br>

<li>
    <b>RoomController: </b>El controlador de habitaciones se encargaría de gestionar las operaciones relacionadas con las habitaciones de una casa donde están instalados los dispositivos. Esto podría incluir la creación y gestión de habitaciones, la asignación de dispositivos a habitaciones específicas y la obtención de información sobre las habitaciones.
</li> <br>




</div>

##### 5.4.3. Application Layer

<div align =justify>

<p>En el contexto de "Smart Home Project Management," el Application Layer se adapta para ofrecer una experiencia móvil a los usuarios. Permite a los usuarios vincular dispositivos inteligentes a proyectos de remodelación específicos y gestionar estos dispositivos desde la aplicación móvil. Los usuarios pueden encender, apagar y ajustar la configuración de los dispositivos a través de la interfaz móvil. Además, se generan eventos para reflejar los cambios de estado de los dispositivos y proporcionar notificaciones a los usuarios móviles.</p>

<p><b>Command Handlers:</b></p>

<li>
    <b>LinkDeviceToProjectCommandHandler: </b>Procesa comandos para vincular dispositivos inteligentes a proyectos de remodelación específicos en ModelHouse. Actualiza la información de asociación en la base de datos para reflejar estos cambios.
</li>
<li>
    <b>ManageDeviceCommandHandler: </b>Permite a los usuarios administrar dispositivos inteligentes dentro de sus proyectos de remodelación. Permite operaciones como encender, apagar o ajustar la configuración de los dispositivos.
</li> <br>

<p><b>Event Handlers:</b></p>

<li>
    <b>DeviceLinkedToProjectEventHandler: </b>Responde a eventos que indican la vinculación exitosa de un dispositivo inteligente a un proyecto de remodelación. Actualiza el estado de los dispositivos y los proyectos en la base de datos.
</li>
<li>
    <b>DeviceStatusUpdatedEventHandler: </b>Maneja eventos relacionados con cambios en el estado de los dispositivos inteligentes, como encendido, apagado o cambios de configuración. Proporciona notificaciones a los usuarios y actualiza el estado en tiempo real.
</li><br>

</div>

##### 5.4.4. Infrastructure Layer

##### 5.4.5. Bounded Context Software Architecture Component Level Diagrams
<center>
            <img src="../images/structurizr-86418-Smart Home Project Management Component Diagram.png">
    </center>

##### 5.4.6. Bounded Context Software Architecture Code Level Diagrams

###### 5.4.6.1. Bounded Context Domain Layer Class Diagrams

<center>
            <img src="../images/Smart home management class.png">
    </center>


###### 5.4.6.2. Bounded Context Database Design Diagram

<center>
            <img src="../images/Smart home db.png">
    </center>
