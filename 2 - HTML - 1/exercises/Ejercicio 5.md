# Ejercicio 5

Por último, vamos a agregarle una imágen a nuestra página justo antes del botón de **Compartir Noticia**.

Cómo se agrega una imágen? Con el elemento ``<img>``

Ejemplo

```HTML
<img>
```

Pero el elemento ``<img>`` por si solo no representa nada. Para indicarle cuál es la imagen a mostrar, debemos agregarle un atributo a este elemento.

Pero.. Que carajo es un **atributo**? Un atributo es una palabra clave que permite modificar un elemento HTML. Los atributos se escriben dentro de la etiqueta de inicio. 

Ejemplo

```HTML
<!-- align es una atributo que modifica la posición del texto -->
<!-- "center" hace que el texto se posicione en el "centro" de la página -->
<h1 align="center">
    Marcelo Araujo
</h1>
```

Ahora bien, para indicarle a nuestro elemento ``<img>`` cual será la imágen a mostrar, debemos usar el atributo **src**.

Ejemplo

```HTML
<img src="urlDeLaImagenAMostrar">
```

Ahora que sabemos como decirle al elemento ``<img>`` cual imágen mostrar, busquen en google una imagen que represente el poder de los gatos ante los perros.

Por ejemplo busquen: **cat hits dog**.

Cuando la encuentren, denle click y luego presionen 'Copiar dirección de imágen'.

Luego ingresen lo copiado como valor del atributo **src**.