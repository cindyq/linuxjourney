# mv (Move)

## Lesson Content

Utilizado para mover archivos y también renombrarlos. Bastante similar al comando cp en términos de sus opciones y funcionalidad.

Podes renombrar archivos así:

<pre>$ mv oldfile newfile</pre>

O podes mover un archivo a una carpeta diferente:

<pre>$ mv file2 /home/pete/Documents</pre>

Y mover mas de una rchivo a la vez:

<pre>$ mv file_1 file_2 /somedirectory</pre>

Podes renombrar carpetas también:

<pre>$ mv directory1 directory2</pre>

Como cp, si mv un archivo o directorio va a sobreescribir cualquier cosa que esté en ese directorio. Entonces podes usar la opción -i para preguntarte antes de que sobreescriba algo.

<pre>mv -i directory1 directory2</pre>

Digamos que querías mover un archivo para sobreecribir el previo. Podes también hacer un backup de ese archivo y va a renombrar la versión vieja con un ~. 

<pre>$ mv -b directory1 directory2</pre>

## Exercise

Renombrá un archivo, y mové ese archivo a una carpeta diferente.

## Quiz Question

¿Cómo renombrás un archivo llamado cat a dog?

## Quiz Answer

mv cat dog
