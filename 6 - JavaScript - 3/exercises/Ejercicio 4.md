# Ejercicio 4

#### En una página web sin contenido, realizar la siguiente consigna:

Un amigo nos pidió un "programa" para calcular cuánto le va a costar salir a comprarse ropa. Su local favorito tiene los siguientes precios:

- Remeras: $400
- Pantalones: $750
- Zapatillas: $1300

Él quiere poder ingresar el producto a comprar, seguido de la cantidad. Y que al final, le muestre el total de la compra. Ejemplo:

"Ingrese el producto a comprar": ``remera``

"Ingrese la cantidad a comprar": 3

3 (cantidad) * 400 (precio por remera) = $1200

---

Extra:

Nuestro amigo está contento, pero no del todo... Quiere poder comprar mas de un tipo de producto, como por ejemplo remeras y pantalones. Por lo tanto necesita que el programa le siga preguntando por mas compras, hasta que no tenga mas nada que comprar y pueda detener el programa.

Hablando en detalle, necesita que:

El programa le permita ingresar productos a comprar, y que luego de ingresar un producto el programa le pregunte:

``'Desea seguir comprando?'``

- Si él ingresa la palabra ``'si'``, el programa le tendrá que volver a pedir que ingrese un producto (y la cantidad obviamente)
- Si él ingresa la palabra ``'no'``, el programa dejará de preguntarle y le mostrará el total de dinero que deberá pagar, terminando así el programa.

Ayuda:

> Probablemente tengan que usar un bucle para seguir pidiendo productos y un ``if`` para decidir si hay que seguir preguntando o no.