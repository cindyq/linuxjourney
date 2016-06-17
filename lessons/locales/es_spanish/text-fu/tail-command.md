# tail

## Lesson Content

Parecido al comando head, el comando tail te permite ver por defecto las 10 últimas líneas de un archivo.

<pre>$ tail /var/log/syslog</pre>

Al igual que con el comando head, puedes cambiar el número de líneas que quieres ver.

<pre>$ tail -n 10 /var/log/syslog</pre>

Otra gran opción que puedes usar es la etiqueta -f (siguiente), que te permitirá seguir el archivo mientras crece. Inténtalo y ve lo que pasa.

<pre>$ tail -f /var/log/syslog</pre>

El archivo syslog está cambiando continuamente mientras interactuas con tu sistema y, usando tail -f, puedes ver todo lo que se esta añadiendo a dicho archivo.

## Exercise

Mira la página de ayuda de tail y lee acerca de otros comandos que no hemos mencionado.

<pre>$ man tail</pre>

## Quiz Question

¿Qué etiqueta se usa para seguir un archivo con tail?

## Quiz Answer

-f
