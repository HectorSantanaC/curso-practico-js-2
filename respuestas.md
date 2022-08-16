## Variables y operaciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una variable y para qué sirve?
Es un elemento que se utiliza para almacenar información.

- ¿Cuál es la diferencia entre declarar e inicializar una variable?
Declarar es simplemente poner nombre a la variable e inicializar es añadir el valor a esa variable.

- ¿Cuál es la diferencia entre sumar números y concatenar strings?
Sumar números es una operación matemática y concatenar strings es unir varios elementos de tipo string.

- ¿Cuál operador me permite sumar o concatenar?
El operador +.

### 2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

Nombre = String
Apellido = String
Nombre de usuario en Platzi = String
Edad = Number
Correo electrónico = String
Mayor de edad = Boolean
Dinero ahorrado = Number
Deudas = Number

### 3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.

```
let nombre = Héctor;
let apellido = Santana;
let NombreDeUsuario = HectorSantanaC;
let edad = 37;
let correoElectronico = ejemplo@gmail.com;
let mayorDeEdad = true;
let dineroAhorrado = 1000;
let deudas = 100;
```

### 4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

Nombre completo (nombre y apellido)
```
let nombreCompleto = nombre + ‘ ‘ + apellido;
```

Dinero real (dinero ahorrado menos deudas)
```
let dineroReal = dineroAhorrado - deudas;
```

## Funciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una función?
Es un conjunto de instrucciones agrupadas para realizar una tarea específica.

- ¿Cuándo me sirve usar una función en mi código?
Cuando necesitemos realizar ciertas acciones con valores que guardamos anteriormente en nuestras variables y reutilizarla mas de una vez en el futuro.

- ¿Cuál es la diferencia entre parámetros y argumentos de una función?
Los parámetros son los elementos que llamamos en nuestra función y los argumentos son los valores de esos elementos.

### 2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
```
```
function saludo(name, lastname, nickname) {
    let completeName = `${name} ${lastname}`;
    return console.log(`Mi nombre es ${completeName}, pero prefiero que me digas ${nickname}`);
}
```

## Condicionales

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un condicional?
Es una estructura que nos devuelve si una expresión es verdadera o falsa para realizar una acción.

- ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?
If, else, else if y switch. Las diferencias son la sintaxis y que switch solo permite trabajar sobre una sola condición mientras que con if podemos introducir varias.

- ¿Puedo combinar funciones y condicionales?
Si.

### 2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

```
const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
   case "Free":
       console.log("Solo puedes tomar los cursos gratis");
       break;
   case "Basic":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       break;
   case "Expert":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       break;
   case "ExpertPlus":
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       break;
}
```
```
let tipoDeSuscripcion = "Basic";

if (tipoDeSuscripcion === "Free") {
    console.log("Solo puedes tomar los cursos gratis");
} else if (tipoDeSuscripcion === "Basic") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
} else if (tipoDeSuscripcion === "Expert") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
} else if (tipoDeSuscripcion === "ExpertPlus") {
    console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
}
```
### 3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).

```
let tipoDeSuscripcion = "Basic";

if (tipoDeSuscripcion === "Free") {
    console.log("Solo puedes tomar los cursos gratis");
}

if (tipoDeSuscripcion === "Basic") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
}

if (tipoDeSuscripcion === "Expert") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
}

if (tipoDeSuscripcion === "ExpertPlus") {
    console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
}
```

> 💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays u objetos y un solo condicional. 😏

```
const tiposDeSuscripciones = {
    Free: "Solo puedes tomar los cursos gratis",
    Basic: "Puedes tomar casi todos los cursos de Platzi durante un mes",
    Expert: "Puedes tomar casi todos los cursos de Platzi durante un año",
    ExpertPlus: "Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"
};

function conseguirTipoDeSuscripcion(suscripcion) {
    if (tiposDeSuscripciones[suscripcion]) {
        console.log(tiposDeSuscripciones[suscripcion]);
        return;
    }
    console.warn('Ese tipo de suscripcion no existe');
}
```

## Ciclos

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un ciclo?
Un ciclo es un bucle que realiza tareas repetitivas en base a una condición hasta que se cumpla.

- ¿Qué tipos de ciclos existen en JavaScript?
For, while y do while.

- ¿Qué es un ciclo infinito y por qué es un problema?
Es cuando en un ciclo nunca se cumple una condición y se repite indefinidamente, y es un problema porque nuestro código se quedaría bloqueado.

- ¿Puedo mezclar ciclos y condicionales?
Si.

### 2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

```
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

let i = 0

while (i < 5) {
    console.log("El valor de i es: " + i);
    i++;
}
```
```
for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}

let i = 10;

while (i >= 2) {
    console.log("El valor de i es: " + i);
    i--;
}
```

### 3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es 2 + 2. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.
> 💡 Pista: puedes usar la función prompt de JavaScript.

```
let respuesta;
    
while (respuesta != '4') {
    let pregunta = prompt('¿Cuanto es 2 + 2?');
    respuesta = pregunta;
}
alert('Felicitaciones!!!');
```

## Listas
### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un array?
Es una lista de elementos

```
const array = [elemento1, elemento2, elemento3...]
```

- ¿Qué es un objeto?
Es una lista de elementos, pero la diferencia es que cada elemento tiene un nombre clave:

```
const objeto = {
    elemento1: nombreElemento1,
    elemento2: nombreElemento2,
    elemento3: nombreElemento3,
}
```

- ¿Cuándo es mejor usar objetos o arrays?
Arrays cuando lo que haremos en un elemento es lo mismo que en todos los demas. Mientras que un objeto cuando los nombres de cada elemento son importantes para nuestro algoritmo.

- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?
Si.

### 2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.

```
function imprimirElPrimerElemento(array) {
		return console.log(array[0]);
}

```
### 3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

```
function imprimirElementosArrayUnoPorUno(array) {
    for (let i = 0; i < array.length; i++) {
        console.log(array[i]);
    }
}
```
### 4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).

```
function imprimirElementoObjetoUnoPorUno(objeto) {
    for (const elemento in objeto) {
        console.log(`${elemento}: ${objeto[elemento]}`);
    }
}
```
```
function imprimirElementosObjetoUnoPorUno(objeto) {
    const array = Object.values(objeto);
    for (let i = 0; i < array.length; i++) {
        console.log(array[i]);
    }
}
```