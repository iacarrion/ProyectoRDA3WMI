# EduPlaner

Plataforma web para ayudar a estudiantes a organizar tareas, proyectos, fechas de entrega y su progreso académico en un solo lugar.

## Descripción

EduPlaner centraliza la gestión académica del estudiante mediante pantallas dedicadas a tareas, calendario, recordatorios, proyectos, herramientas de filtrado, progreso por materia, registro, ayuda y configuración de usuario.

## Estructura del proyecto

```
ProyectoRDA3WMI/
│
├── inicio_escritorio.html          # Pantalla de inicio
├── Tareas_escritorio.html           # Gestion de tareas
├── calendario_escritorio.html        # Calendario academico (tema morado)
├── calendario_mobil.html             # Calendario (version mobile)
├── Progreso_escritorio.html          # Progreso academico y tendencias (tema verde)
├── progresotablet.html                # Progreso (version tablet)
├── herramientas_escritorio.html       # Filtros y herramientas (escritorio)
├── herramientas_mobile.html           # Filtros y herramientas (mobile)
├── configuracion_escritorio.html      # Configuracion de usuario
├── proyectos_escritorio.html          # Gestion de proyectos
├── proyectos_mobile.html               # Gestion de proyectos (mobile)
├── ayuda_escritorio.html               # Ayuda y soporte (escritorio)
├── ayuda_mobile.html                    # Ayuda y soporte (mobile)
├── registro.html                        # Registro de nuevos usuarios
│
├── scss/
│   ├── _variables.scss     # Tokens de diseno (colores, tipografia, espaciados, radios)
│   ├── _header.scss         # Estilos del encabezado
│   ├── _hero.scss            # Estilos de la seccion "Quienes somos" y botones
│   ├── _cards.scss           # Estilos de tarjetas e inputs
│   └── styles.scss            # Archivo principal, importa los partials
│
├── css/
│   ├── styles.css               # CSS compilado/editado, usado directamente por el HTML
│   └── styles.css.map           # Mapa de fuente (uso interno de depuracion)
│
└── README.md
```

> **Nota:** `css/styles.css` es la hoja de estilos general del proyecto. Contiene los estilos base del UI Kit (variables, header, hero, botones, tarjetas, inputs) mas los estilos especificos de cada pantalla nueva agregada (registro, calendario, progreso), todos reutilizando las mismas variables de color, tipografia y espaciado.

## Tecnologías utilizadas

- **HTML5** semántico
- **CSS3** con variables (custom properties) y **SCSS** como base del sistema de diseño
- **JavaScript** vanilla para componentes interactivos (acordeón de materias)
- **Git y GitHub** para control de versiones (flujo de ramas individuales y pull requests)
- Diseño basado en un **UI Kit** definido en Figma

## Pantallas del proyecto

### Trabajadas en la actividad grupal
- **Inicio**: pantalla principal con navegación a todas las secciones.
- **Tareas**: lista de tareas, agregar, editar y ver actividades pendientes.
- **Herramientas**: filtros por materia, prioridad, fecha de entrega, estado y tipo de actividad.
- **Configuración**: gestión de usuarios, perfil, accesibilidad y cierre de sesión.
- **Progreso**: gráfico comparativo de tendencias y avance por materia.

### Agregadas por el equipo (posterior a la actividad grupal)
- **Ayuda**: tutorial de uso y mensajes de soporte para el usuario (versiones escritorio y mobile).
- **Lista de tareas ampliada**: mejoras sobre la pantalla de tareas original.

### Trabajo individual (pantallas nuevas, no cubiertas en grupo)
- **Registro** *(rama personal: `feature/pantalla-registro`)*: formulario de creación de cuenta, reutilizando `.input`, `.btn`, tipografía y espaciados del UI Kit. Incluye componente de **alerta de error** y mensajes de validación por campo.
- **Calendario** *(rama personal: `feature/pantalla-calendario`)*: calendario académico con tema morado, replicado desde el diseño de Figma. Incluye **acordeón interactivo** de materias (JavaScript) y lista de exámenes con checklist.
- **Mejoras a Progreso** *(rama personal: `feature/pantalla-progreso-color`)*: aplicación del tema verde del Figma, gráfico SVG de tendencias, y componentes adicionales de **alerta de resumen** y **barras de progreso con porcentaje** por materia.

## Cómo ejecutar el proyecto

No requiere instalación ni servidor. Basta con abrir cualquier archivo `.html` directamente en el navegador (doble clic, o "Abrir con Live Server" desde VS Code).

Si se realizan cambios en los archivos `.scss`, deben recompilarse a CSS:

```bash
npm install -g sass
sass scss/styles.scss css/styles.css
```

Actualmente, `css/styles.css` se mantiene y edita de forma directa para agilizar el desarrollo; se recomienda sincronizarlo periódicamente con los archivos `.scss` fuente.

## Flujo de trabajo en equipo

El desarrollo se organizó mediante ramas individuales por integrante y por funcionalidad:

```bash
git checkout main
git pull origin main
git checkout -b feature/nombre-de-la-tarea

# ... cambios y commits ...

git push origin feature/nombre-de-la-tarea
```

Luego se abre un **Pull Request** en GitHub para revisar y fusionar los cambios a la rama `main`. En caso de conflictos (por ejemplo, en `css/styles.css` al integrar cambios de varias ramas), se resuelven localmente antes de completar la fusión:

```bash
git checkout <tu-rama>
git merge main
# resolver conflictos manualmente
git add .
git commit -m "Resuelve conflicto de fusion"
git push origin <tu-rama>
```

## Pull Requests destacados

| Rama | Pantalla | Enlace |
|---|---|---|
| `feature/pantalla-registro` | Registro | _agregar enlace_ |
| `feature/pantalla-calendario` | Calendario | https://github.com/iacarrion/ProyectoRDA3WMI/pull/13 |
| `feature/pantalla-progreso-color` | Progreso (estilos y componentes) | _agregar enlace_ |

## Equipo

- Wilmer Calapaqui
- Isaac Carrion
- Marco Luna


## Licencia

Proyecto académico desarrollado con fines educativos.