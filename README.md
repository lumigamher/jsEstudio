

## Fundamentos de JavaScript

### 1. Sintaxis Básica de JavaScript

#### Variables y Tipos de Datos

En JavaScript, las variables se utilizan para almacenar datos que pueden cambiar durante la ejecución del programa. Puedes declarar variables utilizando las palabras clave `var`, `let`, o `const`.

- `var`: Era la forma tradicional de declarar variables en JavaScript, pero su uso ha sido reemplazado en gran medida por `let` y `const`.
- `let`: Permite declarar variables con alcance de bloque, lo que significa que solo están disponibles dentro del bloque en el que fueron declaradas.
- `const`: Similar a `let`, pero el valor de la variable no puede cambiar una vez que se ha asignado.

```js
javascriptCopy code// Declaración de variables
var numero = 10;
let texto = "Hola";
const PI = 3.1416;
```

Los tipos de datos en JavaScript incluyen:

- Números: pueden ser enteros o decimales.
- Cadenas de texto: secuencias de caracteres entre comillas simples o dobles.
- Booleanos: representan un valor de verdad, `true` o `false`.
- Arrays: colecciones ordenadas de datos.
- Objetos: colecciones de pares clave-valor.

```js
javascriptCopy code// Tipos de datos
var numero = 10; // Número
let texto = "Hola"; // Cadena de texto
const PI = 3.1416; // Número (constante)

var esVerdadero = true; // Booleano
var colores = ["rojo", "verde", "azul"]; // Array
var persona = { nombre: "Juan", edad: 30 }; // Objeto
```

#### Operadores

JavaScript incluye una variedad de operadores para realizar operaciones aritméticas, de comparación, lógicas y de asignación.

- Operadores aritméticos: `+` (suma), `-` (resta), `*` (multiplicación), `/` (división), `%` (módulo).
- Operadores de comparación: `==` (igualdad), `!=` (desigualdad), `>` (mayor que), `<` (menor que), `>=` (mayor o igual que), `<=` (menor o igual que).
- Operadores lógicos: `&&` (AND lógico), `||` (OR lógico), `!` (NOT lógico).
- Operadores de asignación: `=` (asignación), `+=`, `-=`, `*=`, `/=`.

```js
javascriptCopy code// Operadores aritméticos
var suma = 5 + 3; // 8
var resta = 10 - 4; // 6
var multiplicacion = 2 * 6; // 12
var division = 20 / 5; // 4

// Operadores de comparación
var x = 10;
var y = 5;
console.log(x > y); // true
console.log(x == y); // false

// Operadores lógicos
var a = true;
var b = false;
console.log(a && b); // false
console.log(a || b); // true
console.log(!a); // false

// Operadores de asignación
var c = 10;
c += 5; // Equivalente a: c = c + 5;
console.log(c); // 15
```



### Estructuras de Control

Las estructuras de control en JavaScript te permiten controlar el flujo de ejecución de tu código, permitiendo tomar decisiones y repetir bloques de código según sea necesario.

#### Sentencia if

La sentencia `if` se utiliza para ejecutar un bloque de código si una condición específica es verdadera. También puedes usar `else` para ejecutar un bloque de código alternativo si la condición es falsa.

```js
javascriptCopy codevar edad = 18;

if (edad >= 18) {
    console.log("Eres mayor de edad");
} else {
    console.log("Eres menor de edad");
}
```

#### Sentencia else if

La sentencia `else if` te permite evaluar múltiples condiciones en secuencia.

```js
javascriptCopy codevar hora = 14;

if (hora < 12) {
    console.log("Buenos días");
} else if (hora < 18) {
    console.log("Buenas tardes");
} else {
    console.log("Buenas noches");
}
```

#### Sentencia switch

La sentencia `switch` permite evaluar una expresión y ejecutar diferentes bloques de código dependiendo del valor de esa expresión.

```js
javascriptCopy codevar diaDeLaSemana = "Lunes";

switch (diaDeLaSemana) {
    case "Lunes":
        console.log("Hoy es lunes");
        break;
    case "Martes":
        console.log("Hoy es martes");
        break;
    default:
        console.log("Hoy no es lunes ni martes");
}
```

#### Bucles

JavaScript admite varios tipos de bucles para repetir bloques de código.

- Bucle `for`: Se utiliza para repetir un bloque de código un número específico de veces.
- Bucle `while`: Se ejecuta mientras una condición específica sea verdadera.
- Bucle `do-while`: Similar a `while`, pero siempre se ejecuta al menos una vez, incluso si la condición es falsa.

```js
javascriptCopy code// Bucle for
for (var i = 0; i < 5; i++) {
    console.log("Iteración #" + i);
}

// Bucle while
var contador = 0;
while (contador < 3) {
    console.log("Contador: " + contador);
    contador++;
}

// Bucle do-while
var x = 0;
do {
    console.log("x = " + x);
    x++;
} while (x < 5);
```





## Clase Date()

#### Constructor sin Argumentos

Si no pasas ningún argumento al constructor `Date`, se crea un objeto que representa la fecha y hora actuales en el momento en que se crea el objeto.

