# Ejercicio 3

Ahora que podemos pedirle un número al usuario, queremos hacer lo siguiente:

- Si la edad ingresada del usuario es mayor o igual a 18, mostrar una alerta con el mensaje **'Pasa wachin'**;

- De lo contrario, mostrar una alerta con el mensaje **'Rajá de acá wachin'**

  > Si, sos un patova de un boliche.

Para esto, vamos a tener que introducir las **Estructuras de Control**.

Suenan mas complicadas de lo que parecen.

Permiten que se ejecute determinado código según una o más condiciones. 

La **Estructura de Control** mas común es el **if**.

Un **if** ejecuta una porción de código si una condición especificada es evaluada como ``true`` (verdadera)

Ejemplo

```js
// Si la condición definida da como resultado true, entonces ...
if (condicionAEvaluar) {
    // ejecutar esta acción
}
```

Ejemplos reales

```js
// Si diez es mayor que cinco, ejecutar la función alert
if (10 > 5) { 
    // la condición devolvió true, por lo tanto ejecuta la función alert
    alert('Diez es mayor que cinco!');
}

// Si tres es mayor que cinco, ejecutar la función alert
if (3 > 5) { 
    alert('Tres es mayor que Cinco);
}
// la condición devolvió false, por lo tanto NO ejecuta la función alert
```

> Practicar escribiendo estas sentencias **if**, ya que suelen generar problemas por olvidarse un paréntesis o etc.

A la estructura **if**, también la puede seguir un **else** (sino).

El **else** se define como: 'Si tal condición no es verdadera, entonces hacer esto'. Si la condición del **if** da como resultado false, se ejecutará entonces el código definido dentro del **else**.

Ejemplo

```js
// Si Cinco es mayor que Diez, ejecutar esto...
if (5 > 10) {
    alert('Cinco es mayor que Diez');
} else { // Si no, ejecutar esto otro ...
    alert('Cinco NO es mayor que Diez');
}

// En este caso, Cinco NO era mayor que Diez, por lo tanto se ejecutó solo el segundo alert
```

Ahora que sabemos usar los **if** y **else**. Implementar la lógica definida al principio del ejercicio.