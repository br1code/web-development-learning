#  JavaScript - 5

Hoy vamos a aprender todo sobre **funciones** en JavaScript.

Una **función** es otro tipo de dato en JavaScript.

> Cuando hablamos de  un **tipo de dato**, podemos decir que es algo que podemos almacenar en una variable, como los ``string`` o los ``boolean``.

Pero las **funciones** no están hechas para almacenar datos estáticos, sino que están hechas para **encapsular código**.

Pero ... para que quisiéramos encapsular código? Hay varias razones, veamos una con el siguiente ejemplo:

```js
var ovejasContadas = 0;
var continuarDurmiendo = true;

while (continuarDurmiendo) {
    var excusa = prompt('Por qué seguís durmiendo?');
    
    switch (excusa) {
        case 'tengo sueño':
            alert('Todavía tenes sueño? Enserio?!?');
            alert('Bueno,seguí durmiendo...');
            ovejasContadas++;
            break;
            
        case 'hace frio':
            alert('Frio? Pero si hace 40 grados?!?');
            alert('Bueno,seguí durmiendo...');
            ovejasContadas++;
            break;
            
        case 'es temprano':
            alert('Temprano? Son las 3 de la tarde?!?');
            alert('Bueno,seguí durmiendo...');
            ovejasContadas++;
            break;
            
        default:
            alert('No me convence tu excusa, a levantarse!');
            alert('Contaste ' + ovejasContadas + ' ovejas...');
            continuarDurmiendo = false;
            break;
    }
}
```

En este ejemplo, simulamos una conversación entre la mente de una persona y la persona en si, mientras esta duerme a altas horas de la tarde.

Quiero hacerles una pregunta: **Cuántas veces se repite esta porción de código en este ejemplo?**

```js
alert('Bueno,seguí durmiendo...');
ovejasContadas++;
```

Se repite unas tres veces .. no? No parece la gran cosa. Pero que pasa si queremos poder soportar mas excusas? 

- Si la persona se siente mal? 
- Si la persona no pudo dormir en toda la noche?
- Si en realidad son las 6 de la mañana?

Para esto habría que ir agregando muchos ``case``, y esto implica que vamos a tener que seguir repitiendo este código, una y otra vez.  Y que pasa si además de decirle que siga durmiendo y de contar otra oveja, necesitamos hacer más cosas como por ejemplo posponer la alarma? Nuestro código se repetiría cada  vez mas.

Que pasa si les digo que hay una forma de evitar esto? **Funciones**.

```js
function seguirDurmiendo() {
    alert('Bueno,seguí durmiendo...');
	ovejasContadas++;
}
```

Con las **Funciones** podemos encapsular una porción de código, y darle un nombre para luego reutilizarla. Evitando que escribamos código repetido.

Ahora cada vez que necesitemos ejecutar esta porción de código, podemos **llamar** a nuestra función de la siguiente manera:

```js
seguirDurmiendo();
```

Por lo tanto, nuestro programa de dormir quedaría de la siguiente forma:

```js
var ovejasContadas = 0;
var continuarDurmiendo = true;

// Definimos nuestra nueva función
function seguirDurmiendo() {
    alert('Bueno,seguí durmiendo...');
	ovejasContadas++;
}

while (continuarDurmiendo) {
    var excusa = prompt('Por qué seguís durmiendo?');
    
    switch (excusa) {
        case 'tengo sueño':
            alert('Todavía tenes sueño? Enserio?!?');
            seguirDurmiendo(); // ejecutamos la función
            break;
            
        case 'hace frio':
            alert('Frio? Pero si hace 40 grados?!?');
            seguirDurmiendo(); // ejecutamos la función
            break;
            
        case 'es temprano':
            alert('Temprano? Son las 3 de la tarde?!?');
            seguirDurmiendo(); // ejecutamos la función
            break;
            
        default:
            alert('No me convence tu excusa, a levantarse!');
            alert('Contaste ' + ovejasContadas + ' ovejas...');
            continuarDurmiendo = false;
            break;
    }
}
```

> Cuando JavaScript llegue a una línea donde está ``seguirDurmiendo()``, va a salir a buscar una **función** con el nombre de ``seguirDurmiendo`` y si la encuentra, va a ejecutar el código definido para la misma.

---

Bueno bueno bueno, antes de meternos mas a fondo hablemos un poco de la sintaxis de las **funciones** y como es que estas funcionan.

