# Ejercicio 3

Para terminar este módulo de HTML, vamos a utilizar el verdadero poder de los **links**.

Así como pudimos usar un link para redireccionar a una página externa, también podemos usar los links para navegar entre nuestras páginas.

O pensaban que las páginas definian TODO su contenido solo en el index.html?.

Si recuedan que al adjuntar un archivo javascript o un archivo de css, en el atributo ``href`` o ``src`` escribiamos la ruta **local** de donde estaba el archivo en nuestra carpeta. Lo mismo necesitamos para crear un link hacia una página local.

Suponiendo que tenemos el siguiente directorio:

```md
CarpetaPrincipal    
└─── index.html            # Archivo HTML para la página principal
└─── otraPagina.html       # Otro archivo HTML con otra sección
└─── index.js              # Archivo Javascript para tu página principal
└─── index.css             # Archivo CSS para tu página principal
```

La ruta desde nuestro index.html hacia otraPagina.html, sería ``"./otraPagina.html"``.

> Recordá que escribir ``./`` indica que te estás refiriendo a la misma carpeta en donde está el archivo actual (en este caso index.html).

Por lo tanto, para crear un link desde index.html hacia otraPagina.html, se escribiria de la siguiente forma:

```html
<a href="./otraPagina.html">Link hacia otraPagina.html</a>
```

Bien! Ahora que sabemos como hacer esto:

- En la página principal (**index.html**), crear un link que vaya hacia la página de gatos (**gatos.html**).
- En la página de gatos (**gatos.html**), crear un link que vuelva hacia la página principal (**index.html**).

> Si necesitas mas ayuda, podes ver el ejemplo "navigate-between-pages-example" en la carpeta de ejemplos.