## **UNIT VII**

---

### Product Implementation, Validation & Deployment

#### 7.1. Software Configuration Management
# Procedimiento de Identificación del Entorno de Desarrollo del Software

### Selección de Elementos de Configuración

- Se identifican los productos de trabajo críticos para el proyecto.
- Se identifican los productos de trabajo que son utilizados por más de un equipo de desarrollo.

## Elementos de Configuración

### Project Management

- [Google Drive](https://drive.google.com/drive) se utiliza para organizar los puntos a realizar, pendientes y realizados.
- [Trello](https://trello.com) se utiliza para establecer hitos y fijar límites para las tareas pendientes.

### Requirements Management

- Se utiliza [Discord](https://discord.com/login) como canal de comunicación para revisar y sugerir cambios en las tareas asignadas a cada integrante.

### Product UX/UI Design

- Se utiliza [Figma](https://figma.com) para el diseño de wireframes de alta fidelidad, Mockup y prototipos móviles.

### Software Development

- [UXPressia](https://uxpressia.com) se utiliza en la creación de artefactos de la metodología Lean UX.
- [Trello](https://trello.com) se usa para dar seguimiento a las historias de usuario y la organización de equipos.
- [Vertabelo](https://vertabelo.com/) se utiliza para la creación de diagramas de bases de datos.
- [Lucid Chart](https://www.lucidchart.com) se utiliza para elaborar Wireflows, User Flows y diagramas de clases.
- [Structurizr](https://structurizr.com) se utiliza para la creación de C4 Context, Container y Component.
- [GitHub](https://github.com) se utiliza para almacenar los repositorios del proyecto.

### Esquema de Identificadores Únicos

Para este proyecto, se utiliza el siguiente esquema para la codificación de los elementos de configuración:

`<StartUp><proyecto><type><name><versión>`

- `<StartUp>`: Identificador de la StartUp (FW).
- `<proyecto>`: Identificador del tipo de proyecto (RKG).
- `<type>`: Identificador del tipo de elemento.
- `<name>`: Nombre del elemento.
- `<versión>`: Versión del elemento.

### Ejemplos de Identificadores Únicos

- Requisitos: FW-RKG-REQ
- User stories: FW-RKG-REQ-US-1.0.0
- Sprint Backlog: FW-RKG-REQ-SB-1.0.0
- Product Backlog: FW-RKG-REQ-PB-1.0.0

- Repositorios: FW-RKG-REP
- Landing Page Repository: FW-RKG-REP-LP
- Mobile App Repository: FW-RKG-REP-WA

- Arquitectura: FW-RKG-ARQ
- User stories: FW-RKG-REQ-US-1.0.0
- Sprint Backlog: FW-RKG-REQ-SB-1.0.0
- Product Backlog: FW-RKG-REQ-PB-1.0.0

##### 7.1.1. Software Development Environment Configuration

## Modelo de Creación de Ramas Gitflow

Este proyecto utiliza el modelo de creación de ramas Gitflow para el desarrollo y gestión de versiones en GitHub.

### Repositorios

| Nombre           | Enlace                                                                                                            |
|------------------|-------------------------------------------------------------------------------------------------------------------|
| Back-end         | [Arquitecturas-De-Software-Emergente/ModelHouseV2](https://github.com/Arquitecturas-De-Software-Emergente/ModelHouseV2)           |
| Front-end mobile | [Arquitecturas-De-Software-Emergente/ModelHouseMovil](https://github.com/Arquitecturas-De-Software-Emergente/ModelHouseMovil)       |
| Front-end Web    | [Arquitecturas-De-Software-Emergente/ModelHouseV1](https://github.com/Arquitecturas-De-Software-Emergente/ModelHouseV1) |
| Landing Page     | [Arquitecturas-De-Software-Emergente/LandingPage](https://github.com/Arquitecturas-De-Software-Emergente/LandingPage)        |

### Ramas en el Modelo Gitflow

- **Main Branch:** En esta rama se encuentra la versión completa, probada y sin problemas en su ejecución. Es la rama que se desplegará y mostrará a los usuarios.

- **Hotfix Branch:** Se utiliza en caso de problemas con la versión en la rama Main. Sirve como respaldo para encontrar y solucionar problemas lo más rápido posible.

- **Release Branch:** En esta rama, la aplicación móvil se ejecuta sin problemas, pero debe pasar por pruebas para validar todas las funcionalidades. Cuando las pruebas se completan sin errores, esta versión pasa a la rama Main.

- **Develop Branch:** Esta rama sigue en desarrollo y se utilizan para solucionar distintos problemas o requerimientos en desarrollo. Cuando esta rama está lista para un sprint, pasa a la rama Release.

- **Feature Branch:** Estas ramas se crean según sea necesario para agregar nuevas funcionalidades a la aplicación móvil.
    - Deben derivarse de la rama develop.
    - Deben fusionarse de vuelta a la rama develop.
    - Notación: `Name of feature`

##### 7.1.2. Source Code Management

##### 7.1.3. Source Code Style Guide & Conventions

##### 7.1.4. Software Deployment Configuration

#### 7.2. Solution Implementation

##### 7.2.1. Sprint 1

###### 7.2.1.1. Sprint Planning 1

###### 7.2.1.2. Sprint Backlog 1

###### 7.2.1.3. Development Evidence for Sprint Review

###### 7.2.1.4. Testing Suite Evidence for Sprint Review

###### 7.2.1.5. Execution Evidence for Sprint Review.

###### 7.2.1.6. Services Documentation Evidence for Sprint Review

###### 7.2.1.7. Software Deployment Evidence for Sprint Review

###### 7.2.1.8. Team Collaboration Insights during Sprint

#### 7.3. Validation Interviews

##### 7.3.1. Diseño de Entrevistas

##### 7.3.2. Registro de Entrevistas

##### 7.3.3. Evaluaciones según heurísticas

##### 7.4. Video About-the-Product