Una **función** se define utilizando la palabra ``function``, seguido del nombre, seguido de unos paréntesis y al final unas llaves.

```js
function nombreDeLaFuncion() {
    // código a ejecutar
}
```

Y para llamar a esta función, se escribe el nombre seguido de unos **paréntesis**.

```js
nombreDeLaFuncion();
```

Ahora bien, hablemos de una cosa. Habíamos dicho que las **Funciones** eran un tipo de dato mas en JavaScript. Eso significa que las podemos **almacenar en una variable**? Si, pero sin que lo sepan ya lo estábamos haciendo.

Cuando estuvimos definiendo nuestra función:

```js
function nombreDeLaFuncion() {
    // código a ejecutar
}
```

JavaScript al leer esto, hizo lo siguiente:

```js
var nombreDeLaFuncion = function () {
    // código a ejecutar
};
```

JavaScript creó una variable por nosotros utilizando el nombre que le dijimos y almacenó la ``function`` en la misma.

> Noten la diferencia: si definimos una ``function`` de la primer forma, no hace falta terminar con un ``;``. En cambio de la segunda forma, estamos definiendo la variable y asignándole un valor, por lo tanto si es necesario escribir un ``;``.

Genial! Entonces la variable ``nombreDeLaFuncion`` almacena la ``function`` en si, y por eso yo puedo llamarla por su nombre, como cualquier otra variable? **Si**, la única diferencia es que a las funciones las podes **ejecutar** utilizando los **paréntesis**.

Wait ... Para que sirven esos paréntesis? 

Se acuerdan cuando usamos la **función** ``alert``???

```js
alert('Hola');
```

En esta función, dentro de los paréntesis le pasamos un valor ... Específicamente un ``string``, para que muestre un mensaje con el valor que yo quiera.

Esa es la idea, los paréntesis están para que al **llamar** a una función puedas pasarle **uno o mas valores** con el fin de que la ``function`` ejecute su código utilizando estos **valores**.

Sabiendo esto, que tal si implementamos nuestra propia función ``alert``? Tranquilos, no va a ser más que una farsa. Es solo a modo de ejemplo.

```js
// Quiero definir una función llamada mostrarMensaje
// Y que pueda recibir un valor y mostrarlo en un alert
function mostrarMensaje(mensaje) {
    // Esta función ahora puede recibir un valor
    /* Y JavaScript va a crear una variable llamada mensaje
    // con el valor recibido */
    
    // Entonces puedo utilizar esa variable como yo quiera
    alert(mensaje);
}
```

Dentro del los paréntesis de una ``function``, podemos recibir valores. A estos valores técnicamente se los llama **argumentos** (algunos los llaman **parámetros**).

**Argumentos** es una palabra plural, significa que puedo recibir varios **argumentos**? Si

```js
// Recibimos varios argumentos separandolos por coma.
function mostrarDosMensajes(mensaje1, mensaje2) {
    alert(mensaje1);
    alert(mensaje2);
}

// Enviamos varios argumentos, separandolos por coma
mostrarDosMensajes('Hola', 'que tal?');
```

> No hay un límite en la cantidad de argumentos a recibir.

Que pasa si en una función esperamos dos **argumentos**, pero solo le enviamos uno?

```js
// Esperamos dos argumentos
function mostrarDosMensajes(mensaje1, mensaje2) {
    alert(mensaje1); // mensaje1 tiene como valor 'Hola'
    alert(mensaje2); // mensaje2 tiene como valor undefined
}

// Enviamos solamente uno
mostrarDosMensajes('Hola');
```

> No pasa nada, los **argumentos** que no reciben valor quedan como ``undefined``.

Sabiendo esto, podríamos agregar alguna validación por si necesitamos que todos los **argumentos** tengan un valor, por ejemplo:

```js
// Esperamos dos argumentos
function mostrarDosMensajes(mensaje1, mensaje2) {
    // Si mensaje1 o mensaje2 es undefined, mostrar un error
    if (mensaje1 == undefined || mensaje2 == undefined) {
        alert('Alguno de los argumentos no fue envíado');
    } else {
        alert(mensaje1);
        alert(mensaje2);
    }
}

// Enviamos solamente uno
mostrarDosMensajes('Hola');
/* Muestra el mensaje 'Alguno de los argumentos no fue envíado'
ya que el segundo argumento no fue envíado */
```

