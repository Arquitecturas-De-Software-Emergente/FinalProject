## **UNIT V**

---

### Tactical-Level Software Design.

#### 5.1. Bounded Context: subscription and payment

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
    <b>CartController: </b> Esta clase esta encargada de gestionar las operaciones relacionadas con el carrito de compras, como agregar productos al carrito, eliminar productos, actualizar cantidades y calcular el total de la compra en el contexto de suscripciones y pagos.
</li> <br>

<li>
    <b>OrderController: </b>El OrderController se encarga de gestionar las operaciones relacionadas con la creación y gestión de pedidos en el contexto de suscripciones y pagos. Puede encargarse de la finalización de la compra y la generación de confirmaciones de pedidos.
</li> <br>

<li>
    <b>PlansController: </b> Esta clase gestiona la configuración y visualización de los planes de suscripción disponibles en el sistema. Permite a los usuarios seleccionar, ver detalles y administrar la información de facturación y ciclos de pago asociados a los planes de suscripción.
</li> <br>

<li>
    <b>ProductController: </b>El ProductController es responsable de las operaciones relacionadas con la gestión de productos en el contexto de suscripciones y pagos. Esto incluye agregar nuevos productos, actualizar detalles de productos existentes y proporcionar información sobre productos disponibles para compra o suscripción.
</li> <br>

<li>
    <b>SubscriptionsController: </b>Esta clase se encarga de gestionar las suscripciones de los usuarios. Permite a los usuarios ver sus suscripciones activas, actualizar la información de pago asociada a sus suscripciones y gestionar renovaciones automáticas o cancelaciones de suscripciones.
</li> <br>

</div>

##### 5.1.3. Application Layer

##### 5.1.4. Infrastructure Layer

##### 5.1.5. Bounded Context Software Architecture Component Level Diagrams

##### 5.1.6. Bounded Context Software Architecture Code Level Diagrams

###### 5.1.6.1. Bounded Context Domain Layer Class Diagrams

###### 5.1.6.2. Bounded Context Database Design Diagram

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

##### 5.2.4. Infrastructure Layer

##### 5.2.5. Bounded Context Software Architecture Component Level Diagrams

##### 5.2.6. Bounded Context Software Architecture Code Level Diagrams

###### 5.2.6.1. Bounded Context Domain Layer Class Diagrams

###### 5.2.6.2. Bounded Context Database Design Diagram

#### 5.3. Bounded Context: Service Management

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
    <b>ProjectActivityController: </b>Esta clase gestiona las actividades relacionadas con proyectos en el contexto de Service Management, permitiendo la creación, edición y seguimiento de actividades asociadas a proyectos.
</li> <br>

<li> 
    <b>ProjectResourceController: </b>El ProjectResourceController está encargado de la gestión de recursos o activos relacionados con proyectos, como la asignación de recursos a proyectos específicos.
</li> <br>

<li> 
    <b>ProposalController: </b>Esta clase gestiona las propuestas relacionadas con proyectos o servicios, incluyendo la creación, revisión y aceptación de propuestas.
</li> <br>

<li> 
    <b>RequestController: </b>El RequestController maneja las solicitudes de servicio o proyectos, permitiendo a los usuarios crear solicitudes, realizar seguimiento y recibir respuestas de proveedores de servicios.
</li> <br>

</div>

##### 5.3.3. Application Layer

##### 5.3.4. Infrastructure Layer

##### 5.3.5. Bounded Context Software Architecture Component Level Diagrams

##### 5.3.6. Bounded Context Software Architecture Code Level Diagrams

###### 5.3.6.1. Bounded Context Domain Layer Class Diagrams

###### 5.3.6.2. Bounded Context Database Design Diagram

#### 5.4. Bounded Context: Smart Home Project management

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
    <b>ProjectActivityController: </b>Esta clase gestiona las actividades relacionadas con proyectos en el contexto de Service Management, permitiendo la creación, edición y seguimiento de actividades asociadas a proyectos.
</li> <br>

<li>
    <b>ProjectResourceController: </b>El ProjectResourceController está encargado de la gestión de recursos o activos relacionados con proyectos, como la asignación de recursos a proyectos específicos.
</li> <br>

<li>
    <b>ProposalController: </b>Esta clase gestiona las propuestas relacionadas con proyectos o servicios, incluyendo la creación, revisión y aceptación de propuestas.
</li> <br>

<li>
    <b>RequestController:</b>El RequestController maneja las solicitudes de servicio o proyectos, permitiendo a los usuarios crear solicitudes, realizar seguimiento y recibir respuestas de proveedores de servicios.
</li> <br>


</div>

##### 5.4.3. Application Layer

##### 5.4.4. Infrastructure Layer

##### 5.4.5. Bounded Context Software Architecture Component Level Diagrams

##### 5.4.6. Bounded Context Software Architecture Code Level Diagrams

###### 5.4.6.1. Bounded Context Domain Layer Class Diagrams

###### 5.4.6.2. Bounded Context Database Design Diagram