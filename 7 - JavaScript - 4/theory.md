# JavaScript - 4

En este módulo vamos a aprender sobre arrays (listas).

Un array es otro tipo de dato en JavaScript, pero el concepto de array es casi el mismo en todos los lenguajes de programación.

Veamos algunas características de los arrays:

- Un **array** es una lista de **elementos**. 

- Cada **elemento** tiene una **posición** en la lista.

- Las **posiciones** de los **elementos** empiezan a contar desde ``0``.

- Se puede acceder a un **elemento** de un **array** indicando su **posición**.

  

- El orden los **elementos** de un **array** depende del orden en el que se los agregan. Aunque el orden de los elementos puede modificarse luego.

- Se pueden **agregar** y **eliminar** elementos de un **array** en cualquier momento.

- En JavaScript, un **array** puede tener elementos de diferentes **tipos de datos**, al mismo tiempo. Por ejemplo, puedo tener un ``array`` con elementos de tipo ``string`` y con elementos de tipo ``number``. Esto no es posible en algunos lenguajes de programación.

Bueno, veamos un poco de código ...

---

Los arrays se crean usando corchetes ``[]``.

```js
var lista = [];
```

---

Los elementos de un array se separan con una coma ``,``.

```js
var lista = ['cassie', 'sultan', 'rakhan', 'kaisa'];
```

---

Podemos obtener la longitud de un **array** accediendo a su **propiedad** ``length``.

```js
var lista = ['cassie', 'sultan', 'rakhan', 'kaisa'];

lista.length // 4
```

> Que es una propiedad? Ya lo vamos a entender cuando lleguemos a ver **Objetos**. Por ahora quedense con que algunos tipos de datos como los **arrays**, son **Objetos**. Y los **Objetos** pueden contener variables (propiedades) y funciones dentro. ``length`` es una **propiedad** que tienen todos los **arrays**. Para acceder a una **propiedad** o una **función** de un objeto, se utiliza el ``.`` seguido del nombre.

---

Podemos acceder a los elementos de un **array** de forma individual, utilizando corchetes junto al índice de su posición.

```js
var lista = ['cassie', 'sultan', 'rakhan', 'kaisa'];

lista[0] // devuelve 'cassie'
lista[1] // devuelve 'sultan'
lista[2] // devuelve 'rakhan'
lista[3] // devuelve 'kaisa'
```

> El índice (posición) de un **array** es de tipo ``number``.

---

Si intentamos acceder a un elemento que no existe, devolverá ``undefined``.

```js
var lista = ['cassie', 'sultan', 'rakhan', 'kaisa'];

lista[99] // undefined
```

> ``undefined`` significa que 'no tiene valor'. Cuando definimos una variable sin darle un valor inicial, la variable tendrá el valor ``undefined`` hasta que le asignes un valor.

---

El **valor** de un **elemento** de un **array** puede modificarse.

```js
var lista = ['cassie', 'sultan', 'rakhan', 'kaisa'];

alert(lista); // Muestra 'cassie', 'sultan', 'rakhan', 'kaisa'

lista[0] = 'homero'; // Modificamos el valor del elemento que está en la posición 0

alert(lista); // Muestra 'homero', 'sultan', 'rakhan', 'kaisa'
```

---

Podemos agregar un elemento a un **array** utilizando la función ``push``.

> La función ``push`` proviene de los **arrays**. Como habíamos mencionado antes, los **arrays** son objetos, y los objetos pueden tener **propiedades** y **funciones**. Por lo tanto, para utilizar la función ``push`` necesitamos utilizar el ``.``

```js
var lista = ['cassie', 'sultan', 'rakhan', 'kaisa'];

lista.push('homero'); // agregamos el elemento nuevo

alert(lista); // Muestra 'cassie', 'sultan', 'rakhan', 'kaisa', 'homero'
```