> El nombre de los **argumentos** no es estricto. El nombre del argumento que se espera dentro de una función no tiene que ser igual al valor recibido. El nombre de un **argumento** no significa nada para JavaScript, solo sirve para darle un nombre a la variable dentro de la función.

---

Ahora hagamos una pausa y expliquemos otra de las razones por la cuales se utilizan las **Funciones**.

Recuerdan cuando tuvimos que usar la función ``prompt``?

```js
var nombre = prompt('Ingrese su nombre');

alert('Hola ' + nombre);
```

La función ``prompt`` recibe un **argumento**, el cual será utilizado para mostrar un mensaje. Pero esta función tiene algo en especial, permite que el usuario ingrese un texto y lo devuelve ...

Que significa que lo **devuelve** ? Que al llamar a esa función, podemos guardar el valor obtenido en una variable. Entones las funciones además de ejecutar acciones, pueden devolver o **retornar** valores? **Si**.

Para esto se utiliza la palabra ``return``.

```js
function sumarUno(numero) {
    return numero + 1;
}
```

Al escribir ``return`` seguido de un valor, podemos "retornar" ese valor. Haciendo que la función termine inmediatamente. 

Y si una función retorna un valor, podemos almacenarlo en una variable.
```js
function sumarUno(numero) {
    return numero + 1;
}

// Se ejecuta la función sumarUno, con el argumento 5
// Esta función devuelve el argumento recibido + 1
var miNumero = sumarUno(5);

alert(miNumero); // muestra 6
```

Veamos otro ejemplo

```js
function multiplicar(numero1, numero2) {
    return numero1 * numero2;
}

var resultado = multiplicar(5, 2);

alert(resultado); // Muestra 10
```

Otro ejemplo

```js
function crearSaludo(nombre) {
    return 'Hola ' + nombre;
}

var mensaje = crearSaludo('Carlos');

alert(mensaje); // Muestra 'Hola Carlos'
```

Otro ejemplo

```js
function crearSaludo(nombre, tipo) {
    if (tipo == 'formal') {
        return 'Buenas tardes ' + nombre;
    } else if (tipo == 'informal') {
        return 'Buenas ' + nombre + ', todo bien?';
    }
}

var mensajeFormal = crearSaludo('Carlos', 'formal');
var mensajeInformal = crearSaludo('Carlos', 'informal');

alert(mensajeFormal); // Muestra 'Buenas tardes Carlos'
alert(mensajeInformal); // Muestra 'Buenas Carlos, todo bien?'
```

Otro ejemplo

```js
function crearSaludo(nombre) {
    return 'Hola ' + nombre;
}

/* Las funciones que retornan un valor, pueden utilizarse 
directamente. No es necesario guardarlas en una variable */
alert(crearSaludo(nombre));

// O un ejemplo de esto que ya vimos antes ...
var edad = parseInt(prompt('Ingrese su edad'));
/* Primero se ejecuta la función prompt, luego se ejecuta
la función parseInt con el valor devuelto por prompt */
```

No existe una regla técnica que te dice que hay que definir una **función** antes de usarla

```js
// Esto funciona
alert(multiplicar(10, 2));

function multiplicar(a, b) {
    return a * b;
}

// Esto funciona
alert(multiplicar(5, 2));
```

> Esto tiene una razón que va mas allá del scope de este módulo. Por ahora pueden saber que las funciones en JavaScript son "definidas" (y con varias comillas) antes de ejecutar cualquier otra cosa. Por lo tanto llamar a una ``function`` que está definida varias líneas después, funciona perfectamente.

---

Ahora quiero que vean otro ejemplo un poco diferente a los que estuvimos viendo. Habíamos dicho que las **funciones** son otro tipo de dato mas en JavaScript y que podemos almacenarlas en variables para luego ejecutarlas.

```js
var saludar = function() {
    alert('Hola!!');
};
```

Y que luego podemos ejecutarlas

```js
saludar();
```

Y que las funciones pueden recibir **argumentos**

```js
function multiplicar(a, b) {
    return a * b;
}
```

Los **argumentos** que reciben las funciones, pueden ser de cualquier tipo de dato. Osea que también se pueden enviar **funciones**? **Si**.

```js
// Y si definimos una función, que recibe otra función como argumento?
function ejecutarFuncion(funcionAEjecutar) {
    alert('Voy a ejecutar la función que recibí como argumento');
    funcionAEjecutar();
}
```

