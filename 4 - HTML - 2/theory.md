# HTML - 2

En este módulo vamos a ver algunos elementos nuevos.

## Links

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

Tambien podés usar los links de la siguiente forma:

Si en vez de un texto, agregas una etiqueta ``img``, la imagen actuará como un link! Al darle click a la imagen, te redireccionará a la página.

```html
<a href="https://google.com">
    <img src="fotoDeGatito">
</a>
```

Los links se pueden usar de un montón de formas, pero las vamos a ver en otro momento.

## Tablas

|  Producto | Stock  | Precio Minorista  | Precio Mayorista  |
|---|---|---|---|
|  Pepsi | 34  |  $14.50 |  $13.00 |
|  Monster | 3  |  $10.00 |  $8.50 |

Las tablas son, tablas .. Te permiten definir columnas y filas, son totalmente personalizables (estilo) y son muy faciles de crear.

Para crear una tabla, se utiliza la etiqueta ``table```.

```html
<table>

</table>
```

Ahora bien, para agregar filas (row) a nuestra tabla, se utiliza la etiqueta ``tr``.

```html
<table>
    <tr>

    </tr>
</table>
```

Esto va a crear una fila nueva, pero para que podamos ver "algo", necesitamos agregarle columnas. Para esto se utilizan las etiquetas ``th`` (table head / encabezado de tabla) y ``td`` (table data-cell / dato o celda de tabla).

Los elementos ``th`` se usan para agregar una columna de tipo encabezado (como lo son **Produto**, **Stock**, **Precio Minorista** y **Precio Mayorista**).

Los elementos ``td`` se usan para agregar una columna de "dato" o contenido.

Estos elementos se agregan dentro de una fila ``td``, uno seguido del otro. Estos terminan definiendo el orden de las columnas.

Vamos a escribir la tabla de productos que vimos recién, en HTML.

```html
<table>

    <!-- La primer fila, la usamos para definir las columnas de encabezado -->
    <tr>
        <th>Producto</th>
        <th>Stock</th>
        <th>Precio Mayorista</th>
        <th>Precio Minorista</th>
    </tr>

    <!-- Las demás filas, las usamos para agregar el contenido de la tabla -->
    <tr>
        <td>Pepsi</td>
        <td>34</td>
        <td>$14.50</td>
        <td>$13.00</td>
    </tr>

    <tr>
        <td>Monster</td>
        <td>3</td>
        <td>$10.00</td>
        <td>$8.50</td>
    </tr>

</table>
```

En otro momento vamos a ver como personalizar las tablas.