# grep

## Lesson Content

El comando grep puede ser el comando más común a la hora de procesar texto que usarás. Permite buscar en archivos carácteres que coincidan con un cierto patrón. ¿Qué pasa si quieres saber si existe un archivo en un directorio o si quieres ver si una cadena de texto esta contenida en un archivo? Seguramente no revisaras cada linea de texto, usaras grep!

Usemos nuestro archivo de muestra sample.txt como ejemplo:

<pre>$ grep zorro sample.txt</pre>

Deberías ver que grep encontró zorro en el archivo sample.txt.

Puedes also buscar patrones con independencia de si están en mayúscula o minúscula usando la etiqueta -i:

<pre>$ grep -i algunpatron algunarchivo</pre>

Para darle un poco más de flexibilidad, puedes combinarlo con otros comando con |.

<pre>$ env | grep -i User</pre>

Como puedes ver grep es muy versátil. Puedes incluso usar expresiones regulares en tu patrón:

<pre>$ ls /algundirectorio | grep '.txt$'</pre>

Debería devolver todos los archivos acabados en .txt en algundirectorio.

## Exercise

Puedes haber oido hablar de egrep o fgrep, estos son comandos anticuados que han sido sustituidos por grep -E y grep -F. Lee la página de ayuda de grep para aprender más.

## Quiz Question

¿Qué comando usas para buscar un patrón determinado?

## Quiz Answer

grep
