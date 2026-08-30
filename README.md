# 🎓 EduPlaner - Sistema Integral de Gestión Académica

![EduPlaner Banner](https://via.placeholder.com/1200x400.png?text=EduPlaner+-+Organizacion+y+Progreso+Estudiantil)

**EduPlaner** es una plataforma web desarrollada de principio a fin pensando en las necesidades reales de los estudiantes universitarios[cite: 4]. Este proyecto representa la culminación de un proceso exhaustivo de investigación de Experiencia de Usuario (UX) y Desarrollo de Interfaces (UI), abarcando desde la concepción del problema en la fase RDA 1 hasta la codificación total del Front-End en la fase RDA 3[cite: 4].

Nuestra misión principal con EduPlaner es combatir la dispersión de la información académica[cite: 4]. Comúnmente, los estudiantes dividen su atención entre agendas físicas, recordatorios mentales y diversas plataformas institucionales, lo que inevitablemente lleva al olvido de tareas y a un alto nivel de estrés[cite: 4]. EduPlaner soluciona esto centralizando deberes, exámenes, proyectos y gráficas de rendimiento en un único ecosistema digital accesible, rápido e intuitivo[cite: 4].

## 🔗 Enlaces Oficiales del Proyecto

* **🌐 Proyecto Desplegado (En Vivo):** [EduPlaner en GitHub Pages](https://iacarrion.github.io/ProyectoRDA3WMI/)[cite: 4]
* **💻 Repositorio Código Fuente:** [ProyectoRDA3WMI](https://github.com/iacarrion/ProyectoRDA3WMI)[cite: 4]
* **🎨 Prototipos Interactivos:** *(Añade aquí el link a tu archivo de Figma)*

---

## 🎯 Origen del Proyecto: El Problema y Nuestro Usuario

El desarrollo de esta plataforma está estrictamente fundamentado en el **Diseño Centrado en el Usuario (DCU)**[cite: 4]. Durante nuestra investigación inicial, descubrimos que los estudiantes universitarios gestionan varias materias de forma simultánea, y al carecer de un punto único de organización, pierden fechas de entrega importantes y acumulan actividades atrasadas[cite: 4]. Además, notamos una gran dificultad en los estudiantes para dimensionar su propio avance a lo largo del semestre académico[cite: 4].

### La "User Persona" que guio nuestro desarrollo
Para materializar estas frustraciones en soluciones de código, construimos perfiles basados en encuestas reales, destacando a nuestro usuario principal: **Mateo**[cite: 4].
* **Perfil:** Estudiante universitario de 22 años con un nivel tecnológico alto[cite: 4].
* **Comportamiento Digital:** Utiliza principalmente su teléfono celular para revisar tareas rápidamente en cualquier lugar, y su computadora portátil para sesiones de estudio profundas[cite: 4].
* **Dolores (Frustraciones):** Olvida frecuentemente fechas de entrega, le cuesta priorizar qué actividad realizar primero y se frustra cuando las aplicaciones tienen una curva de aprendizaje compleja o interfaces confusas[cite: 4].
* **Motivación:** Desea fervientemente visualizar su progreso real para mantenerse motivado y organizar sus proyectos de manera eficiente[cite: 4].

Basados en Mateo, tomamos decisiones cruciales de arquitectura: implementamos un diseño rigurosamente responsivo (*mobile-first*), añadimos una sección dedicada de "Recordatorios" y creamos un panel visual de "Progreso" que calcula automáticamente el rendimiento[cite: 4].

---

## ✨ Arquitectura de la Información y Experiencia de Usuario

EduPlaner se compone de un ecosistema de pantallas interconectadas. El mapa de sitio fue refinado iterativamente desde los wireframes iniciales, incorporando incluso una pantalla de Registro que no estaba contemplada originalmente pero que resultó vital para la lógica de la aplicación[cite: 4].

1. **Inicio:** Un panel de bienvenida (*dashboard*) que muestra las opciones principales, asegurando que las funciones esenciales estén a un solo clic de distancia[cite: 4].
2. **Registro:** Formulario validado para la creación de cuentas de usuario[cite: 4].
3. **Mis Tareas:** El núcleo operativo. Permite listar tareas clasificadas por materia, agregar nuevas mediante un formulario dinámico y marcarlas como completadas[cite: 4].
4. **Calendario:** Una vista mensual que incorpora un acordeón de materias y una lista editable y persistente de próximos exámenes[cite: 4].
5. **Recordatorios:** Un espacio dedicado exclusivamente para dar de alta y baja alertas tempranas, evitando el olvido de actividades[cite: 4].
6. **Proyectos:** Galería visual que agrupa actividades relacionadas bajo un mismo proyecto académico mayor[cite: 4].
7. **Progreso:** Un panel analítico que muestra un gráfico comparativo de tendencias (generado dinámicamente) y tarjetas individuales que calculan automáticamente el porcentaje de avance por materia[cite: 4].
8. **Herramientas, Ayuda y Configuración:** Módulos de soporte que incluyen filtros avanzados, un buscador de preguntas frecuentes (FAQ) y administración de accesibilidad[cite: 4].

### El Flujo de Valor Principal
Para demostrar el poder de la aplicación, el usuario puede experimentar el siguiente flujo ininterrumpido:
El usuario ingresa a "Mis Tareas" y completa el formulario de nueva actividad, pudiendo incluso crear una materia nueva en ese instante[cite: 4]. Al presionar "Agregar Tarea", la lista se actualiza instantáneamente en pantalla sin recargar el navegador[cite: 4]. Posteriormente, al marcar esa tarea mediante el *checkbox* de completada y navegar hacia la pantalla de "Progreso", el usuario verá cómo el porcentaje de avance de esa materia se ha recalculado de manera automática y el gráfico general de tendencias refleja su nuevo esfuerzo[cite: 4].

---

## 🛠️ Ingeniería y Desarrollo Front-End

Tomamos la decisión consciente de construir este proyecto utilizando tecnologías nativas de la web. Esto no solo garantiza un rendimiento ligero y rápido, sino que demuestra un dominio profundo de las bases del desarrollo frontend sin depender de librerías de terceros.

### 1. Estructura Semántica y Accesible (HTML5)
Rechazamos el uso excesivo de `<div>` genéricos[cite: 4]. Cada pantalla está maquetada utilizando etiquetas estructurales semánticas (`<header>`, `<main>`, `<section>`, `<nav>`, `<footer>`), lo que mejora drásticamente la interpretación del sitio por parte de navegadores y tecnologías de asistencia[cite: 4]. Se implementaron atributos de accesibilidad como `aria-label` y `role="img"` en elementos decorativos[cite: 4].

### 2. Sistema de Diseño y Preprocesamiento (CSS3 / SCSS)
La escalabilidad visual se logró estructurando los estilos con el preprocesador **SCSS**.
* **Arquitectura de Archivos:** Dividimos la lógica visual en parciales (`_variables.scss`, `_header.scss`, `_hero.scss`, `_cards.scss`) que finalmente compilan en un único archivo de distribución `styles.css`[cite: 4].
* **Tokens de Diseño (Variables):** Definimos una base estricta en el seudoclase `:root`. 
  * *Tipografía:* Arial y sans-serif (`--font-primary`)[cite: 4].
  * *Espaciados:* Uniformes utilizando variables como `--space-sm` (1 rem) para interiores de tarjetas, `--space-md` (1.5 rem) para separaciones de secciones y `--space-lg` (2 rem) para bloques principales[cite: 4].
  * *Bordes:* Estandarizados con `--radius-sm` (6px) para botones y `--radius-md` (12px) para contenedores mayores[cite: 4].
* **Componentización:** Se crearon clases maestras reutilizables como `.btn` (con modificadores `-primary`, `-success`, `-danger`), `.card` (con elevación y sombra en estado `:hover`), y `.input` (con bordes reactivos al estado `:focus` o `-error`)[cite: 4].

### 3. Layout Responsivo y Flexbox
La aplicación fue concebida con la filosofía *Desktop-first* en su código base, pero fuertemente adaptada a la realidad del usuario móvil mediante *Media Queries*.
Elegimos **Flexbox** como el mecanismo de diseño predominante (por encima de CSS Grid) debido a que necesitábamos que las tarjetas de navegación y tareas tuvieran un reordenamiento fluido (`flex-wrap: wrap`) que se adaptara orgánicamente al espacio disponible[cite: 4].
* **Dispositivos Móviles (hasta 390px):** Las tarjetas colapsan a una sola columna (`flex: 1 1 100%`), los menús se simplifican y las secciones descriptivas apilan sus elementos verticalmente[cite: 4].
* **Tablets (hasta 768px):** La cuadrícula se reorganiza en dos columnas, mientras que los formularios mantienen un ancho seguro y centrado para no deformarse[cite: 4].
* **Escritorio (1440px y superior):** Se despliegan tres columnas completas aprovechando el espacio panorámico de los monitores[cite: 4].

### 4. Lógica y Persistencia (Vanilla JavaScript - ES6+)
Para que EduPlaner fuera una aplicación realmente útil y no solo una maqueta visual, desarrollamos la interactividad íntegramente con JavaScript puro.
* **Manipulación del DOM:** Uso de `querySelector`, `addEventListener` y creación de nodos HTML dinámicos al vuelo para las listas de tareas y exámenes[cite: 4].
* **Persistencia de Datos (LocalStorage):** Toda la información ingresada por el usuario (tareas, estados de completado, materias nuevas) se guarda directamente en la memoria local del navegador[cite: 4]. Esto permite que el usuario cierre la pestaña, regrese horas después y encuentre toda su planificación intacta sin necesidad de un servidor backend[cite: 4].
* **Cálculo Dinámico:** Construimos algoritmos que leen el estado de las tareas guardadas y recalculan matemáticamente el porcentaje de avance, inyectando estos valores en gráficos SVG renderizados dinámicamente[cite: 4].

---

## 🧪 Pruebas de Calidad, UX y Resolución de Problemas

Un producto de software profesional requiere someterse a escrutinio. Participamos en una etapa de **Validación Cruzada** donde un equipo auditor independiente (Grupo 8) evaluó nuestro proyecto bajo las normativas de Accesibilidad (WCAG) y las 10 Heurísticas de Usabilidad de Jakob Nielsen[cite: 4].

### Hallazgos y Refactorización del Código
Esta auditoría arrojó 9 hallazgos críticos que abordamos con total seriedad mediante correcciones de código directas:
* **Accesibilidad y Contraste:** Las herramientas como WAVE detectaron problemas de legibilidad en la sección "¿Quiénes somos?", los cuales solucionamos ajustando las variables de contraste del texto secundario sobre fondos claros[cite: 4]. Además, se insertaron rigurosamente los atributos `alt` faltantes en imágenes informativas vitales para lectores de pantalla[cite: 4].
* **Corrección de Diseño Responsivo:** Detectamos un bug crítico donde pantallas enteras (como *Herramientas* o *Proyectos*) no respondían a los media queries en celulares. Descubrimos que faltaba la etiqueta `<meta name="viewport">` en el `<head>`, lo cual fue reparado inmediatamente para recuperar la adaptabilidad móvil[cite: 4].
* **Navegación y Prevención de Errores (Heurísticas):** Se corrigió un error 404 proveniente de un enlace roto en la pantalla de Registro, garantizando una ruta de escape clara para el usuario (Heurística de Control y Libertad del Usuario)[cite: 4]. También se uniformó el idioma de ciertos componentes del calendario que estaban por error en inglés[cite: 4].
* **Consistencia Visual:** Documentamos y aceptamos el reto de unificar paletas de colores divergentes descubiertas en pantallas como *Calendario* (morado `#8F8BD9`) y *Progreso* (verde `#B9F2B0`), para alinearlas con el sistema azul base del UI Kit corporativo[cite: 4].

---

## 🤝 Metodología de Trabajo en Equipo y Git

Desarrollar una aplicación de este calibre requirió una coordinación meticulosa entre los miembros del equipo. Establecimos un flujo de trabajo profesional utilizando control de versiones con **Git y GitHub**.

* **Estrategia de Ramas (Branching):** En lugar de sobreescribir el trabajo mutuamente, implementamos ramas individuales enfocadas en funcionalidades específicas (ej. `feature/pantalla-registro`, `feature/calendario`, `feature/responsive-cards`, `feature/scss-header`)[cite: 4].
* **Integración (Pull Requests):** Todo el código nuevo se integraba a la rama `main` de manera progresiva.
* **Resolución de Conflictos:** Al compartir archivos troncales (como el archivo compilado `styles.css` o el `_variables.scss`), nos enfrentamos a múltiples conflictos de fusión (*merge conflicts*). El equipo aprendió a resolver estas colisiones de código manualmente, analizando qué líneas conservar, demostrando madurez técnica y evitando la pérdida del trabajo de los compañeros[cite: 4].

---

## 🏁 Conclusiones del Desarrollo

El tránsito desde los primeros bocetos y diagramas de arquitectura en la fase inicial, hasta la programación de esta robusta interfaz funcional en la fase final, ha sido un reto inmenso. EduPlaner demuestra empíricamente que la separación entre el diseño conceptual y la programación es una ilusión; decisiones aparentemente simples como omitir un *meta tag* pueden destruir la experiencia del usuario, y la implementación de persistencia con *LocalStorage* puede transformar un simple archivo HTML en una herramienta de productividad indispensable[cite: 4]. 

Este proyecto refleja nuestra capacidad para escuchar a los usuarios, maquetar con estándares web modernos, escribir lógica estructurada en JavaScript y trabajar colaborativamente en un entorno real de control de versiones[cite: 4].

---