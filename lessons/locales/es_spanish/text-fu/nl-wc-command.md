# wc y nl

## Lesson Content

El comando wc (word count) muestra el número total de palabras en un archivo.

<pre>$ wc /etc/passwd
 96     265    5925 /etc/passwd
</pre>

Muestra el número de líneas, el número de palabras y el número de bytes, respectivamente.

Para ver solo el número de un campo concreto, usa las etiquetas, -l, -w o -c, respectivamente.

<pre>$ wc -l /etc/passwd
96</pre>

Otro comando que puedes usar para comprobar el número de líneas de un archivo es el comando nl (number lines).

<pre>
file1.txt
i
like
turtles
</pre>

<pre>$ nl file1.txt
1. i
2. like
3. turtles
</pre>

## Exercise

¿Cómo obtendrías el número total de líneas usando el archivo nl sin buscar el número en la salida del comando? Pista: Usa algún comando que hayas aprendido en el curso.

## Quiz Question

¿Qué comando usarías para obtener solamente el número total de palabras de un archivo?

## Quiz Answer

wc -w
