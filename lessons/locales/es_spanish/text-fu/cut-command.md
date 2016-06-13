# cut

## Contenido de la lección

Vamos a aprender unos cuantos comandos que serán de utilidad a la hora de procesar texto. Antes de comenzar, creemos un archivo sobre el que trabajaremos. Copia y pega el siguiente comando, una vez hecho eso inserta un TAB entre perro y perezoso (mantén pulsado Ctrl-v + TAB).

<pre>$ echo 'El rápido zorro marrón salta sobre el perro perezoso' > sample.txt</pre>

First command we'll be learning about is the cut command. It extracts portions of text from a file.

To extract contents by a list of characters:

<pre>$ cut -c 5 sample.txt</pre>

This outputs the 5th character in each line of the file. In this case it is "q", note that the space also counts as a character.

To extract the contents by a field, we'll need to do a little modification:

<pre>$ cut -f 2 sample.txt</pre>

The -f or field flag cuts text based off of fields, by default it uses TABs as delimiters, so everything separated by a TAB is considered a field. You should see "dog" as your output.

You can combine the field flag with the delimiter flag to extract the contents by a custom delimiter:

<pre>$ cut -f 1 -d ";" sample.txt</pre>

This will change the TAB delimiter to a ";" delimiter and since we are cutting the first field, the result should be "The quick brown".

## Exercise

What does the following command do? Why?

<pre>$ cut -c 5-10 sample.txt
$ cut -c 5- sample.txt
$ cut -c -5 sample.txt
</pre>

## Quiz Question

What command would you use to get the first character of every line in a file?

## Quiz Answer

cut -c 1
