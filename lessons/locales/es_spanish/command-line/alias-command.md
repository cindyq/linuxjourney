# alias

## Lesson Content

A veces tipear comandos se vuelve repetitivo o es necesario reutilizar un comando largo; en esos caso es mejor tenerlo guardado bajo un alias. Para crear un alias, simplemente hay que especificar el nombre del alias y asignarlo al comando.

<pre>$ alias foobar='ls -la'</pre>

Ahora en lugar de tipear ls -la, directamente podes tipear foobar y se va a ejecutar ese comando, lo cual es muy bueno. Sin embargo este comando no va a guardar tu alias después de reiniciar; entonces vas a necesitar un alias permanente en:

<pre>~/.bashrc</pre>

o el archivo equivalente con tu perfil del shell para tenerlo disponible después de reiniciar.

Podes borrar alias con el comando unalias:

<pre>$ unalias foobar</pre>

## Exercise

Crear un par de alias y después borrarlos.

## Quiz Question

¿Qué comando se utiliza para crear un alias?

## Quiz Answer

alias
