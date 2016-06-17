# stderr (Standard Error)

## Lesson Content

Intentemos algo distinto, por ejemplo listar los contenidos de un directorio que no existe en tu pc y redirigir la salida al archivo peanuts.txt.

<pre>$ ls /fake/directory > peanuts.txt </pre>

Lo que verías es:

<pre>ls: cannot access /fake/directory: No such file or directory</pre>

Estarás pensando, ¿no debería haberse enviado dicho mensaje al archivo? De hecho, existe otro canal de E/S en juego llamado standard error (stderr). Por defecto, stderr envia su salida también a la pantalla, siendo un canal completamente diferente al stdout. Por tanto, necesitarás redirigir su salida de otra forma.

Por desgracia, el redictor no es tan fácil como usar <b>&lt;</b> o <b>&gt;</b> pero no es mucho más díficil. Tendremos que usar descriptores de archivo. Un descriptor de archivo es un número no negativo que se usa para acceder a un archivo o canal. Profundizaremos en ello más tarde, pero por ahora saber que los descriptores de archivo para stdin, stdout y stderr son 0, 1 y 2, respectivamente.

Así que ahora si queremos redirigir nuestro stderr al archivo podemos hacer esto:

<pre>$ ls /fake/directory 2> peanuts.txt</pre>

Deberías ver los mensajes de stderr solo en peanuts.txt.

Pero, ¿qué pasa si quisiera ver ambos stderr y stdout en el archivo peanuts.txt? Es posible hacerlo también con descriptores de archivo:

<pre>$ ls /fake/directory > peanuts.txt 2>&1</pre>

Esto envia los resultados de ls /fake/directory al archivo peanuts.txt y luego redirecciona stderr a stdout via 2>&1. El orden de operaciones es importante aquí, 2>&1 envia stderr a dondequiera que stdout esté apuntando. En este caso, stdout esta apuntando a un archivo, por lo que 2>&1 también envía stderr a un archivo. Por lo tanto, si abres el archivo peanuts.txt deberías ver ambos, stderr y stdout. En nuestro caso, el comando anterior solo saca stderr.

Hay una forma más corta de redirigir ambos stdout y stderr a un archivo:

<pre>$ ls /fake/directory &> peanuts.txt</pre>

Ahora, ¿qué pasa si no quiero nada de eso y quiero deshacerme de los mensajes de stderr por completo? Bien, puedes redirigir la salida a un archivo especial llamado /dev/null que descartará cualquier entrada.

<pre>$ ls /fake/directory 2> /dev/null</pre>

## Exercise

¿Qué hace el siguiente comando?

<pre>$ ls /fake/directory >> /dev/null 2>&1</pre>

## Quiz Question

¿Cuál es el redirecotr para stderr?

## Quiz Answer

2>
