# cut

## Lesson Content

Vamos a aprender unos cuantos comandos que serán de utilidad a la hora de procesar texto. Antes de comenzar, creemos un archivo sobre el que trabajaremos. Copia y pega el siguiente comando, una vez hecho eso inserta un TAB entre perro y perezoso (mantén pulsado Ctrl-v + TAB).

<pre>$ echo 'El rápido zorro; marrón salta sobre el     perro perezoso' > sample.txt</pre>

El primer comando que aprenderemos a usar es cut. Este comando extrae partes de un texto de un archivo.

Para extraer contenidos dados por una lista de caracteres:

<pre>$ cut -c 5 sample.txt</pre>

Esto saca el quinto caracter de cada línea del archivo. En este caso es "á", ya que el espacio en blanco también cuenta como un caracter.

Para extraer los contenidos por campos, tenemos que hacer una pequeña modificación:

<pre>$ cut -f 2 sample.txt</pre>

La etiqueta -f hace que se saque texto basado en campos, por defecto se usan TABs como delimitadores, por lo que todo lo que este separado con un TAB se considera un campo. Deberías ver "perro" en la salida.

Se pueden combinar la etiqueta de campo con la etiqueta de delimitador para extraer el contenido dado por un delimitador a medida:

<pre>$ cut -f 1 -d ";" sample.txt</pre>

Esto cambiará el delimitador TAB por ";" y, como estamos cortando el primer campo, el resultado debería ser "El rápido zorro".

## Exercise

¿Qué hacen los siguientes comandos? ¿Por qué?

<pre>$ cut -c 5-10 sample.txt
$ cut -c 5- sample.txt
$ cut -c -5 sample.txt
</pre>

## Quiz Question

What command would you use to get the first character of every line in a file?

## Quiz Answer

cut -c 1
