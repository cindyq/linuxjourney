# history

## Lesson Content

En tu shell, hay una historia de los comandos que ingresaste previamente; podes verlos todos. Esto es muy útil cuando querés encontrar un comando que ejecutaste anteriormente sin tener que tipearlo de nuevo.

<pre>$ history</pre>

Para "tipear" de nuevo el último comando, simplemente apretá la flecha para arriba.

Para ejecutar el comando previo, sin reescribirlo, usamos !!. Si tipeaste cat file1 y querés ejecutarlo de nuevo, podes usar !! y va a ejecutar el último comando que ejecutaste.

Otra atajo del history es ctrl-R que inicia la búsqueda reversa. Si apretas ctrl-R y tipeas partes del comando que querés encontrar va a mostrarte coindidencias que podes navegar apretando ctrl-R de nuevo. Cuando encuentres el comando que querés usar, apretá Enter.

¿La terminal se está llenando de cosas no? Vamos a limpiarla un poco, usando el comando clear para limpiar el display.

<pre>$ clear</pre>

¿Ahora se ve mejor no?

Mientras estamos hablando acerca de cosa útiles, una de las mas útiles funciones de cualquier sistema e interfaz de línea de comandos es auto-completar mediante la tecla tab. Si empezás a escribir un comando, archivo, carpeta, etc y apretás la tecla tab, va a autocompletar acorde a lo que encuentre en la carpeta que estás buscando siempre y cuando no encuentre algún otro archivo cuyo nombre empiece por esas letras. Por ejemplo, si querés ejecutar el comando chrome, podes escribir chr y apretar tab para que autocomplete chrome por vos.  

## Exercise

Navegá a través de los comandos previos en el history con las teclas arriba y abajo. Experimentá con la búsqueda reversa ctrl-R.

## Quiz Question

¿Cuál es el comando para limpiar la terminal?

## Quiz Answer

clear
