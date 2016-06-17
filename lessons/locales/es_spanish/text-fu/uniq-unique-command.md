# uniq (Unique)

## Lesson Content

El comando uniq es otra útil herramienta para parsear texto.

Digamos que tienes un archivo con muchas duplicidades:

<pre>
reading.txt
book
book
paper
paper
article
article
magazine
</pre>

Si quieres quitar las duplicidades, puedes usar el comando uniq:

<pre>$ uniq reading.txt
book
paper
article
magazine</pre>

Se pueden obtener el número de ocurrencias de una línea:

<pre>$ uniq -c reading.txt
2 book
2 paper
2 article
1 magazine</pre>

Se pueden obtener solo los valores únicos:

<pre>$ uniq -u reading.txt
magazine</pre>

Se pueden obtener solo los valores duplicados:

<pre>$ uniq -d reading.txt
book
paper
article
</pre>

<b>Nota</b> : uniq no detecta líneas duplicadas a menos que sean adyacentes. Por ejemplo:

Digamos que tienes un archivo con duplicidades que no son adyacentes:

<pre>
reading.txt
book
paper
book
paper
article
magazine
article
</pre>

<pre>$ uniq reading.txt
reading.txt
book
paper
book
paper
article
magazine
article</pre>

El resultado devuelto por uniq contendrá todas las entradas tal y como aparecen en el primer ejemplo.

Para salvar esta limitación de uniq podemos usar sort en combinación con uniq:

<pre>
$ sort reading.txt | uniq
article
book
magazine
paper</pre>

## Exercise

¿Qué resultados obtendrías si ejecutas uniq -uc?

## Quiz Question

¿Qué comando usarías para quitar duplicidades en un archivo?

## Quiz Answer

uniq
