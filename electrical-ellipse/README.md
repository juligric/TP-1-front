Descripción

Esta aplicación es un organizador de tareas tipo tablero (estilo Trello) desarrollado con Astro, HTML, CSS y JavaScript.

Permite al usuario crear, organizar y mover tareas entre distintas columnas de forma visual y simple.


Funcionalidades principales
- Agregar nuevas tareas
-  Eliminar tareas
- Mover tareas entre columnas con drag & drop
- Contador automático de tareas por columna
-  Guardado automático en el navegador (localStorage)
- Modo oscuro


Como funciona 
La aplicación se basa en un array de tareas que se guarda en el navegador.

Cada tarea tiene esta estructura:

{
  text: "Hacer tarea",
  status: "todo" // puede ser: todo, progress o done
}

Funcionamiento cada paso 

1. Cargar los datos
Cuando se abre la app:

Se buscan las tareas en localStorage
Si no hay nada, se empieza con un array vacío
let tasks = JSON.parse(localStorage.getItem("tasks")) || [];

2. renderizado de tareas

La función render():

Limpia las columnas
Recorre todas las tareas
Las dibuja en la columna correspondiente
Actualiza los contadores

3. Agregar tareas

Cuando el usuario escribe y toca "Agregar":

Se crea una nueva tarea
Se guarda en el array
Se actualiza la pantalla

4. Drag & Drop

Las tareas se pueden arrastrar entre columnas:

Se guarda el índice de la tarea
Al soltarla, se cambia su status
Se vuelve a renderizar

5. Guardado automático

Cada cambio se guarda en el navegador:
localStorage.setItem("tasks", JSON.stringify(tasks));
Esto permite que las tareas no se pierdan al recargar la página.

6. Modo oscuro 🌙

El botón activa o desactiva una clase en el body:
document.body.classList.toggle("dark");
Y el estilo cambia con CSS.

6. Diseño
Diseño tipo tablero (3 columnas)
Estilo moderno con sombras y bordes redondeados
Responsive (funciona en celular)
Animaciones suaves al interactuar

7. Estructura del proyecto
src/
 ├── components/
 │    └── TaskApp.astro
 ├── layouts/
 │    └── Layout.astro
 └── pages/
      └── index.astro

public/
 └── (assets como imágenes)

 