# join and split

## Lesson Content

El comando join te permite unir archivos que tengan un campo en común:

Digamos que tenía dos archivos y quería unirlos:
<pre>file1.txt
1 John
2 Jane
3 Mary

file2.txt
1 Doe
2 Doe
3 Sue

$ join file1.txt file2.txt
1 John Doe
2 Jane Doe
3 Mary Sue
</pre>

¿Te has fijado como uní los archivos? Fueron unidos usando el primer campo por defecto, teniendo que ser estos idénticos. Si no lo son puedes ordenarlos, por lo que en este caso los archivos serían unidos via 1, 2, 3.

¿Cómo unirías los siguientes archivos?

<pre>file1.txt
John 1
Jane 2
Mary 3

file2.txt
1 Doe
2 Doe
3 Sue
</pre>

Para unir este archivo tienes que especificar que campos vas a unir, en este caso queremeos el campo 2 del archivo file1.txt y el campo 1 del archivo file2.txt, con lo que el comando a usar sería algo así:

<pre>
$ join -1 2 -2 1 file1.txt file2.txt
1 John Doe
2 Jane Doe
3 Mary Sue
</pre>

-1 se refiere al archivo file1.txt y -2 al archivo file2.txt. Puedes incluso separar un archivo en varios archivos con el comando split:

<pre>$ split somefile</pre>

Esto separará el archivo en diferentes archivos, por defecto los separará una vez al alcanzar el límite de 1000 líneas. Los archivos seran nombrados como x** por defecto.

## Exercise

Une dos archivos con distinto número de lineas, ¿qué ocurre?

## Quiz Question

¿Qué comando usarías para unir archivos llamados cat dog cow?

## Quiz Answer

join cat dog cow
