Task Board App

App tipo Kanban hecha con Astro, HTML, CSS y JavaScript.  crear, mover y eliminar tareas en tres columnas: To Do, In Progress y Done. Usa drag and drop y guarda los datos en localStorage.

Funciones
Crear tareas
Mover tareas entre columnas
Eliminar tareas
Contadores por estado
Modo oscuro
Persistencia local
Estructura de datos

Cada tarea es un objeto con texto y estado:
{ text, status }

Estructura del proyecto

/src
components/TaskApp.astro
layouts/Layout.astro
pages/index.astro

Uso

Instalar dependencias con npm install
Ejecutar con npm run dev
Abrir en http://localhost:4321

Nota

No usa backend, los datos se guardan en el navegador.
