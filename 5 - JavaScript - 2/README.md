# JavaScript - 2

Hoy vamos a aprender como funcionan los bucles y cuales son sus usos comunes.

En palabras simples, un bucle es una **"porción de código"** que se va a ejecutar tantas veces según diga una **"condición"**.

Cuando hablamos de **"porción de código"** nos referimos a declaraciones y ejecuciones de código, por ejemplo:

```js
var mensaje = 'Hello';

alert(mensaje);
```

Cuando hablamos de **"condición"** nos referimos a un valor booleano (true o false), el cual puede ser el resultado de una comparación. Por ejemplo:

```js
var cincoEsMayorQueTres = 5 > 3; // true

alert(cincoEsMayorQueTres); // Muestra una alerta con el valor true
```

Por lo tanto, podemos decir que un bucle es un **conjunto de declaraciones y ejecuciones de código** que se van a ejecutar tantas veces según lo determine el **resultado de una condición**.

Veamos entonces el primer bucle:

### Bucle ``While`` (mientras)

El ``while`` es el ejemplo mas claro de un bucle, veamos como se escribe:

```js
while (condicionAEvaluar) {
    // código a ejecutar
}
```

> "Mientras x condición sea verdadera, ejecutar este código"

Este bucle se inicia con la palabra ``while``, seguido de dos paréntesis, seguido de dos llaves;

Dentro de los dos paréntesis va una **condición**.

Dentro de las dos llaves, va las declaraciones y ejecuciones de código.

El proceso del bucle ``while`` a nivel de ejecución (a medida que se va ejecutando) es el siguiente:

1 - Se llega a la línea donde está el while.
2 - Se evalúa la condición que está entre los dos paréntesis.
3 - Si el resultado es **true**, ingresar adentro de las dos llaves para ejecutar el código y volver al punto 2.
4 - Si el resultado es **false**, dar como terminado el ``while`` y seguir con el código que haya luego del mismo.

Veamos un ejemplo, paso a paso:

```js
var numero = 0;

while (numero < 2) {
    alert(numero);
    numero = numero + 1;
}

alert('ke wea hermano');
```

- Se define una variable ``numero`` con valor ``0``.
- Se llega a la línea donde comienza el ``while``.
- Se evalúa la condición definida dentro de los dos paréntesis:
    - ``numero < 2`` numero actualmente tiene como valor ``0``. Por lo tanto: ``0 < 2`` Cero es menor que Dos? = ``true``
- La condición devolvió ``true``, por lo tanto se ejecuta todo el código definido dentro de las llaves:
    - Se ejecuta la función ``alert``, mostrando el valor de la variable ``numero``. El cual es ``0``.
    - Se le suma ``1`` a la variable ``numero``, teniendo ahora como valor ``1``.
- Se vuelve a evaluar la condición definida dentro de los dos paréntesis:
    - ``numero < 2`` numero actualmente tiene como valor ``1``. Por lo tanto: ``1 < 2`` Uno es menor que Dos? = ``true``
- La condición devolvió ``true``, por lo tanto se ejecuta todo el código definido dentro de las llaves:
    - Se ejecuta la función ``alert``, mostrando el valor de la variable ``numero``. El cual es ``1``.
    - Se le suma ``1`` a la variable ``numero``, teniendo ahora como valor ``2``.
- Se vuelve a evaluar la condición definida dentro de los dos paréntesis:
    - ``numero < 2`` numero actualmente tiene como valor ``2``. Por lo tanto: ``2 < 2`` Dos es menor que Dos? = ``false``
- La condición devolvió ``false``, se da como finalizado el bucle ``while``.
- Luego de finalizar el ``while``, el código debe seguir. Por último se ejecuta el ``alert`` con el mensaje 'ke wea hermano'.

Parece mas complicado de lo que es. 

De lo único que hay que asegurarse siempre es evitar los **bucles infinitos**. Que significa esto?

Crear un **bucle infinito** significa crear un bucle en el cual la condición **SIEMPRE** de como resultado true. 

Por eso mismo en el ejemplo de recién, en cada iteración del bucle le sumamos ``1`` a nuestro contador. Asegurándonos de que en algún momento el bucle llegue a ``2``, provocando que ``2 < 2`` de como resultado ``false`` y a su vez de como finalizado el bucle.

### Bucle ``for``

Este bucle es muy parecido al ``while``, con algunas diferencias. Veamos como se escribe:

