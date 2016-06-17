# stdout (Standard Out)

## Lesson Content

Por ahora, nos hemos familiarizado con muchos comandos y sus salidas, lo que nos lleva al siguiente tema, canales E/S (entrada/salida). Ejecutemos el siguiente comando y veamos como funciona.

<pre>$ echo Hello World > peanuts.txt</pre>

¿Qué ha ocurrido? Comprobaremos el directorio donde ejecutaste ese comando y deberías ver un archivo llamado peanuts.txt, mira dentro del archivo y deberías ver el texto Hello World. Han ocurrido muchas cosas en un solo comando, asi que veamos que ha pasado.

Primero, centrémonos en la primera parte:

<pre>$ echo Hello World</pre>

Sabemos que esto imprime Hello World por pantalla, ¿pero cómo lo hace? Los procesos usan canales E/S para recibir entradas y devolver salidas. Por defecto, el comando echo toma la entrada (entrada standard o stdin) desde el teclado y devuelve la salida (salida standard o stdout) por pantalla. Así que cuando escribes escribes echo Hello World en tu terminal, obtienes Hello World en la pantalla. Sin embargo, la redirección E/S nos permite cambiar este comportamiento por defecto dándonos una gran flexibilidad con los archivos.

Continuemos con la siguiente parte del comando:

<pre> > </pre>

El símbolo > es un operador de redirección que nos permite cambiar hacia donde sale la salida standard. Nos permite enviar la salida de echo Hello World a un archivo en vez de a la pantalla. Si el archivo realmente no existe, lo creará para nosotros. Sin embargo, si existe, lo sobreescribirá (puedes añadir una etiqueta en la terminal para prevenirlo, dependiendo del tipo de consola que estes usando).

Y así es como funciona la redirección de la salida standard.

Digamos que no quiero sobreescribir peanuts.txt, por suerte hay un operador de redirección para eso, >>:

<pre>$ echo Hello World >> peanuts.txt</pre>

Esto añadirá Hello World al final de peanuts.txt, si el archivo no existe todavía, lo creará para nosotros tal y como lo hace el operador >.


## Exercise

Ejecuta un par de comandos:

<pre>
$ ls -l /var/log > myoutput.txt
$ echo Hello World > rm
$ > somefile.txt
</pre>

## Quiz Question

¿Qué redirector usas para añadir una salida a un archivo?

## Quiz Answer

<pre> >>
</pre>
