# The Shell

## Lesson Content

¿El mundo es nuestra ostra, o realmente la shell es nuestra ostra?¿ Qué es la shell? La shell basicamente es un programa que coge nuestros comandos desde el teclado y se lo pasa al sistema operativo para ejecutarlos. Si alguna vez has usado una GUI (una ventana para el usuario), es probable que hayas visto un programa como una consola o un terminal, esos son los programas que ejecuta un shell para ti. A lo largo de este curso completo, aprenderemos todas las maravillas del shell.

En este curso usaremos el shell bash (shell Bourne Again), casi todas las distribuciones Linux usar por defecto la bash shell. Hay otras shells disponibles como KSH, ZSH, TSCH pero en este curso no usaremos ninguno de ellos.

¡Vamos a ello! Dependiendo de la distribución sus comandos pueden tener pequeñas variaciones, pero lo normal es que es que cumpla con el siguiente formato:
<pre>username@hostname:current_directory
pete@icebox:/home/pete $</pre>

¿Ves el $ al final del comando? Cada shell tendrá diferentes comandos, en nuestro caso el $ para un usuario normal que utiliza Bash, Bourne o Korn shell, no se agrega el símbolo de indicador de comando cuando se escribe el comando, solo tienes que saber que está ahí.

Vamos a empezar con un comando sencillo, echo. El comando echo imprime un argumento de texto en la pantalla.

<pre>$ echo Hello World</pre>

## Exercise

Prueba con alguno de estos otros comando y mira a ver qué muestran:

<ol>
<li>$ date</li>
<li>$ whoami</li>
</ol>

## Quiz Question
¿Qué debería de mostrar por pantalla si escribes el comando: echo Hello World?

## Quiz Answer

Hello World