# regex (Regular Expressions)

## Lesson Content

Las expresiones regulares son una poderosa herramienta para seleccionar en base a patrones. Usan una notación especial similar a la ya vista como los wildcards.

Veremos un par de las más comunes expresiones regulares, aquellas que son casi universales en casi cualquier lenguaje de programación.

Usaremos esta frase como nuestra cadena de prueba:
<pre>
sally sells seashells
by the seashore
</pre>

<b>1. Principio de una línea con ^</b> nos dará como resultado "by the seashore"

<pre>
<b>^</b>
</pre>

<b>2. Final de una línea con $</b> nos dará como resultado "by the seashore"

<pre>
seashore<b>$</b>
</pre>

<b>3. Coincidencia con cualquier caracter con .</b> nos dará como resultado

<pre>
b<b>.</b>
</pre>

<b>4. Bracket notation with [] and ()</b>

This can be a little tricky, brackets allow us to specify characters found within the bracket.

<pre>
d<b>[iou]</b>g
would match: dig, dog, dug
</pre>

The previous anchor tag ^ when used in a bracket means anything except the characters within the bracket.

<pre>
d<b>[^i]</b>g
would match: dog and dug but not dig
</pre>

Brackets can also use ranges to increase the amount of characters you want to use.

<pre>
d<b>[a-c]</b>g
will match patterns like dag, dbg, and dcg
</pre>

Be careful though as brackets are case sensitive:

<pre>
d<b>[A-C]</b>g
will match dAg, dBg and dCg but not dag, dbg and dcg
</pre>

And those are some basic regular expressions.

## Exercise

Intenta combinar las expresiones regulares con grep y busca algo en algunos archivos.

<pre>
grep [expresión regular] [archivo]

## Quiz Question

¿Qué expresión regular usarías si quisieras buscar un caracter individual?

## Quiz Answer

.
