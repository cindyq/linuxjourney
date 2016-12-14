# cp (Copy)

## Lesson Content

Comencemos por hacer algunas copias de archivos. Semejante a copiar y pegar archivos en otros sistemas operativos, el shell nos brinda una forma simplificada de hacerlo.

<pre>$ cp mycoolfile /home/pepe/Documentos/cooldocs</pre>

mycoolfile es el archivo que queres copiar y /home/pepe/Documentos/cooldocs es la ubicación donde a la que lo estas copiando

Podes copiar múltiples archivos y carpetas usando wildcards. Un wildcard es un caracter que puede ser sustituido en una selección basada en patrones, brindándote mayor flexibilidad en las búsquedas.


<ul>
<li>* el wildcard de los wildcards, es utilizado para representar todos y cada uno de los caracteres de cualquier string.</li>
<li>? representa un único caracter</li>
<li>[] representa cualquier caracter entre los corchetes</li>
</ul>

<pre>$ cp *.jpg /home/pepe/Fotos</pre>

Este comando copia todos los archivos con la extensión .jpg en el directorio actual en la carpeta Fotos.

Un comando útil se consigue agregando la opción -r, que copia recursivamente los archivos y directorios dentro de alguna carpeta.

Intentá hacer cp en una carpeta que contenga un par de archivos dentro de tu carpeta Documentos. ¿No funcionó? Bueno eso es porque necesita copiar los archivos y carpetas dentro también con la opción -r.

<pre>$ cp -r Pumpkin/ /home/pepe/Documentos</pre>

Una cosa para remarcar, si copias un archivo dentro de una carpeta que tiene el mismo nombre, el archivo va a ser sobreescrito con lo que sea que estes copiando bajo ese mismo nombre ahora. Esto no es bueno si no queremos que nuestro antiguo archivo sea sobreescrito accidentalmente. Podes usar la opción -i (interactivo) para preguntarte antes de sobreescribir cualquier archivo.  

<pre>$ cp -i mycoolfile /home/pepe/Fotos</pre>

## Exercise

Copiá un par de archivos, con cuidado de no sobreescribir algo importante.

## Quiz Question

¿Qué opción es necesario especificar para copiar recursivamente una carpeta?

## Quiz Answer

-r
