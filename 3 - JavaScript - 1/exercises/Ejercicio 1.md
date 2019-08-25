# Ejercicio 1

Crear una página web, sin contenido. Ya que será utilizada para prácticar un poco Javascript.

Crea el archivo Javascript y vinculalo a tu página web. (Ver ejemplo del primer módulo).

A continuación, pidele al usuario que ingrese su nombre.

Ayuda:

```js
// Para pedir una entrada al usuario, podes usar la función prompt
// Esta recibe un string como argumento y muestra una ventana con el mensaje definido
// Junto a una caja de texto para ingresar un valor. 
// Esta función devuelve un string, con el valor ingresado por el usuario.
prompt('Por favor, ingrese su nombre');
```

Como dijimos recién, la función ``prompt`` devuelve un string con el valor ingresado por el usuario. Por lo tanto podemos guardar ese valor en una variable.

Ayuda:

```js
var nombre = prompt('Por favor, ingrese su nombre');
// Ahora nombre tiene el valor ingresado por el usuario
```

Ahora que sabemos como pedirle al usuario un valor, y como guardarlo. Quiero que le mostremos al usuario **un saludo**!

Si el usuario, por ejemplo, ingresa: 'Mauricio Macri'
Se le debe mostrar una alerta con el mensaje: 'Hola Mauricio Macri, sos re gato';

> Para esto, recordá usar los operadores de suma (para concatenar strings) y la función alert (para mostrar el mensaje)