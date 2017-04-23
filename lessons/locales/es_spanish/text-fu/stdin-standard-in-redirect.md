# stdin (Standard In)

## Lesson Content

En nuestra anterior lección aprendimos que podemos usar distintos canales de salida standard, tales como un archivo o la pantalla. Pues bien, tambien hay distintos canales de entrada (stdin) que podemos usar. Sabemos que existe el stdin desde dispositivos como el teclado, pero tambien podemos usar archivos, salidas desde otros procesos y la terminal, veamos un ejemplo.

Usemos el archivo peanuts.txt de la lección previa en este ejemplo, recuerda que tenía el texto Hola Mundo.

<pre>$ cat <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt </pre>

De la misma forma que que teníamos <b>&gt;</b> para redirección de stdout, podemos usar <b>&lt;</b> para redireccionar stdin.

Normalmente, en el comando cat, mandas un archivo y dicho archivo se convierte en la entrada standard, en este caso, hemos redireccionado peanuts.txt para que sea nuestra stdin. Por tanto, la salida de cat peanuts.txt que sería Hola Mundo se redirecciona a otro archivo llamado banana.txt.

## Exercise

Ejecuta un par de comandos:
<pre>
$ echo <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
$ ls <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
$ pwd <b>&lt;</b> peanuts.txt <b>&gt;</b> banana.txt
</pre>

## Quiz Question

¿Qué redirector usas para redireccionar stdin?

## Quiz Answer

<