> El bucle for es mucho mas usado que el while.

```js
for (definición de variable contador; condición del bucle; aumento de contador) {
    // código a ejecutar
}
```

El bucle ``for`` consiste en 4 partes:

1 - **Definición de variable contador**: se define una variable que se va a utilizar como contador. A diferencia del ejemplo anterior con el ``while``, el bucle ``for`` nos permite definir el contador dentro del mismo. Generalmente se lo llama ``i`` o ``index`` (índice) y se lo inicializa con un valor de ``0``.

```js
for (var index = 0; condición del bucle; aumento de contador) {
    // código a ejecutar
}
```

2 - **Definición de condición a evaluar**: se define cual será la condición a evaluar para decidir si el bucle debe continuar o no. Tiene el mismo comportamiento que en el bucle ``while``. **Si la condición da true, ejecuta el código dentro de las llaves**.

```js
for (var index = 0; index < 2; aumento de contador) {
    // código a ejecutar
}
```

3 - **Aumento de contador**: así como explicamos lo de los bucles infinitos y que debemos evitarlos, generalmente le aumentamos ``1`` al contador para que en algún momento la condición de como resultado ``false``. Este aumento se ejecuta cada vez que termina una iteración del bucle.

```js
for (var index = 0; index < 2; index++) {
    // código a ejecutar
}
```

4 - **Código a ejecutar**: acá se escribe el código que se va a ejecutar en cada iteración del bucle. Acá adentro tenemos acceso a la variable ``index``, el cual en cada iteración tendrá como valor el contador actual. Esta variable de contador nos va a servir más tarde cuando intentemos recorrer una lista, accediendo elemento por elemento según su posición.

```js
for (var index = 0; index < 2; index++) {
    alert('El valor actual del contador es ' + index);
}
```


El proceso del bucle ``for`` a nivel de ejecución (a medida que se va ejecutando) es el siguiente:

1 - Se llega a la línea donde está el ``for``.
2 - Se define la variable contador (**primera parte del ``for``**).
3 - Se evalúa la condición. (**segunda parte del ``for``**)
4 - Si el resultado es **true**, ingresar adentro de las dos llaves para ejecutar el código, luego aumentarle ``1`` al contador (**tercera parte del ``for``**) y volver al punto 3.
5 - Si el resultado es **false**, dar como terminado el ``for`` y seguir con el código que haya luego del mismo.

Veamos un ejemplo paso a paso:

```js
for (var index = 0; index < 2; index++) {
    alert('El valor actual del contador es ' + index);
}

alert('ke wea hermano');
```

- **Comienza** la definición del bucle ``for``.
- Primera parte del ``for``, **se define una variable** llamada ``index`` con valor inicial de ``0``.
- Se **evalúa la condición**: ``index < 2`` = la variable ``index`` tiene como valor 0 = ``0 < 2`` da como resultado ``true``.
- La **condición devolvió ``true``**, por lo tanto se ejecuta todo el código definido dentro de las llaves:
    - Se ejecuta la función ``alert`` mostrando el mensaje 'El valor actual del contador es 0'.
- La ejecución del código dentro de las llaves terminó, por lo tanto **la iteración del ``for`` es finalizada**. Se le aumenta ``1`` al contador. Ahora la variable ``index`` tiene como valor ``1``.
- Se vuelve a **evaluar la condición**: ``index < 2`` = la variable ``index`` ahora tiene como valor 1 = ``1 < 2`` da como resultado ``true``.
- La **condición devolvió ``true``**, por lo tanto se ejecuta todo el código definido dentro de las llaves:
    - Se ejecuta la función ``alert`` mostrando el mensaje 'El valor actual del contador es 1'.
- La ejecución del código dentro de las llaves terminó, por lo tanto **la iteración del ``for`` es finalizada**. Se le aumenta ``1`` al contador. Ahora la variable ``index`` tiene como valor ``2``.
- Se vuelve a **evaluar la condición**: ``index < 2`` = la variable ``index`` ahora tiene como valor 2 = ``2 < 2`` da como resultado ``false``, **se da como finalizado el bucle ``for``**.
- Luego de finalizar el ``for``, el código debe seguir. Por último se ejecuta el ``alert`` con el mensaje 'ke wea hermano'.

---

Con esto terminamos el módulo, luego vamos a dar un poco de listas (arrays) y van a ver como podemos utilizar los bucles para recorrer los elementos de una lista. Ahora a hacer la ejercitación!!