Esta **función** recibe otra **función** como argumento, luego dentro de su código puede ejecutar la función recibida utilizando los paréntesis, como venimos haciendo siempre.

Entonces ... que tal si llamamos a esa función y le pasamos otra función?

```js
// Y si definimos una función, que recibe otra función como argumento?
function ejecutarFuncion(funcionAEjecutar) {
    alert('Voy a ejecutar la función que recibí como argumento');
    // funcionAEjecutar es una función, la podemos ejecutar
    funcionAEjecutar();
}

// Definimos otra función
function saludar() {
    alert('Hola!!');
}

// llamamos a ejecutarFuncion y le pasamos nuestra función saludar
ejecutarFuncion(saludar);

/* Esto muestra dos alertas:
Primero muestra 'Voy a ejecutar la función que recibí como argumento'
Luego muestra 'Hola!!' */
```

Veamos otro ejemplo

```js
function ejecutarFuncionVariasVeces(funcionAEjecutar, cantidadVeces) {
    for (var index = 0; index < cantidadVeces; index++) {
        funcionAEjecutar();
    }
}
```

Esta ``function`` recibe dos argumentos:

- Una ``function``, la cual será ejecutado tantas veces indique ``cantidadVeces``.
- Un ``number`` el cual determinará cuantas veces se ejecutará el bucle ``for``.

Ahora vamos a probarla:

```js
function ejecutarFuncionVariasVeces(funcionAEjecutar, cantidadVeces) {
    for (var index = 0; index < cantidadVeces; index++) {
        funcionAEjecutar();
    }
}

function saludar() {
    alert('Hola!!');
}

ejecutarFuncionVariasVeces(saludar, 5);
```

La función ``saludar`` se ejecutará 5 veces.

Probemos enviándole otra función, pero de una manera diferente.

```js
function ejecutarFuncionVariasVeces(funcionAEjecutar, cantidadVeces) {
    for (var index = 0; index < cantidadVeces; index++) {
        funcionAEjecutar();
    }
}

ejecutarFuncionVariasVeces(function() {
    alert('Gracias br1 por enseñarnos!');
}, 5);
```

Que? Ven algo raro? Si, en vez de definir una función con un nombre se la pasamos directamente. A estas **funciones** se las llama **Funciones Anónimas**. Son funciones que no tienen nombre, y que se las pasa directamente a otra función.

> No te asustes si la sintaxis es un poco rara. Te vas a ir acostumbrando.

---

Las **funciones** también se utilizan para una clara **separación de intereses**.

> Según Wikipedia: la **separación de intereses**, también denominada separación de preocupaciones o separación de conceptos, es un principio de diseño para separar un programa informático en secciones distintas, tal que cada sección enfoca un interés delimitado.

Básicamente es separar porciones de código según sus responsabilidades. Para esto utilizamos funciones. 

Veamos un ejemplo:

```js
var listaDeNotas = [];

var continuarIngresadoNotas = true;

while (continuarIngresadoNotas) {
    var nuevaNota = parseInt(prompt('Ingrese la nueva nota'));
    
    if (nuevaNota == 0) {
        continuarIngresadoNotas = false;
        alert('El ingreso de notas finalizó');
    } else {
        listaDeNotas.push(nuevaNota);
    }
}

var totalNotas = 0;

for (var index = 0; index < listaDeNotas.length; index++) {
    var notaActual = listaDeNotas[index];
    totalNotas = totalNotas + notaActual;
}

var promedio = totalNotas / listaDeNotas.length;

alert('El promedio de ' + listaDeNotas.length + ' notas es: ' + promedio);

var notaMayor = 0;

for (var index = 0; index < listaDeNotas.length; index++) {
    var notaActual = listaDeNotas[index];
    
    if (notaActual > notaMayor) {
        notaMayor = notaActual;
    }
}

alert('La mayor nota ingresada es: ' + notaMayor);
```

Bueno, este ejemplo parece muy largo pero es bastante simple. A simple vista podemos notar que este código tiene tres partes principales:

- El usuario puede ingresar notas de exámenes, uno a uno. Cuando ingresa el número ``0``, el programa deja de pedirle mas notas. Las notas se guardan en una lista. También se va almacenando el total de las notas.

- Se calcula el promedio de todas las notas, y se lo muestra con un mensaje.
- Se calcula la nota mayor y se la muestra con un mensaje.

