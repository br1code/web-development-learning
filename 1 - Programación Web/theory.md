# Programacion Web

La **Programación Web** es una de las "ramas" del desarrollo de software, como lo son el desarrollo de aplicaciones de escritorio, aplicaciones mobile, etc.

En resumen, por ahora vamos a limitar a la Programacion Web a **"el desarrollo de paginas web"**. Mas adelante se van a dar cuenta que no es solo esto, pero para empezar es suficiente.

No creo que haga falta explicar que es una pagina web, ya que las usan a diario. Pero lo que si se van a dar cuenta facil es que, acceden a una pagina web desde un **navegador** (ya sea chrome, internet explorer, mozilla, hasta un navegador de tu celular como chrome), y el navegador es quien se encarga de **interpretar** el "codigo" y mostrar la pagina como se debe. 

Ahora hablemos de este "**codigo**". Una pagina web, en la actualidad, consiste de tres principales tecnologias/lenguajes.

- **HTML**
  - Es un lenguaje de marcado, que se basa en escribir etiquetas de inicio y de cierre, para definir la estructura y el contenido de la pagina web.
- **CSS**
  - Es un lenguaje de diseño gráfico que sirve para escribir reglas que definiran como se tiene que ver el contenido de una pagina web.
- **Javascript**
  - Es un lenguaje de programacion o mejor definidio, de scripting. Permite definir el comportamiento y ejecutar acciones en una pagina web.

> Que es **scripting**? Lo van a ver mas adelante, pero una definicion simple es que es un lenguaje que no necesita ser procesado y traducido a otro lenguaje (compilar) para ejecutarse. Con Javascript podes ejecutar tu codigo sin necesidad de compilar.

Veamos un ejemplo de una pagina web con una estructura convencional de archivos.
#### Ejemplo: index.html
```HTML
<!DOCTYPE html>
<html>
<head> <!-- Adentro de la etiqueta head, iran etiquetas de 'configuracion' de la pagina  -->
    <title>Mi Pagina Web</title> <!-- Titulo de la pagina  -->
    <link rel="stylesheet" href="style.css"> <!-- Agregamos nuestro archivo de CSS  -->
</head>
<body> <!-- Adentro de la etiqueta body, ira el contenido de nuestra pagina  -->
    <h1>Hola!</h1>
    <script src="app.js"></script> <!-- Agregamos nuestro archivo de Javascript  -->
</body>
</html>
```

#### Ejemplo: style.css

```CSS
/* Regla que define que cualquier elemento h1 tendra su texto de color rojo */
h1 {
    color: red;
}
```
#### Ejemplo: app.js

```JS
// Ejecutamos una funcion de alerta con el mensaje 'Que onda?'
alert('Que onda?');
```

> Puedes ver este ejemplo en la carpeta 'examples' de este modulo.

Al abrirlo, nos vamos a encontrar con una pagina con un titulo 'Mi Pagina Web', un texto encabezado 'Hola!'. Esto es lo que definimos en nuestro archivo de HTML.

Ademas, seguramente salio una alerta con un mensaje. Exactamente como lo definimos en nuestro archivo javascript.

Y por si no te habias dado cuenta, en nuestro archivo CSS definimos una regla para que cualquier elemento del tipo H1 dentro de nuestra pagina tenga el color rojo.

Con esto podemos recordar la frase anterior. El navegador es el que se encarga de leer e interpretar el HTML (estructura de elementos, por ejemplo el titulo y el texto encabezado), el CSS (estilos de la pagina, por ejemplo el color del texto), y el Javascript (acciones y comportamientos, por ejemplo mostrar una alerta).

> En este mini curso, vamos a aprender un poco de cada una de estas tres. Enfocandonos principalmente en HTML y Javascript.