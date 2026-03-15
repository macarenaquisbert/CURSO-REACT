# 📂 Estructura Básica de un Documento

Cada vez que creas un archivo .html, esta es la jerarquía de selección:

<html>: La caja madre que contiene todo.

<head>: Lo que no se ve (configuración, título de la pestaña).

<body>: Lo que sí se ve (el contenido).

HTML
<!DOCTYPE html>
<html lang="es">
<head>
    <title>Mis Apuntes</title>
</head>
<body>
    <div class="contenedor">
        <h1>¡Hola Mundo!</h1>
    </div>
</body>
</html>

---

## 🧠 ¿Qué más va en el <head>?
El <head> contiene los Metadatos. Sirve para configurar el idioma, los caracteres especiales (como la ñ o los acentos) y para conectar tu archivo HTML con otros archivos (estilos y lógica).

* **1. Conectar el estilo (CSS)**
Para que tus cajas <div> no sean simples bloques blancos y negros, usamos la etiqueta <link>.

¿Para qué sirve? Para traer el archivo de diseño.

Comando: <link rel="stylesheet" href="estilos.css">

* **2. Conectar la lógica (JavaScript)**
Para que tu página tenga movimiento o funciones (como un botón que salude), usamos la etiqueta <script>.

¿Para qué sirve? Para traer el archivo de programación.

Comando: <script src="script.js"></script>

Tip de Pro: Se suele poner al final del <body> para que la página cargue más rápido, pero también puede ir en el <head>.

* **3. Configuración esencial (Meta Tags)**
<meta charset="UTF-8">: Sirve para que se vean bien las ñ y los acentos. Sin esto, verás símbolos raros.

<meta name="viewport"...>: Es lo que hace que tu página se vea bien en celulares (Responsive Design).

* **📂 Estructura Completa y "Profesional"**
Copia este código en tu README para tener la plantilla definitiva:

HTML
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <title>Mis Apuntes Pro</title>

    <link rel="stylesheet" href="style.css">

    <script src="app.js" defer></script> 
    </head>
<body>
    <div class="contenedor">
        <h1>¡Ahora mi Head está completo!</h1>
    </div>
</body>
</html>


---

## 🧱 Estructura HTML: El esqueleto de la Web

### 📦 ¿Qué es un `<div>`?
El `div` (Division) es una caja invisible. No tiene forma ni color por sí sola, sirve para **agrupar** otros elementos y ordenarlos.



* **¿Para qué sirve?** Para crear secciones en tu página (cabecera, cuerpo, pie de página).
* **¿Cómo funciona?** Es un elemento en bloque, lo que significa que ocupa todo el ancho disponible y salta a la siguiente línea.

```html
<div>
  <h1>Título dentro de una caja</h1>
  <p>Este párrafo está agrupado con el título.</p>
</div>

---

## 🏷️ Etiquetas Esenciales en el `<body>`

No todo es `div`. Para que Google entienda tu página y sea accesible, usamos etiquetas con significado (Semántica).

### 1. Títulos y Textos
* `<h1>` a `<h6>`: Títulos. El `<h1>` es el más importante (solo debe haber uno por página).
* `<p>`: Para párrafos de texto.
* `<span>`: Para textos cortos dentro de un párrafo que quieres resaltar (es como un `div` pero no salta de línea).
* `<a>`: Enlaces o links. Usa el atributo `href` para decir a dónde va.
    * Ejemplo: `<a href="https://google.com">Ir a Google</a>`

### 2. Listas (Para organizar apuntes)
* `<ul>`: Lista desordenada (con puntitos).
* `<ol>`: Lista ordenada (con números 1, 2, 3).
* `<li>`: Cada elemento dentro de la lista.



### 3. Multimedia
* `<img>`: Para imágenes. Usa `src` (la fuente/ruta) y `alt` (descripción por si no carga).
    * Ejemplo: `<img src="foto.jpg" alt="Mi foto de perfil">`

---

## 🍱 Etiquetas Semánticas (El Orden "Pro")
En lugar de usar `div` para todo, usa estas etiquetas para que tu código sea profesional:

| Etiqueta | Para qué sirve |
| :--- | :--- |
| `<header>` | El encabezado de la página. |
| `<nav>` | El menú de navegación (links). |
| `<main>` | El contenido principal y único. |
| `<section>` | Para agrupar temas relacionados. |
| `<article>` | Un contenido que se entiende por sí solo. |
| `<footer>` | El pie de página (contactos, redes). |

---

## 🧠 ¿Qué es `href` vs `src`?

* **`href` (Hypertext Reference):** Se usa para **referenciar** una ubicación (ir a otro lugar).
    * *Se usa en:* `<a>` y `<link>`.
* **`src` (Source):** Se usa para **traer un recurso** (meter algo adentro de la página).
    * *Se usa en:* `<img>` y `<script>`.

---

## 📂 Estructura Completa del Documento

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mis Apuntes</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <nav>Menú de navegación</nav>
    </header>

    <main>
        <section>
            <h1>Bienvenido a mis apuntes</h1>
            <p>Aquí explico cómo funciona el body.</p>
        </section>
    </main>

    <footer>
        <p>Creado por Macarena</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>

