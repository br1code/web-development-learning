# HTML - 2

En este módulo vamos a ver algunos elementos nuevos.

Empezemos con los links.

Para que sirven? Para darles click y que te redireccione a otra página.

Cómo se usan?

```html
<a>Ingresá a este link!</a>
```

Perfecto, va a aparecer un link (probablemente sea un texto en algún color, y si pones el mouse encima va a cambiar la flechita).

Pero el link así como está, no sirve de nada. Falta indicarle cual es la página a donde redireccionar. Hay que agregarle un **atributo**.

```html
<a href="https://google.com">Ingresá a este linkl!</a>
```
Con el atributo ``href`` le indicamos la URL a redireccionar.

Por defecto, al darle click va a abrir el link en la misma pestaña. Podemos cambiar esto con el atributo ``target``.

```html
<a href="https://google.com" target="_blank">Ingresá a este linkl!</a>
```

> "_blank" indica que el link se abrirá en una nueva pestaña.