Podríamos agregarle comentarios al código para ver la separación clara:

```js
var listaDeNotas = [];

var continuarIngresadoNotas = true;

// Pedir notas al usuario
while (continuarIngresadoNotas) {
    var nuevaNota = parseInt(prompt('Ingrese la nueva nota'));
    
    if (nuevaNota == 0) {
        continuarIngresadoNotas = false;
        alert('El ingreso de notas finalizó');
    } else {
        listaDeNotas.push(nuevaNota);
    }
}

// Calcular promedio de notas
var totalNotas = 0;

for (var index = 0; index < listaDeNotas.length; index++) {
    var notaActual = listaDeNotas[index];
    totalNotas = totalNotas + notaActual;
}

var promedio = totalNotas / listaDeNotas.length;

alert('El promedio de ' + listaDeNotas.length + ' notas es: ' + promedio);

// Calcular nota mayor
var notaMayor = 0;

for (var index = 0; index < listaDeNotas.length; index++) {
    var notaActual = listaDeNotas[index];
    
    if (notaActual > notaMayor) {
        notaMayor = notaActual;
    }
}

alert('La mayor nota ingresada es: ' + notaMayor);
```

Pero ... no sería mejor separar cada parte en funciones? 

Empezemos con la primera parte: **Pedir notas al usuario**.

Vamos a crear una función que pida notas al usuario y devuelva una lista con las notas ingresadas.

```js
function obtenerNotas() {
    var listaDeNotas = [];
    var continuarIngresadoNotas = true;

    while (continuarIngresadoNotas) {
        var nuevaNota = parseInt(prompt('Ingrese la nueva nota'));

        if (nuevaNota == 0) {
            continuarIngresadoNotas = false;
            alert('El ingreso de notas finalizó');
        } else {
            listaDeNotas.push(nuevaNota);
        }
    }
    
    return listaDeNotas; // Devolvemos la lista de notas
}
```

Ahora ya con la lógica de **obtener notas** separada en una función, podemos utilizarla

```js
// Ejecutamos la función obtenerNotas y guardamos la lista creada
var listaDeNotas = obtenerNotas();

// FUNCIONES -------------------
function obtenerNotas() {
    var listaDeNotas = [];
    var continuarIngresadoNotas = true;

    while (continuarIngresadoNotas) {
        var nuevaNota = parseInt(prompt('Ingrese la nueva nota'));

        if (nuevaNota == 0) {
            continuarIngresadoNotas = false;
            alert('El ingreso de notas finalizó');
        } else {
            listaDeNotas.push(nuevaNota);
        }
    }
    
    return listaDeNotas; // Devolvemos la lista de notas
}
```

Perfecto! Ahora vamos a separar la parte de **calcular el promedio de notas**:

Vamos a definir una función que **reciba una lista de notas** y devuelva un ``number`` indicando el promedio.

```js
function calcularPromedioNotas(listaDeNotas) {
    var totalNotas = 0;
    
    // Recorremos la lista y vamos guardando el total de notas
    for (var index = 0; index < listaDeNotas.length; index++) {
        var notaActual = listaDeNotas[index];
        totalNotas = totalNotas + notaActual;
	}

    // Calculamos el promedio de notas
	var promedio = totalNotas / listaDeNotas.length;
    
    return promedio; // Devolvemos el promedio obtenido
}
```

Ahora ya con **la lógica de calcular el promedio** separada en una función, podemos utilizarla:

> Noten que las funciones que vamos definiendo las dejamos al final del código.

```js
// Ejecutamos la función obtenerNotas y guardamos la lista creada
var listaDeNotas = obtenerNotas();

// Calculamos el promedio pasando como argumento nuestra lista creada
var promedio = calcularPromedioNotas(listaDeNotas);
alert('El promedio de ' + listaDeNotas.length + ' notas es: ' + promedio);

// FUNCIONES -------------------
function obtenerNotas() {
    var listaDeNotas = [];
    var continuarIngresadoNotas = true;

    while (continuarIngresadoNotas) {
        var nuevaNota = parseInt(prompt('Ingrese la nueva nota'));

        if (nuevaNota == 0) {
            continuarIngresadoNotas = false;
            alert('El ingreso de notas finalizó');
        } else {
            listaDeNotas.push(nuevaNota);
        }
    }
    
    return listaDeNotas; // Devolvemos la lista de notas
}

function calcularPromedioNotas(listaDeNotas) {
    var totalNotas = 0;
    
    // Recorremos la lista y vamos guardando el total de notas
    for (var index = 0; index < listaDeNotas.length; index++) {
        var notaActual = listaDeNotas[index];
        totalNotas = totalNotas + notaActual;
	}

    // Calculamos el promedio de notas
	var promedio = totalNotas / listaDeNotas.length;
    
    return promedio; // Devolvemos el promedio obtenido
}
```

