# paste

## Lesson Content

El comando paste es parecido al comando cat, une líneas en un archivo. Creemos un nuevo archivo con los siguientes contenidos:

<pre>
sample2.txt
El
rápido
zorro
marrón
</pre>

Combinemos todas las líneas en una sola:

<pre>$ paste -s sample2.txt</pre>

El delimitador por defecto para pegar es TAB, por lo que ahora hay una línea con TAB separando cada palabra.

Cambiemos este delimitador (-d) por algo más apropiado:

<pre>$ paste -d ' ' -s sample2.txt</pre>

Ahora todo debería estar en una línea delimitada con espacios.

## Exercise

Intenta pegar varios archivos juntos, ¿qué ocurre?

## Quiz Question

¿Qué etiquete usas con paste para que todo se una en una sola línea?

## Quiz Answer

-s