```js
let fechaActual = new Date();
console.log(fechaActual); // Muestra la fecha y hora actuales
```

#### Constructor con Argumentos

```js
new Date()
new Date(*date string*)

new Date(*year,month*)
new Date(*year,month,day*)
new Date(*year,month,day,hours*)
new Date(*year,month,day,hours,minutes*)
new Date(*year,month,day,hours,minutes,seconds*)
new Date(*year,month,day,hours,minutes,seconds,ms*)

new Date(*milliseconds*)
```

Puedes pasar diferentes argumentos al constructor `Date` para especificar una fecha y hora específicas. Estos argumentos pueden ser el año, mes (0-11), día, hora, minuto, segundo y milisegundo.

```js
let fechaEspecifica = new Date(2024, 1, 9, 12, 30, 0);
console.log(fechaEspecifica); // Muestra la fecha y hora especificadas
```

### Métodos de la Clase Date

La clase `Date` tiene varios métodos útiles para trabajar con fechas y horas.

#### Obtener Componentes de la Fecha y Hora

Puedes obtener los componentes individuales de una fecha, como el año, mes, día, hora, minuto, segundo, etc.

```js
let fecha = new Date();
let año = fecha.getFullYear(); // Obtener el año (ej. 2024)
let mes = fecha.getMonth(); // Obtener el mes (0-11, donde 0 es enero)
let dia = fecha.getDate(); // Obtener el día del mes (1-31)
let hora = fecha.getHours(); // Obtener la hora (0-23)
let minuto = fecha.getMinutes(); // Obtener los minutos (0-59)
let segundo = fecha.getSeconds(); // Obtener los segundos (0-59)
let milisegundo = fecha.getMilliseconds(); // Obtener los milisegundos (0-999)
let diaSemana = fecha.getDay(); // Obtener el día de la semana (0-6, donde 0 es domingo)
```

#### Establecer Componentes de la Fecha y Hora

También puedes establecer los diferentes componentes de una fecha utilizando métodos similares con el prefijo `set`.

```js
fecha.setFullYear(2025);
fecha.setMonth(2); // Marzo (0-11)
fecha.setDate(15);
fecha.setHours(16);
fecha.setMinutes(30);
fecha.setSeconds(0);
fecha.setMilliseconds(0);
```

#### Formatos de Fechas

JavaScript proporciona métodos para formatear fechas en diferentes formatos.

```js
let fecha = new Date();
let formato1 = fecha.toString(); // "Tue Feb 09 2024 12:30:00 GMT+0000 (UTC)"
let formato2 = fecha.toDateString(); // "Tue Feb 09 2024"
let formato3 = fecha.toISOString(); // "2024-02-09T12:30:00.000Z"
let formato4 = fecha.toLocaleDateString(); // Formato local dependiendo de la configuración regional del sistema
let formato5 = fecha.toLocaleTimeString(); // Formato de hora local
```

### Operaciones con Fechas

La clase `Date` también permite realizar operaciones con fechas, como la adición o resta de días, horas, etc.

```js
let fecha = new Date();

// Sumar un día
fecha.setDate(fecha.getDate() + 1);

// Restar 5 horas
fecha.setHours(fecha.getHours() - 5);

// Comparar fechas
let otraFecha = new Date(2024, 1, 10);
if (fecha.getTime() === otraFecha.getTime()) {
    console.log("Las fechas son iguales");
} else {
    console.log("Las fechas son diferentes");
}
```

### Timezones (Zonas Horarias)

La clase `Date` en JavaScript maneja las fechas y horas en el huso horario local del sistema en el que se está ejecutando el código. Esto significa que la fecha y la hora pueden variar según la configuración del huso horario del sistema.	

```js
let fecha = new Date(); // Fecha y hora actual en el huso horario local
```

Sin embargo, también puedes crear fechas en un huso horario específico utilizando los métodos `setUTC*()` o pasando un offset de tiempo en milisegundos.

### Parseo de Fechas

Puedes parsear una cadena de texto que representa una fecha en un objeto `Date` utilizando el constructor `Date` con la cadena de texto como argumento.

```js
let fecha = new Date("2024-02-09T12:30:00.000Z"); // Parsear una cadena de texto en formato ISO
```

### Gestión de Fechas Futuras y Pasadas

Puedes comparar fechas para determinar si una fecha es anterior, posterior o igual a otra.

```js
let fecha1 = new Date(2024, 1, 9);
let fecha2 = new Date(2024, 1, 10);

if (fecha1 < fecha2) {
    console.log("fecha1 es anterior a fecha2");
} else if (fecha1 > fecha2) {
    console.log("fecha1 es posterior a fecha2");
} else {
    console.log("fecha1 es igual a fecha2");
}
```

### Funciones Estáticas de la Clase Date

La clase `Date` también tiene funciones estáticas que pueden ser útiles para trabajar con fechas, como `now()`, que devuelve el número de milisegundos transcurridos desde el 1 de enero de 1970 hasta el momento actual.

```js
let milisegundosTranscurridos = Date.now();
console.log(milisegundosTranscurridos); // Número de milisegundos desde el 1 de enero de 1970
```





