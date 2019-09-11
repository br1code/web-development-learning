# Ejercicio 9

#### En una página web sin contenido, realizar la siguiente consigna:

Eres un empleado público de la ANSES, y estás en los últimos 15 minutos de tu turno de trabajo.

Tienes las siguientes personas en la cola esperándote:

```js
var personasEnCola = ['Carlos', 'Juan', 'Florencia', 'Bruno', 'Ana', 'Sebastian', 'Marcelo'];
```

Te das cuenta de que hay 7 personas en la cola, y que gracias a tus años de experiencia sabes que seguro vas a llegar a atender solo a 5.

Lo ideal sería que vayas a avisarle a las últimas dos personas que no vas a llegar a atenderlas para que se vayan, pero sabes que estuvieron esperando 1 hora y media y además ya tienen el papel del turno en la mano. Aunque tuviste un día de mierda y eso ya no te importa, por lo tanto tomaste una decisión:

> Voy a recibir a todas las personas, una por una sin saltearme ninguna. Al terminar de atender a cada persona, voy a gritar ``'Siguiente!!'``. **Pero** a las últimas dos personas les voy a gritar ``'Ya cerramos, vuelva prontos!!!'`` a cada una y luego voy a salir de mi puesto.

Al final, antes de irte, tienes que gritarle a tu jefe que te vas con un texto de ``'Chau, me voy. Nos vemos mañana'!!``

Aclaración:

- Atender a una persona es algo ficticio. No hace falta mostrar un mensaje. Solo es necesario avisar que tiene que pasar el siguiente.

Condiciones:

- No se puede utilizar mas de un bucle para recorrer la lista de ``personasEnCola``.