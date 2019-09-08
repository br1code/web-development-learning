# JavaScript - 3

En este módulo vamos a aprender a usar la declaración ``switch``.

El ``switch`` es mas o menos lo equivalente a muchos ``if`` anidados. Veamos este ejemplo.

```js
var colorPreferido = prompt('Ingrese su color preferido');

if (colorPreferido == 'rojo') {
    alert('Tu color preferido es el rojo, genial!');
} else if (colorPreferido == 'azul') {
    alert('Tu color preferido es el azul, genial!');
} else {
    alert('Tu color preferido no es ni el azul ni el rojo, que mal.');
}
```

En este ejemplo de ``if``, ``else if`` y ``else`` definimos tres posibles casos de ejecución.

- Si el color preferido es rojo
- Si el color preferido es azul
- Si no es ninguno de los definidos

Definimos cada posible caso, con una condición. Generalmente en estas condiciones, utilizamos un operador de comparación. Ej: ``== < >``.

Ahora bien, que pasa si en un futuro necesitamos soportar mas colores? Verde, amarillo, violeta, etc. Tendríamos que agregar muchos ``else if`` por cada color nuevo.

Para esto mismo, existe una otra alternativa que, si bien todavía vamos a necesitar escribir algo cada vez que tengamos que soportar un nuevo color, nos permite escribirlo de una forma mucho mejor y limpia. La declaración ``switch``.

```js
switch (variableAEvaluar) {
    case posibleCaso:
        // código a ejecutar si la variableAEvaluar es igual al posibleCaso
        break;
    
    case otroPosibleCaso:
        // código a ejecutar si la variableAEvaluar es igual al otroPosibleCaso
        break;
    
    default:
        /* código a ejecutar si variableAEvaluar no es igual 
        a ninguno de los posibles casos */
        break;
}
```

El ``switch`` recibe un valor de cualquier tipo, pero generalmente recibe ``string`` (cadenas de texto) o ``int`` (números). Dentro del mismo, definimos posibles ``case`` (casos) en los que queremos que se ejecute una porción de código si y solo si el valor recibido es **IGUAL** al valor definido en el ``case``.

Si el ``switch`` recibe una variable con valor ``5`` y tenemos definido un ``case`` con el valor ``5``, se ejecutará el código definido para ese ``case``. Si **NO** tenemos definido un ``case`` con el valor recibido en el ``switch``, se ejecutará el código definido en el ``default``.

> El ``default`` es opcional, así como el ``else`` en un ``if``. 

Veamos el uso de un ``switch`` común, reutilizando el ejemplo anterior:

```js
var colorPreferido = prompt('Ingrese su color preferido');

switch (colorPreferido) {
    case 'rojo':
        alert('Tu color preferido es el rojo, genial!');
        break;
    
    case 'azul':
        alert('Tu color preferido es el azul, genial!');
        break;
        
    default:
        alert('Tu color preferido no es ni el azul ni el rojo, que mal.');
        break;
}
```

Este ``switch`` hace exactamente lo mismo que el ejemplo del principio utilizando ``if``, ``else if`` y ``else``. Pero ... no se ve un poco más claro?

La variable que el ``switch`` evalúa es ``colorPreferido``. 

- Si el valor de ``colorPreferido`` es ``'rojo'`` , muestra ``'Tu color preferido es el rojo, genial!'``
- Si el valor de ``colorPreferido`` es ``'azul'``, muestra ``'Tu color preferido es el azul, genial!'``
- SI el valor de ``colorPreferido`` no es ni ``rojo`` ni ``azul``, muestra ``'Tu color preferido no es ni el azul ni el rojo, que mal.'``

Hablemos un poco de la palabra ``break``. Para que sirve?

Escribiendo ``break;`` estamos indicando que el ``case`` se evaluó y ejecutó el código definido para el mismo, y que el ``switch`` ya terminó.

Pero, al final el ``switch`` es casi lo mismo que usar ``if``, ``else if`` y ``else``? Mmm si pero no... Miren este ejemplo:

```js
var colorPreferido = prompt('Ingrese su color preferido');

switch (colorPreferido) {
    case 'rojo':
	case 'azul':
	case 'amarillo':
        alert('Tu color preferido es primario!');
        break;
        
    case 'naranja':
	case 'verde':
	case 'violeta':
        alert('Tu color preferido es secundario!');
        break;
    
    default:
        alert('Tu color preferido es ... ni idea');	
        break;
}
```

Este ejemplo es diferente: 

- Si el ``colorPreferido`` es ``'rojo'`` o ``'azul'`` o ``'amarillo'`` muestra el mensaje ``'Tu color preferido es primario!'``
- Si el ``colorPreferido`` es ``'naranja'`` o ``'verde'`` o ``'violeta'`` muestra el mensaje ``'Tu color preferido es secundario!'``
- Si el ``colorPreferido`` no es ninguno de estos seis, muestra el mensaje ``'Tu color preferido es ... ni idea'``

Perfecto! Si para un ``case`` no escribimos un ``break``, el código interpreta que puede haber otro ``case`` que si sea igual que el valor recibido en el ``switch``. 

Si tuvieramos que escribir este ejemplo utilizando ``if``, ``else if`` y ``else``, tendríamos que usar bastante el operador ``||`` (que significa **O** en una condición).

```js
var colorPreferido = prompt('Ingrese su color preferido');

if (colorPreferido === 'rojo' || colorPreferido === 'azul' || colorPreferido === 'amarillo') {
    alert('Tu color preferido es primario!');
} else if (colorPreferido === 'naranja' || colorPreferido === 'verde' || colorPreferido === 'violeta') {
    alert('Tu color preferido es secundario!');
} else {
    alert('Tu color preferido es ... ni idea');
}
```

Aahhhhh, y ahora?? Cual te parece mejor para estas situaciones? Y si tuvieras que agregar 20 colores mas???? Ya estamos, esto es el ``switch``. Ahora a hacer unos ejercicios para no olvidarse de como se escribe, ya que mucho más adelante van a ver mejores formas para reemplazar los ``if`` y los ``switch``.