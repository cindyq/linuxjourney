# ls (List Directories)

## Lesson Content

Ahora que sabemos como movernos en el sistema, ¿cómo sabemos lo está disponible a nuestro alrededor? Hasta ahora es como si nos moviéramos en la oscuridad. Podemos usar este genial comando para listar el contenido de una carpeta. El comando ls va a listar los archivos y carpetas presentes en el directorio actual por defecto, aunque podemos especificar que path queremos listar.

<pre>$ ls
$ ls /home/pete</pre>

ls es una herramienta bastante importante, que tambien muestra información sobre los archivos y carpetas que estas viendo.

También fijate que no todos los archivos dentro de la carpeta van a ser visibles. Los archivos cuyos nombres comiencen con . están ocultos, podes verlos sin embargo con la opción -a (ver "all" o todo).

<pre>$ ls -a</pre>

Hay también una opción mas útil, -l para ver la salida larga, que muestra una lista detallada. Esta lista contiene informacion detallada para cada archivo, comenzando de la izaquierda: permisos del archivo, número de links, nombre del dueño, grupo del dueño, tamaño del archivo, fecha y hora de la última modificación y nombre del archivo/carpeta.

<pre>$ ls -l</pre>

<pre>pete@icebox:~$ ls -l
total 80
drwxr-x--- 7 pete penguingroup   4096 Nov 20 16:37 Desktop
drwxr-x--- 2 pete penguingroup   4096 Oct 19 10:46  Documents
drwxr-x--- 4 pete penguingroup   4096 Nov 20 09:30 Downloads
drwxr-x--- 2 pete penguingroup   4096 Oct  7 13:13   Music
drwxr-x--- 2 pete penguingroup   4096 Sep 21 14:02 Pictures
drwxr-x--- 2 pete penguingroup   4096 Jul 27 12:41   Public
drwxr-x--- 2 pete penguingroup   4096 Jul 27 12:41   Templates
drwxr-x--- 2 pete penguingroup   4096 Jul 27 12:41   Videos</pre>

Los comandos tienen opciones llamadas flags o argumentos, como quieras llamarlos, que le agregan o cambian su funcionalidad. Fijate como agregamos -a y -l, uniéndolos en -la. El orden de estas opciones determina en qué orden van, la mayor parte del tiempo esto no importa demasiado así que podrías usar -al y todavía va a funcionar.

<pre>$ ls -la</pre>

## Exercise

Ejecuta ls con distantas opciones y fijate la salida que recibís.

## Quiz Question

¿Qué comando usarías para ver archivos ocultos?

## Quiz Answer

ls -a
