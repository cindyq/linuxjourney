# head

## Lesson Content

Digamos que tenemos un archivo muy largo, de hecho tenemos mucho donde elegir, por ejemplo ejecuta cat /var/log/syslog. Deberías ver páginas y páginas de texto. ¿Qué pasa si solo querías ver las primeras líneas de texto del archivo? Esto se puede hacer con el comando head, que por defecto te mostrará las 10 primeras líneas de un archivo.

<pre>$ head /var/log/syslog</pre>

Puedes modificar el número de líneas a tu antojo, digamos que quiero ver las primeras 15 líneas.

<pre>$ head -n 15 /var/log/syslog</pre>

La etiqueta -n se usa para designar el número de líneas.

## Exercise

¿Qué hace el siguiente comando y por qué?

<pre>$ head -c 15 /var/log/syslog</pre>

## Quiz Question

¿Qué etiqueta usarías para cambiar el número de líneas que quieres ver con el comando head?

## Quiz Answer

-n
