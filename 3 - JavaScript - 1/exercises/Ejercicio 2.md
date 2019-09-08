# Ejercicio 2

Luego de preguntarle el nombre al usuario, queremos preguntarle cuantos años tiene para guardar el valor en una variable.

Ayuda:

Para pedir al usuario un valor, seguimos usando la función ``prompt``.
Dijimos que esta función devolvía un valor de tipo **string**.

```js
var edad = prompt('Cuantos años tienes?');
// edad ahora es una variable de tipo string, con el valor ingresado por el usuario
```

Pero en realidad lo queremos guardar como tipo de dato **number** (número entero). Cómo podemos hacer esto?

Vamos a tener que usar una función, que convierta un tipo de dato en otro tipo de dato. Específicamente queremos que convierta un **string** en un **number**.

Para esto, podemos usar la función ``parseInt``. La cual recibe un valor como argumento, y devuelve un **number** con el valor convertido.

Ejemplos

```js
var numero = parseInt('5');
// Convierte el string '5' a un int 5.
// numero ahora es una variable de tipo int, con valor 5.
```

Sabiendo esto, podemos convertir el valor ingresado por el usuario a un **number**.

```js
var edad = prompt('Cuantos años tienes?');
var edadConvertida = parseInt(edad);
// edadConvertida ahora es una variable de tipo int, con el valor convertido ingresado por el usuario
```

También puedes hacer todo en una misma línea
```js
var edad = parseInt(prompt('Cuantos años tienes?'));
// la función prompt se ejecuta primero, devolviendo un string con el valor ingresado por el usuario
// luego se llama a la función parseInt, con el string devuelto por la función prompt
```

> Se puede ejecutar una función adentro de los paréntesis de un llamado a otra función. En realidad se puede ejecutar una función en cualquier lugar del código.

Si ya pudiste pedirle la edad al usuario, y guardarla en una variable. Sigamos con el siguiente ejercicio.