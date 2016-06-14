# sort

## Lesson Content

El comando sort es útil para ordenar líneas.

<pre>
file1.txt
dog
cow
cat
elephant
bird

$ sort file1.txt
bird
cat
cow
dog
elephant
</pre>

Puedes incluso hacer una ordenación inversa:

<pre>$ sort -r file1.txt
elephant
dog
cow
cat
bird
</pre>

Y también una ordenación via valor numérico:

<pre>$ sort -n file1.txt
bird
cat
cow
elephant
dog
</pre>

## Exercise

La verdadera potencia de sort esta en su posibilidad de ser combinado con otros comandos, ejecuta el siguiente comando y mira que sucede:

<pre>$ ls /etc | sort -rn</pre>

## Quiz Question

¿Qué etiqueta usas para hacer una ordenación inversa?

## Quiz Answer

-r
