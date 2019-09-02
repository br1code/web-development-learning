Javascript es un lenguaje de programación/scripting que nos permite modificar el comportamiento de la página y actuar en base a la interacción del usuario.

Por ejemplo, si el usuario le da click a un botón, en nuestro Javascript podemos tener definido que es lo que va a pasar.

Las bases de este lenguaje son muy parecidas a cualquier otro lenguaje.

Leen y ejecutan línea por línea, podes hacer operaciones matemáticas, podes trabajar con textos, ejecutar una acción o la otra según tal condición, podes hacer cosas repetitivas sin limite alguno, etc.

Pero primero vayamos con lo primero, **declarar una variable**.

## Variables

Una variable es un valor que se guardará en la memoria y que le podes dar un nombre para identificarlo. Por ejemplo, si necesitas almacenar el nombre de tu gato para luego utilizarlo varias veces durante tu página, lo ideal es declarar una variable con el valor, con un nombre relacionado al mismo.

> Para practicar, podemos usar la consola de un navegador para escribir código Javascript.

```js
// Declarar una variable consiste en la palabra *var*, 
// seguido del nombre de la variable 
// seguido de un signo igual =
// seguido del valor
// y al final un punto y coma ;
var nombreVariable = 'valorDeLaVariable';
```

Para obtener el valor de nuestra variable, simplemente la escribimos por su nombre

```js
nombreVariable
```

Ejemplo de uso:

```js
// Definimos nuestra variable
var mensaje = 'Plata o Plomo';

// La utilizamos en otro lugar del código. El valor está guardado en memoria.
alert(mensaje);
```

> alert es una función que muestra una alerta con un mensaje. Mas tarde vamos a saber que es una función

Una variable luego de inicializarse, puede sobreescribir su valor. Por ejemplo:

```js
var nombre = 'Pepito';

alert(nombre); // Muestra un mensaje de alerta con el texto 'Pepito'

nombre = 'Carlitos'; // Editamos el valor de la variable

alert(nombre); // Ahora muestra un mensaje de alerta con el texto 'Carlitos'
```

> Recordar que el código se va leyendo y ejecutando **"línea por línea"**.

---
## Tipos de Datos
Ahora que sabemos definir una variable, vamos a conocer los tipos de datos mas comúnes en Javascript.

#### String (cadena de texto)
En el ejemplo de recién, definimos una variable con un valor del tipo texto, o mejor dicho cadena de texto (llamado **string**). Los strings se escriben entre comillas (pueden ser comillas simples o no).

```js
var variableDeTexto = 'Este es un string';
```

Un string puede ser sobreescrito por otro string

```js
var variableDeTexto = 'Este es un string';
variableDeTexto = 'Este es el nuevo string';
```
Un string puede concatenarse con otro string, devolviendo un nuevo string. Se utiliza el **operador +**

```js
var variableDeTexto = 'Este es un string';
var otraVariableDeTexto = ' y este es otro string';

// Muestra una alerta con el texto: 'Este es un string y este es otro string'
alert(variableDeTexto + otraVariableDeTexto);
```

```js
var mensaje = 'Las rosas';

mensaje = mensaje + ' son rojas';

// Muestra una alerta con el texto: 'Las rosas son rojas'
alert(mensaje);
```

### Int (Enteros/Números enteros)
Un ``int`` es un número sin decimales. Es uno de los tipos de datos más utilizados. Con los ``int`` se pueden utilizar los operadores aritméticos para realizar sumas, restas, divisiones, etc.

```js
var numero = 5;
```

Podemos hacer sumas
```js
var numeroUno = 5;
var numeroDos = 8;

var suma = numeroUno + numeroDos;

// Muestra una alerta con el valor: 13
alert(suma);
```

> Si, la función **alert** tambien puede recibir un número. Lo interpretará como un string '13'.

Otros ejemplos

```js
var numeroUno = 5;
var numeroDos = 8;

var resta = numeroUno - numeroDos;
var multiplicacion = numeroUno * numeroDos;
var division = numeroUno / numeroDos;

numeroUno = numeroUno + 1; // numeroUno ahora tiene como valor 6
numeroUno += 1; // Este es una atajo a la linea de arriba
numeroUno = numeroUno - 2; // numeroUno ahora tiene como valor 4
```

No hay límite a la hora de juntar operadores aritméticos.

```js
var resultado = 1 + 2 - 3 * 4 / 5;
```

### Boolean (Booleano)
Este tipo de dato es el mas importante de cualquier lenguaje de programación. El tipo de dato booleano tiene dos posibles valores: **true** (verdadero) o **false** (falso).

Se utilizan para definir una condición: *Si esto es verdadero, entonces ejecutá esta acción*.

En un rato los vamos a usar bastante, pero dejo algunos ejemplos.

```js
var soyMayorDeEdad = true;
var soyMenorDeEdad = false;
```

Con los booleanos, generalmente se utilizan los operadores de comparación.

Los operadores de comparación sirven para ... comparar. Por ejemplo comparar si un numero es mayor que el otro, o si son iguales, o si uno es mayor o igual que el otro. Se entiende.

Operadores

- **Igual** ``==`` Ejemplo: ``5 == 5`` Cinco es igual a Cinco?
- **Mayor que** ``>`` Ejemplo: ``6 > 5`` Seis es mayor que Cinco?
- **Menor que** ``<`` Ejemplo ``4 < 8`` Cuatro es menor que Ocho?
- **Mayor o igual que** ``>=`` Ejemplo ``3 >= 3`` Tres es mayor o igual que Tres?
- **Menor o igual que** ``<=`` Ejemplo ``4 <= 3`` Cuatro es menor o igual que Tres?

Utilizar un operador de comparación con dos o más valores, devuelven un valor booleano con el resultado de la comparación.

```js
var numeroUno = 4;
var numeroDos = 5;

// La comparación es evaluada, devolviendo un booleano con el resultado
var sonIguales = numeroUno == numeroDos;
// la variable sonIguales ahora tiene como valor false
```

Veamos más ejemplos

```js
var numeroUno = 7;
var numeroDos = 8;

numeroUno > numeroDos; // false
numeroUno < numeroDos; // true
numeroUno >= numeroDos; // false
numeroUno <= numeroDos; // true
numeroUno == numeroDos; // false

// El operador de Igual también se puede usar con strings
var contraseñaEncriptada = 'pepito123';
var contraseñaIngresada = 'peputo123';

var sonIguales = contraseñaEncriptada == contraseñaIngresada; // false
```

---

Ya estamos mas que preparados para empezar a hacer algunos ejercicios. En el módulo 2 de JavaScript vamos a conocer las **Funciones**, los **Objetos** y las **Listas**.