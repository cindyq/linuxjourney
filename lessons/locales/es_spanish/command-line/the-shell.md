# La Shell

## Lesson Content 

El mundo es tu ostra, o mejor dicho la shell[^1] es tu ostra. ¿Que es la shell? Básicamente la shell es un programa que recibe comandos del teclado y los transmite al sistema operativo para que los ejecute. Si alguna vez utilizaste un GUI probablemente viste que había un programa llamado "Terminal" o "Console", estos son simplemente programas que inician un shell. A lo largo de este curso aprenderemos las maravillas de la shell.

En este curso usaremos el programa de shell "bash" (Bourne Again SHell), casi todas las distribuciones de linux vienen con bash por defecto. Existen otras shell como ksh, zsh, tsch, pero no veremos ninguna de ellas aquí.

Pongamos manos a la obra! Dependiendo de la distribución la shell podría verse distinto, pero en su mayoría debería adherirse al siguiente formato:
<pre>username@hostname:current_directory
pete@icebox:/home/pete $</pre>

¿Has notado el símbolo $ al final del interprete de comandos? Las distintas shells tendrán distintos interpretes, en este caso $ es para un usuario normal usando la shell Bash, Bourne o Korn, no hace falta que escribas $ cuando tipees un comando, solo recuerda que existe.

Empecemos con un comando simple, echo. El comando echo solo imprime el texto en la pantalla.

<pre>$ echo Hola Mundo</pre>

[^1]: NdT. La palabra "shell" en ingles significa caparazón.

## Exercise 

Prueba estos comandos para ver el resultado:

<ol>
<li>$ date</li>
<li>$ whoami</li>
</ol>

## Quiz Question

Que deberia imprimirse en la pantalla cuando escribes echo Hola Mundo?

## Quiz Answer

Hola Mundo


