# EduPlaner - Maquetado semántico HTML5

Actividad de maquetado semántico y accesibilidad web sobre el prototipo de la pantalla de calendario académico de EduPlaner.

## Requisitos de la actividad

- [x] Seleccionar una pantalla del prototipo.
- [x] Marcar `header`, `nav`, `main`, `section`, `article`, `aside` y `footer` según corresponda.
- [x] Crear `index.html` con contenido real.
- [x] Aplicar `alt`, `lang`, `label`, `id` y `for`.
- [x] Realizar al menos cinco commits significativos.
- [ ] Presentar informe en formato PDF.

## Pantalla seleccionada

Pantalla de calendario académico de EduPlaner, que incluye: encabezado con logo y perfil, calendario mensual navegable, acordeón de materias y listado de exámenes con checkboxes, y pie de página con acciones principales.

## Etiquetas semánticas aplicadas

| Etiqueta | Dónde se usó en `index.html` |
|---|---|
| `header` | Título "EduPlaner" y foto de perfil del usuario |
| `nav` | Navegación entre meses del calendario, acordeón de materias, y botones del footer |
| `main` | Contenedor central que agrupa calendario, materias y exámenes |
| `section` | Bloque de calendario y bloque de exámenes |
| `article` | Cada examen individual (Desarrollo, Programación, Base de datos, Redes, Sistema Operativo, IA) |
| `footer` | Botones "Regresar al inicio" y "Mis proyectos" |

`aside` no se utilizó porque la pantalla no presenta contenido complementario independiente del flujo principal.

## Atributos de accesibilidad aplicados

- `lang="es"` en `<html>`.
- `alt="Foto de perfil del usuario"` en la imagen del header.
- `label` + `for` en cada checkbox de examen y en el selector de año del calendario.
- `id` único en cada elemento referenciado por `label`, `aria-controls` y `aria-labelledby`.

## Historial de commits (mínimo 5, entre 2 personas)

| # | Commit | Responsable |
|---|---|---|
| 1 | Agrega estructura semantica base: header, main, footer | Isaac Carrion |
| 2 | Implementa seccion de calendario con navegacion de mes | Wilmer Calapaqui |
| 3 | Agrega nav de materias con acordeon y atributos ARIA | Isaac Carrion |
| 4 | Agrega seccion de examenes con checkboxes accesibles (label y for) | Wilmer Calapaqui |
| 5 | Aplica ajustes finales de accesibilidad (lang, alt, id, label-for) | Isaac Carrion |

## Pendiente

- Exportar el informe en PDF con la justificación de cada etiqueta semántica usada.

## Autores

- Isaac Carrion
- Wilmer Calapaqui
---

## Módulo: Lista de Tareas (Isaac Carrion)

Maquetación y diseño visual de la sección de gestión de tareas.

### Archivos
* `lista_tareas.html`

### Funcionalidades maquetadas
* **Panel multimedia superior:** Tarjetas visuales promocionales e informativas.
* **Filtros de estado:** Botones para clasificar actividades (`Añadir al calendario`, `Pendiente`, `Realizadas`).
* **Listado por asignaturas:** Tarjetas organizadas con iconos, títulos y descripciones de las materias.
* **Navegación lateral:** Enlaces de acceso rápido a funciones del panel.

### Vista previa local
```text
http://localhost:5500/lista_tareas.html