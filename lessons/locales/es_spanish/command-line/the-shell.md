# The Shell

## Lesson Content

El mundo es tu ostra ¿O en realidad el shell es tu ostra?¿Que es el shell? El shell es basicamente un programa que toma tus comandos desde el teclado y los envia al sistema operativo para ejecutarlos. Si alguna vez has usado una GUI, probablemente has visto programas como "Terminal" o "Console" estos son solamente programas que ejecutan un shell por ti. En todo este curso, vamos a estar aprendiendo acerca de las maravillas del shell.

En este curso usaremos el programa de shell bash (Bourne Again shell), casi todas las distribuciones de Linux traen por defecto el shell bash. Hay otros shell disponibles como lo son ksh, zsh, tsch, pero no entraremos en ninguno de ellos.

¡Vamos directo a ello! Dependiendo de la distribucion, el prompt de tu shell se verá distinto, pero para la mayor parte debería adherirse al siguiente formato:
<pre>nombre_de_usuario@nombre_de_host:actual_directorio
pete@icebox:/home/pete $</pre>

Nota el signo $ al final del prompt. Diferentes shells tendrán digerentes prompts, en nuestro caso el signo $ es para un usuario normal usando Bash, Bourne o Korn shell, no necesitas agregar el simbolo del prompt cuando escribas el comando, solo sabe que está ahí.

Vamos a empezar con un simple comando, echo. El comando echo solo imprime en pantalla el texto que recibe como argumento.

<pre>$ echo Hello World</pre>

## Exercise

Intenta otros comandos de Linux y ve cual es su salida (output):

<ol>
<li>$ date</li>
<li>$ whoami</li>
</ol>

## Quiz Question

¿Qué deberia ser impreso en pantalla cuando escribes echo Hello World?

## Quiz Answer

Hello World