> La función ``push`` recibe el elemento que se quiere agregar y lo agrega al **array** El elemento nuevo es ubicado al final del **array**.

---

Podemos remover un elemento de un **array** utilizando la función ``splice``. Esta función recibe dos valores:

- El índice del elemento o elementos a remover.
- La cantidad de elementos a remover.

> La función ``splice`` también proviene de los **arrays**, se accede usando el ``.``

```js
var lista = ['cassie', 'sultan', 'rakhan', 'kaisa'];

// Quiero eliminar a sultan
lista.splice(1, 1); // 1: posición de sultan, 1: cantidad de elementos a eliminar

alert(lista); // Muestra 'cassie', 'rakhan', 'kaisa'
```

> Noten como al eliminar un elemento en el 'medio' de un **array**, los elementos que estaban delante del mismo se acomodan, ocupando la posición eliminada.

Veamos una explicación del proceso de eliminar a sultan.

Principalmente la lista se veía asi:

| Índice | ``0``        | ``1``        | ``2``        | ``3``       |
| ------ | ------------ | ------------ | ------------ | ----------- |
| Valor  | ``'cassie'`` | ``'sultan'`` | ``'rakhan'`` | ``'kaisa'`` |

```js
lista.splice(1, 1); // 1: posición de sultan, 1: cantidad de elementos a eliminar
```

Al eliminar ``1`` elemento desde la posición ``1``,  ``'sultan'`` termina siendo removido del **array**. Pero ese lugar que ocupaba no queda vacío, los elementos que estaban delante de él retroceden una posición, **redimensionando el array**.

| Índice | ``0``        | ``1``        | ``2``       |
| ------ | ------------ | ------------ | ----------- |
| Valor  | ``'cassie'`` | ``'rakhan'`` | ``'kaisa'`` |

---

Podemos recorrer los elementos de un **array** utilizando un bucle ``for``.

> Si no recuerdan como usar los bucles ``for``, recomiendo volver a darles una mirada.

La condición de nuestro bucle ``for`` será que el ``index`` no exceda la longitud del **array**.

> Para acceder a la longitud de un **array** usamos la propiedad ``length``.

```js
var lista = ['cassie', 'sultan', 'rakhan', 'kaisa'];

for (var index = 0; index < lista.length; index++) {
    /* Adentro del for, tenemos acceso a la variable index.
    Con la variable index, sabemos el índice actual del for.
    La podemos utilizar para acceder a cada elemento del array */
    alert(lista[index]);
}
```

En la condición del ``for``, definimos que el bucle se ejecutará mientras ``index`` sea menor a la longitud del **array**, por lo tanto el bucle se ejecutará con los índices:

- ``index`` = 0
  - ``lista[0]``
    - ``'cassie'``
- ``index`` = 1
  - ``lista[1]``
    - ``'sultan'``
- ``index`` = 2
  - ``lista[2]``
    - ``'rakhan' ``
- ``index`` = 3
  - ``lista[3]``
    - ``'kaisa'``
- ``index`` = 4. La condición del bucle devuelve ``false``. Fin del bucle.

---

Podemos saber si un elemento existe en un **array**. Para esto hay muchas formas, una de ellas es usar la función ``includes`` de los **arrays**.

> La función ``includes`` recibe un valor, devuelve ``true`` si el valor existe en el **array**. De lo contrario, devuelve ``false``.

```js
var lista = ['cassie', 'sultan', 'rakhan', 'kaisa'];

lista.includes('sultan'); // true

lista.includes('homero'); // false
```

---

Veamos un ejemplo de como crear un **array** de forma dinámica, totalmente por el usuario.

Vamos a hacer que el usuario pueda crear una lista de amigos.

Lo primero que vamos a hacer es crear un **array** nuevo:

```js
var amigos = [];
```

Ahora vamos a preguntarle cuántos amigos quiere almacenar. (Mas adelante vamos a ver como hacer esto sin tener que preguntarle desde un principio cuántos elementos tendrá el **array**).

