# The Shell

## Lesson Content

"El mundo es tu entorno" o en realidad el shell es tu entorno en este caso. ¿Qué es el shell? El shell es básicamente el programa que acepta los comandos que escribís y los envía al sistema operativo para que los ejecute. Si alguna vez usaste una GUI, probablemente hayas visto programas como "Terminal" o "Consola" que ejecutan un shell por vos. A lo largo de todo este curso vamos a conocer las maravillas del shell.

En este curso vamos a usar el shell bash (Bourne Again Shell); casi todas las distribuciones Linux vienen con bash como shell por defecto. Hay otros shells disponibles también, como sh, ksh, zsh, tsch pero no vamos a estudiar ninguno de esos ahora.

Comencemos! Dependiendo de la distribución tu shell prompt puede variar, pero en general se ve más o menos con este formato:

<pre>username@hostname:current_directory
pete@icebox:/home/pete $</pre>

Observaste $ al final del prompt? Shells diferentes van a tener prompts diferente, en nuestro caso el $ representa un usuario normal logueado en Bash, Bourne o Korn shell. No hay que agregar el símbolo en el prompt cuando escribimos un comando, por ahora nos alcanza con saber que está ahí.

Comencemos con un comando simple, echo. El comando echo simplemente imprime en la salida los argumentos que reciba.

<pre>$ echo Hola Mundo</pre>

## Exercise

Proba algunos otros comando Linux y fijate la salida:

<ol>
<li>$ date</li>
<li>$ whoami</li>
</ol>

## Quiz Question

¿Cuál tendría que ser la salida cuando ejecuats echo Hello World?

## Quiz Answer

Hello World
