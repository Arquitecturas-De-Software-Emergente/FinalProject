## **UNIT VII**

---

### Product Implementation, Validation & Deployment

#### 7.1. Software Configuration Management

##### 7.1.1. Software Development Environment Configuration

### Procedimiento de Identificación del Entorno de Desarrollo del Software

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

##### 7.1.2. Source Code Management

### Modelo de Creación de Ramas Gitflow

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

##### 7.1.3. Source Code Style Guide & Conventions

<p align = justify>- Para el desarrollo de nuestro proyecto hemos adoptado algunas referencias para nombrar elementos y programar en los lenguajes utilizados para la solución. </p>

<p align = justify>- Convenciones de Idioma</p>

- Uso del **español** para todos los artefactos que sirven como evidencia de desarrollo de la aplicación.
- Uso del **inglés** para la elaboración del código de compilación, tanto en el Back-end como en el Front-end.

<p align = justify>- Nomenclatura</p>

<p align = justify>- Seguiremos utilizando la nomenclatura establecida en "Software Development Environment Configuration" para lo relacionado con el uso y modificación de los distintos repositorios.</p>

- Herramientas
  - Para el desarrollo de la aplicación, utilizaremos las siguientes tecnologías:
  - **Back-end**: Sprint Boot.
  - **Front-end**: Vue para la web.
  - **Base de datos**: MySQL.
  - **Mobile**: Flutter para las aplicaciones móviles
  - **IDEs**: Rider y Visual Studio Code para la codificación, Flutter y Dart para el desarrollo de aplicaciones móviles, y WebStorm para Vue.
  - **Control de versiones**: GitHub y Gitflow.
  - **Diseño de interfaz**: Figma.

#### Semantic Versioning

<p align = justify>- Seguiremos utilizando Semantic Versioning para controlar las versiones de nuestra aplicación.</p>

#### Conventional Commits

<p align = justify>- Seguiremos las convenciones de commits basadas en "Conventional Commits 1.0.0". Se debe seguir la siguiente estructura para un commit:</p>

```plaintext
git commit -m "<type> (optional scope) <title>" -m "<description>"
  <type> = feat | fix | docs | style | refactor | test | chore
  <title> = 50 caracteres máximo
  <description> = 72 caracteres máximo
```

- Types:
  - Add: se usará para indicar que se añadieron archivos o carpetas.
  - Fix: este tipo de commit se utilizará para la confirmación de una corrección de un error en el código.
  - Feat: este tipo de commit se utilizará para la confirmación de que se ha añadido una nueva funcionalidad.
  - Test: se usará para indicar que se añadieron archivos test.

#### Arquitectura de Vue(convenciones)

<p align = justify>- Para la arquitectura de Vue, se seguirá la siguiente estructura:</p>

```plaintext
src
├── assets
│   ├── css
│   ├── fonts
│   ├── img
│   └── js
├── components
│   ├── common
│   ├── layout
│   └── views
├── router
├── store
├── utils
└── views
```

- **assets**: contiene los recursos estáticos como imágenes, fuentes y archivos CSS.
- **components**: contiene los componentes de la aplicación.
- **router**: contiene los archivos de configuración de las rutas.
- **store**: contiene los archivos de configuración de Vuex.
- **utils**: contiene los archivos de configuración de la aplicación.
- **views**: contiene las vistas de la aplicación.

##### 7.1.4. Software Deployment Configuration

<p align = justify>Para el despliegue de nuestra plataforma, tenemos los siguientes productos.</p>

#### Landing Page

<p align = justify>Para el despliegue del landing page hemos utilizado las siguientes herramientas:</p>

- **Git**: Para manejar las versiones del código de la Landing Page.
- **GitHub**: Para almacenar el proyecto y permitir la colaboración en la codificación.
- **GitFlow**: Para controlar y visualizar el flujo de trabajo del equipo.
- **Trello**: Para dividir las tareas y documentar el sprint.

#### Despliegue

<p align = justify> Para el despliegue de nuestra plataforma, tenemos los siguientes productos.</p>

- Landing Page

<p align = justify> Para el despliegue del landing page hemos utilizado herramientas como:</p>

- **Git:** Para manejar las versiones del código de la Landing Page.
- **GitHub:** Para almacenar el proyecto y poder codificarlo colaborativamente.
- **GitFlow:** Para controlar y visualizar el flujo de trabajo del equipo.
- **Trello:** Para poder dividirnos las tareas a realizar para la documentación del sprint

<p align = justify>Para desplegar el landing page se ha utilizado la herramienta Page de GitHub que nos permitió generar un enlace con todas las características que la rama master contiene. Por otro lado, si quieres desplegarlo de manera remota a partir del repositorio del GitHub, puedes clonar nuestro proyecto con: git clone, en el git local.</p>

<table>
    <thead>
        <tr>
            <th>Backend</th>
            <th><a href="https://github.com/Arquitecturas-De-Software-Emergente/ModelHouseV2.git">https://github.com/Arquitecturas-De-Software-Emergente/ModelHouseV2.git</a></th>
        </tr>
        <tr>
            <th>Frontend</th>
            <th><a href="https://github.com/Arquitecturas-De-Software-Emergente/ModelHouseV1.git">https://github.com/Arquitecturas-De-Software-Emergente/ModelHouseV1.git</a></th>
        </tr>
        <tr>
            <th>Lading Page</th>
            <th><a href="https://github.com/Arquitecturas-De-Software-Emergente/LandingPage.git">https://github.com/Arquitecturas-De-Software-Emergente/LandingPage.git</a>
            </th>
        </tr>
        <tr>
            <th>Mobile</th>
            <th><a href="https://github.com/Arquitecturas-De-Software-Emergente/ModelHouseMovil.git">https://github.com/Arquitecturas-De-Software-Emergente/ModelHouseMovil.git</a></th>
        </tr>
    </thead>
</table>

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