```js
var amigos = [];

var cantidadAmigosAIngresar = parseInt(prompt('Ingrese la cantidad de amigos que va a ingresar'));
```

Como ahora sabemos de antemano cuantos elementos tendrá el **array**, podemos utilizar un bucle ``for`` que se ejecute la cantidad exacta de veces para que en cada iteración del bucle, el usuario ingrese un nombre de un amigo y lo agreguemos a nuestro **array**.

```js
var amigos = [];

var cantidadAmigosAIngresar = parseInt(prompt('Ingrese la cantidad de amigos que va a ingresar'));

for (var index = 0; index < cantidadAmigosAIngresar; index++) {
    var nuevoAmigo = prompt('Ingrese el nombre del amigo');
    
    amigos.push(nuevoAmigo); // agregamos el nuevo amigo al array
}
```

Si por ejemplo, ``cantidadAmigosAIngresar`` tiene como valor ``4``:  este bucle ``for`` se ejecutará ``4`` veces. Permitiendole agregar ``4`` amigos al **array**.

Al terminar el bucle ``for``, ya tendremos nuestro **array** de amigos con sus respectivos elementos.

---

Veamos otro ejemplo simple. Partiendo de un **array** de números ya definido, tenemos que filtrar los elementos de ese **array** y quedarnos solo con los elementos que sean **números menores que 10**.

```js
var listaOriginal = [33, 14, 6, 87, 21, 4, 66, 1];
```

Lo primero que vamos a hacer es crear otro **array**, en el cual guardaremos los **números pares**.

> Cuando se trata de modificar un **array** existente, como por ejemplo eliminar elementos del mismo, generalmente se crea otro **array** o se reemplaza el **array** original por otro. Por que? Recorrer los elementos de un **array** mientras los vas eliminando genera siempre problemas. Mas adelante vamos a ver por qué.

```js
var listaOriginal = [33, 14, 6, 87, 21, 4, 66, 1];

var listaNueva = [];
```

Ahora vamos a recorrer los elementos de ``listaOriginal``.

```js
var listaOriginal = [33, 14, 6, 87, 21, 4, 66, 1];

var listaNueva = [];

for (var index = 0; index < listaOriginal.length; index++) {
    var elementoActual = listaOriginal[index];
}
```

En cada iteración del bucle ``for``, tenemos acceso al elemento actual del **array**. Lo que vamos a hacer es lo siguiente:

- Si el número es **menor a 10**: lo vamos a agregar a la ``listaNueva``.

```js
var listaOriginal = [33, 14, 6, 87, 21, 1, 66, 4];

var listaNueva = [];

for (var index = 0; index < listaOriginal.length; index++) {
    var elementoActual = listaOriginal[index];
    
    if (elementoActual < 10) {
        listaNueva.push(elementoActual);
    }
}

alert(listaNueva); // Muestra 6, 1, 4
```

De esta forma, al terminar el bucle ``for`` nuestra ``listaNueva`` tendrá solo los números menores a ``10``.

Y ya que estamos, podemos ordenar nuestra ``listaNueva``. Para esto podemos utilizar la función ``sort`` de los **arrays**. 

> Mas adelante vamos a explicar cómo funciona esta función, pero para el objetivo de este módulo no es algo totalmente necesario. Tampoco implementaremos nuestro propia lógica para ordenar la lista.

```js
var listaOriginal = [33, 14, 6, 87, 21, 1, 66, 4];

var listaNueva = [];

for (var index = 0; index < listaOriginal.length; index++) {
    var elementoActual = listaOriginal[index];
    
    if (elementoActual < 10) {
        listaNueva.push(elementoActual);
    }
}

alert(listaNueva); // Muestra 6, 1, 4

listaNueva.sort();

alert(listaNueva); // Muestra 1, 4, 6
```

> Noten que la función ``sort`` modifica directamente el **array**. 