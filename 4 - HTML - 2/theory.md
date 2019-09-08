# HTML - 2

En este módulo vamos a ver algunos elementos nuevos.

## Links

Empecemos con los links.

Para que sirven? Para darles click y que te redireccione a otra página.

Cómo se usan?

```html
<a>Ingresá a este link!</a>
```

Perfecto, va a aparecer un link (probablemente sea un texto en algún color, y si pones el mouse encima va a cambiar la flechita).

Pero el link así como está, no sirve de nada. Falta indicarle cual es la página a donde redireccionar. Hay que agregarle un **atributo**.

```html
<a href="https://google.com">Ingresá a este link!</a>
```
Con el atributo ``href`` le indicamos la URL a redireccionar.

Por defecto, al darle click va a abrir el link en la misma pestaña. Podemos cambiar esto con el atributo ``target``.

```html
<a href="https://google.com" target="_blank">Ingresá a este link!</a>
```

> "_blank" indica que el link se abrirá en una nueva pestaña.

También podes usar los links de la siguiente forma:

Si en vez de un texto, agregas una etiqueta ``img``, la imagen actuará como un link! Al darle click a la imagen, te redireccionará a la página.

```html
<a href="https://google.com">
    <img src="fotoDeGatito">
</a>
```

Los links se pueden usar de un montón de formas, como por ejemplo para **navegar entre páginas** (archivos HTML). En la sección de ejercicios vamos a ver como se hace esto.

## Tablas

|  Producto | Stock  | Precio Minorista  | Precio Mayorista  |
|---|---|---|---|
|  Pepsi | 34  |  $14.50 |  $13.00 |
|  Monster | 3  |  $10.00 |  $8.50 |

Las tablas son, tablas .. Te permiten definir columnas y filas, son totalmente personalizables (estilo) y son muy fáciles de crear.

Para crear una tabla, se utiliza la etiqueta ``table``.

```html
<table>

</table>
```

El contenido de una tabla, se define generalmente con dos etiquetas. 

``thead`` para definir la fila de columnas de encabezado (como lo son **Produto**, **Stock**, **Precio Minorista** y **Precio Mayorista**). (thead = cabeza tabla)

``tbody`` para definir las filas de columnas del contenido de la tabla. (cuerpo = tabla)

```html
<table>
    <!-- Dentro de la etiqueta thead, definimos la fila con las columnas de encabezado -->
    <thead>
    
    </thead>

    <!-- Dentro de la etiqueta tbody, agregamos las filas de contenido de la tabla -->
    <tbody>

    </tbody>
</table>
```

Ahora bien, para agregar filas (row) a nuestra tabla, se utiliza la etiqueta ``tr``. Sirven para agregar filas tanto en el encabezado como en el cuerpo de la tabla. (``tr`` = table row = fila de tabla)

```html
<table>
    <!-- Dentro de la etiqueta thead, definimos la fila con las columnas de encabezado -->
    <thead>
        <tr> <!-- Esta es una fila nueva -->
        
        </tr>
    </thead>

    <!-- Dentro de la etiqueta tbody, agregamos las filas de contenido de la tabla -->
    <tbody>
        <tr> <!-- Esta es una fila nueva -->
        
        </tr>
    </tbody>
</table>
```

Esto va a crear una fila nueva, pero para que podamos ver "algo", necesitamos agregarle columnas. Para esto se utilizan las etiquetas ``th`` (table head / encabezado de tabla) y ``td`` (table data-cell / dato o celda de tabla).

Los elementos ``th`` se usan para agregar una columna de tipo encabezado (como lo son **Producto**, **Stock**, **Precio Minorista** y **Precio Mayorista**) dentro del encabezado de la tabla ``thead``.

Los elementos ``td`` se usan para agregar una columna de "dato" o contenido dentro del cuerpo de la tabla ``tbody``.

Estos elementos se agregan dentro de una fila ``tr``, uno seguido del otro. Estos terminan definiendo el orden de las columnas.

Vamos a escribir la tabla de productos que vimos recién, en HTML.

```html
<table>

    <!-- Dentro de la etiqueta thead, definimos la fila con las columnas de encabezado -->
    <thead>
        <tr> <!-- Esta es una fila nueva -->
            <th>Producto</th> 
            <th>Stock</th> <!-- Cada th es una columna -->
            <th>Precio Mayorista</th>
            <th>Precio Minorista</th>
        </tr>
    </thead>

    <!-- Dentro de la etiqueta tbody, agregamos las filas de contenido de la tabla -->
    <tbody>
        <tr> <!-- Esta es una fila nueva -->
            <td>Pepsi</td>
            <td>34</td> <!-- Cada td es una columna -->
            <td>$14.50</td>
            <td>$13.00</td>
        </tr>

        <tr> <!-- Esta es una fila nueva -->
            <td>Monster</td>
            <td>3</td>
            <td>$10.00</td>
            <td>$8.50</td>
        </tr>
    </tbody>

</table>
```

En otro momento vamos a ver como personalizar las tablas. Ya que así como se ven por defecto, no son muy lindas. Las tablas se usan muchísimo en las páginas web.