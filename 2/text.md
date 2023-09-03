# REQUIREMENTS ELICITATION & ANALYSIS

## 1.1 Competidores

### 1.1.1 Análisis competitivo

<table>
    <tr>
        <td colspan=8 align="center">Competitive Analysis Landscape</td>
    <tr>
    <tr >
        <td rowspan=2 colspan=4>¿Por qué llevar a cabo este análisis?</td>
        <td colspan=6>Escriba en el recuadro la pregunta que busca responder o el objetivo de este análisis.</td>
    </tr>
    <tr>
        <td colspan=6>El objetivo principal del Competitive Analysis Landscape es conocer sus competidores, en contraste con la idea principal que se tenga sobre ellos.</td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td align="center" colspan=3>ModelHouse <img src="../images/ModelHouse.png"> </td>
        <td align="center">Coremant <img src="../images/Coremant.png"> </td>
        <td align="center">Joregoga <img src="../images/Joregoga.png"> </td>
        <td align="center">Construcción & Remodelación <img src="../images/Construcción.png"> </td>
    </tr>
    <tr>
        <td>Perfil</td>
        <td>Overview</td>
        <td colspan=3>Una aplicación intermediaria entre el proveedor y el cliente. Que permite a este último, encontrar empresas de remodelación de calidad de manera rápida y la opción de comentar sus trabajos. En cuanto a los proveedores, tiene un canal donde mostrar sus proyectos y organizar sus actividades. Como opción adicional, además, podrá visualizar gráficos analíticos</td>
        <td>Una empresa especializada en la construcción, remodelación y mantenimiento que reúne técnicos experimentados para soluciones sostenibles y servicios de calidad.</td>
        <td>Empresa constructora que brinda servicios de desarrollo y diseño de proyectos de construcción, diseño de interiores, remodelación de casas completas, y obras civiles.</td>
        <td>Empresa de diseño de proyectos que brinda servicios de diseño, anteproyecto e implementación.</td>
    </tr>
    <tr>
        <td>Perfil de Marketing</td>
        <td>Mercado objetivo</td>
        <td colspan=3>Clientes entre los 27 y 45 años que tengan interés de una remodelación.</td>
        <td>Empresas con grandes proyectos.</td>
        <td>Personas que quieran construir y/o remodelar casas y empresas que quieran establecer una construcción en sus zonas.</td>
        <td>Personas y compañías o empresas que quieran remodelar o realizar una construcción en su propiedad.</td>
    </tr>
    <tr>
        <td>Perfil de Producto</td>
        <td>Productos & Servicios</td>
        <td colspan=3>Encontrar al remodelador deseado mediante un buscador y filtro de búsqueda avanzada para encontrar a los trabajadores de acuerdo con sus intereses y podrá revisar el historial de proyectos para informarse de manera eficiente.</td>
        <td>Desarrollo de proyectos de Ingeniería para la construcción y mantenimiento en general.</td>
        <td>Confianza con la remodelación, diseño o construcción de cualquier espacio al estilo que más prefiera con la tecnología más actual</td>
        <td>Ofrece servicios de construcción, enchapes, pisos, vidriería, carpintería metálica, instalaciones eléctricas, trabajos con aire acondicionado, cámaras de seguridad, alarmas contra incendios, instalaciones sanitarias, carpintería de madera, sistema Drywall, señalética y planos de evacuación internet, mobiliarios realizados en melanina y trabajos de pintura y mantenimiento.</td>
    </tr>
    <tr>
        <td>Análisis SWOT</td>
        <td>Fortalezas Debilidades</td>
        <td colspan=3>Mayor rapidez de contratación de remodeladores.</td>
        <td>Técnicos profesionales que brindan servicios de calidad.</td>
        <td>- Trabajadores con más de 5 años de experiencia - Equipamiento Tecnológico</td>
        <td>- 32 años de experiencia en el mercado. - Materiales durables a largo plazo</td>
    </tr>
    
</table>

### 1.1.2 Solution Software Design

