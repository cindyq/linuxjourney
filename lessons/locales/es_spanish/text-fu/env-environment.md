# env (Environment)

## Lesson Content

Ejecuta el siguiente comando:

<pre>$ echo $HOME</pre>

Deberías ver la ruta de tu directorio home, el mío es /home/pete.

¿Qué pasa con este comando?

<pre>$ echo $USER </pre>

¡Deberías ver tu nombre de usuario!

¿De donde sale esta información? Pues sale de tus variables de entorno. Puedes verlas introduciendo

<pre>$ env </pre>

Esto saca bastante información acerca de las variables de entorno que tienes configuradas. Estas variables contienen información útil que la consola y otros procesos pueden usar.

Aquí va un pequeño ejemplo:

<pre>
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/bin
PWD=/home/user
USER=pete
</pre>

Una variable particularmente importante es la variable PATH. Puedes acceder a estas añadiendo $ delante del nombre de la variable tal que así:

<pre>
$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/bin
</pre>

Esto devuelve una lista de rutas separadas por punto y coma en las que tu sistema busca cuando ejecuta un comando. Digamos que descargas manualmente un paquete de internet, lo instalas y lo pones en un directorio inusual. Si quisieras ejecutar dicho comando, escribes $ comando_molon y la consola te dice que no se ha encontrado el comando. ¿Qué pasa? Estás buscando el binario en un directorio y sabes que está allí. Lo que ocurre es que la variable $PATH no comprueba ese directorio para los binarios y lanza un error.

Imagina que tienes cientos de binarios para ejecutar en un directorio, puedes modificar la variable $PATH para incluir dicho directorio en tu variable de entorno PATH.


## Exercise

¿Qué hace el siguiente comando? ¿Por qué?

<pre>$ echo $HOME</pre>

## Quiz Question

¿Cómo puedes ver tus variables de entorno?

## Quiz Answer

env