Genial! Ahora nos queda la última parte: **Obtener la nota mayor**.

Vamos a crear una función que reciba una listas de notas, y que devuelva un ``number`` con el valor de la nota mayor.

```js
function obtenerNotaMayor(listaDeNotas) {
    // Suponemos que una nota no puede ser menor que 0
    var notaMayor = 0;
    
    // Recorremos la lista de notas
    for (var index = 0; index < listaDeNotas.length; index++) {
        var notaActual = listaDeNotas[index];

        // Si la nota actual es mayor, entonces esa es la nota mayor
        if (notaActual > notaMayor) {
            notaMayor = notaActual;
        }
	}
    
    return notaMayor; // Devolvemos la nota mayor
}
```

Perfecto! Ahora que tenemos la lógica de **obtener la nota mayor** separada en una función, podemos utilizarla. Ahora el código se vería asi:

```js
// Ejecutamos la función obtenerNotas y guardamos la lista creada
var listaDeNotas = obtenerNotas();

// Calculamos el promedio pasando como argumento nuestra lista creada
var promedio = calcularPromedioNotas(listaDeNotas);
alert('El promedio de ' + listaDeNotas.length + ' notas es: ' + promedio);

// Obtenemos la nota mayor pasando como argumento nuestra lista creada
var notaMayor = obtenerNotaMayor(listaDeNotas);
alert('La mayor nota ingresada es: ' + notaMayor);

// FUNCIONES -------------------
function obtenerNotas() {
    var listaDeNotas = [];
    var continuarIngresadoNotas = true;

    while (continuarIngresadoNotas) {
        var nuevaNota = parseInt(prompt('Ingrese la nueva nota'));

        if (nuevaNota == 0) {
            continuarIngresadoNotas = false;
            alert('El ingreso de notas finalizó');
        } else {
            listaDeNotas.push(nuevaNota);
        }
    }
    
    return listaDeNotas; // Devolvemos la lista de notas
}

function calcularPromedioNotas(listaDeNotas) {
    var totalNotas = 0;
    
    // Recorremos la lista y vamos guardando el total de notas
    for (var index = 0; index < listaDeNotas.length; index++) {
        var notaActual = listaDeNotas[index];
        totalNotas = totalNotas + notaActual;
	}

    // Calculamos el promedio de notas
	var promedio = totalNotas / listaDeNotas.length;
    
    return promedio; // Devolvemos el promedio obtenido
}

function obtenerNotaMayor(listaDeNotas) {
    // Suponemos que una nota no puede ser menor que 0
    var notaMayor = 0;
    
    // Recorremos la lista de notas
    for (var index = 0; index < listaDeNotas.length; index++) {
        var notaActual = listaDeNotas[index];

        // Si la nota actual es mayor, entonces esa es la nota mayor
        if (notaActual > notaMayor) {
            notaMayor = notaActual;
        }
	}
    
    return notaMayor; // Devolvemos la nota mayor
}
```

Noten que "limpio" quedó el código ahora. Ahora a simple vista nuestro código se ve así:

```js
// Ejecutamos la función obtenerNotas y guardamos la lista creada
var listaDeNotas = obtenerNotas();

// Calculamos el promedio pasando como argumento nuestra lista creada
var promedio = calcularPromedioNotas(listaDeNotas);
alert('El promedio de ' + listaDeNotas.length + ' notas es: ' + promedio);

// Obtenemos la nota mayor pasando como argumento nuestra lista creada
var notaMayor = obtenerNotaMayor(listaDeNotas);
alert('La mayor nota ingresada es: ' + notaMayor);
```

Y si alguien quiere saber cual es la lógica para **obtener las notas**, para **calcular el promedio** o para **obtener la nota mayor** puede ir a la definición de la función.

---

Genial! Espero que hayas entendido por que se usan funciones y cómo funcionan! Ahora a hacer ejercicios!