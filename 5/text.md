## **UNIT V**

### Tactical-Level Software Design.

## 5.1. Bounded Context: 
### Bounded Context: subscription and payment

### 5.1.1. Domain Layer

### 5.1.2. Interface Layer

- CartController:

<div align=justify>
Esta clase esta encargada de gestionar las operaciones relacionadas con el carrito de compras, como agregar productos al carrito, eliminar productos, actualizar cantidades y calcular el total de la compra en el contexto de suscripciones y pagos.
- OrderController:

El OrderController se encarga de gestionar las operaciones relacionadas con la creación y gestión de pedidos en el contexto de suscripciones y pagos. Puede encargarse de la finalización de la compra y la generación de confirmaciones de pedidos.

- PlansController:

Esta clase gestiona la configuración y visualización de los planes de suscripción disponibles en el sistema. Permite a los usuarios seleccionar, ver detalles y administrar la información de facturación y ciclos de pago asociados a los planes de suscripción.

- ProductController:

El ProductController es responsable de las operaciones relacionadas con la gestión de productos en el contexto de suscripciones y pagos. Esto incluye agregar nuevos productos, actualizar detalles de productos existentes y proporcionar información sobre productos disponibles para compra o suscripción.

- SubscriptionsController:

Esta clase se encarga de gestionar las suscripciones de los usuarios. Permite a los usuarios ver sus suscripciones activas, actualizar la información de pago asociada a sus suscripciones y gestionar renovaciones automáticas o cancelaciones de suscripciones.
</div>

### 5.1.3. Application Layer

### 5.1.4. Infrastructure Layer

### 5.1.6. Bounded Context Software Architecture Component Level Diagrams

### 5.1.7. Bounded Context Software Architecture Code Level Diagrams

#### 5.1.7.1. Bounded Context Domain Layer Class Diagrams

#### 5.1.7.2. Bounded Context Database Design Diagram

## 5.2. Bounded Context: 
### Bounded Context: Identity Access Management

### 5.2.1. Domain Layer

### 5.2.2. Interface Layer
<div align=justify>
- AccountController:

El AccountController maneja las operaciones relacionadas con la gestión de cuentas de usuario, como la creación de cuentas, la autenticación y el cierre de sesiones.

- BusinessProfileController:

Esta clase se encarga de gestionar los perfiles empresariales en el contexto de Identity Access Management, lo que incluye crear y actualizar perfiles empresariales y definir roles y permisos relacionados con la empresa.

- ProjectController:

El ProjectController gestiona las operaciones relacionadas con la gestión de proyectos dentro del contexto de Identity Access Management, permitiendo a los usuarios crear, editar y administrar proyectos.

- UserController:

Esta clase maneja las operaciones de gestión de usuarios, incluyendo el registro, autenticación, actualización de perfiles y eliminación de cuentas.

- UserProfileController:

El UserProfileController está encargado de las operaciones específicas relacionadas con los perfiles de usuario, como la actualización de la información personal del usuario.
</div>

### 5.2.3. Application Layer

### 5.2.4. Infrastructure Layer

### 5.2.6. Bounded Context Software Architecture Component Level Diagrams

### 5.2.7. Bounded Context Software Architecture Code Level Diagrams

#### 5.2.7.1. Bounded Context Domain Layer Class Diagrams

#### 5.2.7.2. Bounded Context Database Design Diagram

## 5.3. Bounded Context: 
### Bounded Context: Service Management

### 5.3.1. Domain Layer

### 5.3.2. Interface Layer
<div align=justify>
- ProjectActivityController:

Esta clase gestiona las actividades relacionadas con proyectos en el contexto de Service Management, permitiendo la creación, edición y seguimiento de actividades asociadas a proyectos.

- ProjectResourceController:

El ProjectResourceController está encargado de la gestión de recursos o activos relacionados con proyectos, como la asignación de recursos a proyectos específicos.

- ProposalController:

Esta clase gestiona las propuestas relacionadas con proyectos o servicios, incluyendo la creación, revisión y aceptación de propuestas.

- RequestController:

El RequestController maneja las solicitudes de servicio o proyectos, permitiendo a los usuarios crear solicitudes, realizar seguimiento y recibir respuestas de proveedores de servicios.
</div>

### 5.3.3. Application Layer

### 5.3.4. Infrastructure Layer

### 5.3.6. Bounded Context Software Architecture Component Level Diagrams

### 5.3.7. Bounded Context Software Architecture Code Level Diagrams

#### 5.3.7.1. Bounded Context Domain Layer Class Diagrams

#### 5.3.7.2. Bounded Context Database Design Diagram