Luego de analizar a nuestros competidores, hemos logrado observar que existen debilidades que aún no han sido resueltas. Esto puede ser utilizado en cuenta para mejorar y destacar, nuestro proyecto, de la competencia. Las ventajas competitivas que podemos desarrollar lo desarrollaremos como estrategias como:

- Capacitación sobre liderazgo de equipos.
- Campaña de marketing en universidades, institutos y empresas.
- Realizar actualizaciones de software cada que se requiera.
- Implementar una sección de mejora para recibir comentarios de la interfaz por parte del usuario.
- Establecer un chat de espera para contactarse con una empresa.
- 


## 2.3 Needfinding
A continuación, se mostrará los artefactos realizados de acuerdo a la retroalimentación de las necesidades de los usuarios a través de las entrevistas. Estos artefactos creados son para los dos tipos de segmentos objetivos: empresa de remodelación y cliente. Estos son user personas, user tax matrix, empathy mapping y el as-is escenario mapping.
### 2.3.1 User personas
#### 2.3.1.1 Cliente

<image
  src="../images/user-persona-cliente.png"
  alt="User persona cliente">

#### 2.3.1.2 Empresa de remodelación 
<image
  src="../images/user-persona-empresa.png"
  alt="User persona empresa de remodelación">

### 2.3.2 User task matrix
Se realiza un análisis de las principales funciones detectadas en la problemática. Esto basado por los comentarios obtenidos de los 2 segmentos de usuario: Cliente y Empresa.
<style>
  table {
    border-collapse: collapse;
    width: 100%;
  }
  th {
    background-color: red;
    color: white;
    font-size: 15px;
  }
  td{
    background-color: white;
    color: black;
    font-weight: 200;
  }
  th, td {
    padding: 10px;
    text-align: center;
  }
  .subh{
    background: skyblue;
  }
</style>
<table>
  <tr>
    <th rowspan="2">Task Matrix</th>
    <th colspan="2">Cliente</th>
    <th colspan="2">Empresa</th>
  </tr>
  <tr>
    <td class="subh">Frecuencia</td>
    <td class="subh">Importancia</td>
    <td class="subh">Frecuencia</td>
    <td class="subh">Importancia</td>
  </tr>
  <tr>
    <td>Brindar seguridad al realizar un acuerdo de remodelación</td>
    <td>A veces</td>
    <td>Alta</td>
    <td>Alta</td>
    <td>Alta</td>
  </tr>
  <tr>
    <td>Registro de los hechos que se realizan durante el periodo de remodelación</td>
    <td>Siempre</td>
    <td>Alta</td>
    <td>Siempre</td>
    <td>Alta</td>
  </tr>
  <tr>
    <td>Publicidad de proyectos de remodelación</td>
    <td>Nunca</td>
    <td>Baja</td>
    <td>Alta</td>
    <td>Media</td>
  </tr>
  <tr>
    <td>Registrar la cotización de la remodelación</td>
    <td>A veces</td>
    <td>Media</td>
    <td>Siempre</td>
    <td>Media</td>
  </tr>
  <tr>
    <td>Registrar reclamos en el transcurso de la cotización.</td>
    <td>Siempre</td>
    <td>Alta</td>
    <td>Siempre</td>
    <td>Alta</td>
  </tr>
</table>

### 2.3.3 Empathy mapping
#### 3.3.3.1 cliente
<image
  src="../images/empathy-mapping-cliente.png"
  alt="Emapthy mapping de cliente">

#### 3.3.3.2 empresa de remodelación
<image
  src="../images/empathy-mapping-empresa.png"
  alt="Empathy mapping de empresa">

### 2.3.4 As-is scenario mapping
#### 2.3.4.1 cliente
<image
  src="../images/as-is-scenario-mapping-cliente.png"
  alt="As-is scenario mapping cliente">

#### 2.3.4.2 empresa
<image
  src="../images/as-is-scenario-mapping-empresa.png"
  alt="As-is scenario mapping empresa">

