# 🚀 Entendiendo la POO: De Moldes a Personajes

La **Programación Orientada a Objetos** es un paradigma que nos ayuda a organizar el código pensando en objetos de la vida real.

---

## 💡 Conceptos Clave

### 1. La Clase (El Molde)
Imaginate que sos un desarrollador de videojuegos y necesitás crear 100 aldeanos. No vas a programar uno por uno. Creás un **molde** (la Clase) que dice: *"Todos los aldeanos tienen nombre, ropa y salud"*.

* **El Constructor:** Es el momento en que el molde se rellena. Es cuando decís: 
*"Este aldeano se va a llamar Juan"*.



### 2. El Objeto (El Personaje real)
Es el aldeano que ya está caminando por el juego. Tiene sus propios datos, pero nació 
del mismo molde que los demás.

### 3. La Herencia (Evolución)
Ahora querés crear un **Aldeano Guerrero**. No necesitás empezar de cero. "Heredás" todo
lo del aldeano normal (nombre, ropa) y solo le agregás lo nuevo: **una espada**.



[Image of object oriented programming inheritance diagram]


---

## 💻 Resolución de Ejercicios

### 📂 EJERCICIO 1: Creando la base
Aquí creamos al `Ciudadano` original, definiendo sus propiedades y su método principal.

```javascript
// Definimos el "molde"
class Ciudadano {
    constructor(nombre, apellido, dni) {
        this.nombre = nombre;     // "this" es como decir "la propiedad de este objeto"
        this.apellido = apellido;
        this.dni = dni;
    }

    // Una acción que todos los ciudadanos saben hacer
    mostrar() {
        return `El ciudadano ${this.nombre} ${this.apellido}, tiene el siguiente número de dni: 
        ${this.dni}`;
    }
}

// Creamos 3 personas reales (Instancias)
const persona1 = new Ciudadano("Juan", "Pérez", "12345678");
const persona2 = new Ciudadano("María", "García", "87654321");
const persona3 = new Ciudadano("Carlos", "Rodríguez", "11223344");

// Les pedimos que ejecuten su acción
console.log(persona1.mostrar());
console.log(persona2.mostrar());
console.log(persona3.mostrar());

---

### EJERCICIO 2: Aplicando Herencia
Acá creamos una versión "específica" del Ciudadano llamada AltaBajaCiudadano.

JavaScript
// "extends" significa que AltaBajaCiudadano es un hijo de Ciudadano
class AltaBajaCiudadano extends Ciudadano {
    constructor(nombre, apellido, dni, activo) {
        // "super" le pasa los datos al padre para que él los acomode
        super(nombre, apellido, dni); 
        this.activo = activo; // Esta es la característica nueva
    }

    // Esta es una acción nueva que solo los "AltaBaja" tienen
    mostrarEstado() {
        return `${this.activo} se encuentra activo`;
    }
}

// Creamos dos personas con este nuevo molde
const userSi = new AltaBajaCiudadano("Ana", "Martínez", "44556677", "SI");
const userNo = new AltaBajaCiudadano("Pedro", "López", "99887766", "NO");

// Probamos su nueva habilidad
console.log(userSi.mostrarEstado());
console.log(userNo.mostrarEstado());

---

** 🔑 Tips para no olvidarte:**

## Resumen de palabras clave

class: Define el molde.

this: Hace referencia al objeto que se está creando/usando en ese momento.

new: La palabra mágica que crea el objeto real (la instancia).

extends: Indica que una clase es hija de otra.

super(): Función obligatoria en herencia para pasarle datos al "padre".

** Nota de estilo: En JavaScript, por convención, los nombres de las clases siempre 
empiezan con Mayúscula (PascalCase), mientras que los objetos y métodos empiezan con 
minúscula (camelCase).** 