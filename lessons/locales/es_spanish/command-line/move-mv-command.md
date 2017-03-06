# mv (Move)

## Lesson Content

El comando mv (por move, "mover" en inglés) es utilizado para mover archivos y también renombrarlos. Bastante similar al comando cp en términos de sus opciones y funcionalidad.

Podes renombrar archivos así:

<pre>$ mv archivoViejo archivoNuevo</pre>

O podes mover un archivo a una carpeta diferente:

<pre>$ mv archivo2 /home/pepe/Documentos</pre>

Y mover mas de un archivo a la vez:

<pre>$ mv archivo_1 archivo_2 /Carpeta</pre>

Podes renombrar carpetas también:

<pre>$ mv carpeta1 carpeta2</pre>

Como cp, si moves con mv un archivo o directorio, el comando va a sobreescribir cualquier cosa que esté en ese directorio. Entonces podes usar la opción -i para preguntarte antes de que sobreescriba algo.

<pre>mv -i carpeta1 carpeta2</pre>

Digamos que querés mover un archivo para sobreecribir el previo. Podes también hacer un backup de ese archivo y va a renombrar la versión vieja con un ~. 

<pre>$ mv -b carpeta1 carpeta2</pre>

## Exercise

Renombrá un archivo y mové ese archivo a una carpeta diferente.

## Quiz Question

¿Cómo renombrás un archivo llamado gato a perro?

## Quiz Answer

mv gato perro
