# Ejercicio 3

#### En una página web sin contenido, realizar la siguiente consigna:

Vamos a simular una calculadora. El usuario podrá ingresar dos números y un signo, definiendo cual será la operación a realizar con los dos números.

Ejemplo:

- Si el usuario ingresa el número ``3``, luego el signo ``+`` y al final el número ``5``, debe mostrar el resultado de la suma de ``3`` y ``5``. 
- Si el usuario ingresa el número ``4``, luego el signo ``-`` y al final el número ``2``, debe mostrar el resultado de la resta entre ``4`` y ``2``.
- Si el usuario ingresa el número ``5``, luego el signo ``*`` y al final el número ``2``, debe mostrar el resultado de la multiplicación entre ``5`` y ``2``.
- Si el usuario ingresa el número ``10``, luego el signo ``/`` y al final el número ``2``, debe mostrar el resultado de la división entre ``10`` y ``2``.

> Recuerda que los números deben ser almacenados en variables de tipo ``number`` y el signo como ``string``.

Ayuda:

> Así podrían comenzar el código.

```js
var primerNumero = parseInt(prompt('Ingrese el primer número a evaluar'));

var signo = prompt('Ingrese la operación a realizar. Posibles valores: + - * /');

var segundoNumero = parseInt(prompt('Ingrese el segundo número a evaluar'));
```

---

Extra:

> Las consignas extras son opcionales. No son necesarias para terminar el ejercicio pero sirven como un desafío personal.

Tenemos un pequeño problema. Si el usuario intenta hacer una división y alguno de los dos números es ``0``, nuestro código va a romper. **No se puede dividir por cero**. 

- Agregar una validación en nuestro ``switch``: si el usuario intenta hacer una división por ``0``, mostrar un mensaje con el texto ``'No es posible dividir por cero'``.

Tenemos un segundo pequeño problema. Si el usuario intenta hacer una multiplicación y alguno de los dos números es ``0``, nuestro codigo deberia devolver ``0``, ya que cualquier numero multiplicado por ``0`` da como resultado ``0``