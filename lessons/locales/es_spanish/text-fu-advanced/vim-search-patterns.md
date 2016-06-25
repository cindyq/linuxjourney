# Vim Search Patterns

## Lesson Content

Para buscar una expresión solo teclea / y lo que quieras buscar mientras estas en una sesión de vim. Una vez que pulses Intro, puedes presionar "n" para ir hacia delante o "N" para ir hacia atrás en los resultados.

<pre>
My pretty file is very pretty.

/pretty

encontrará las palabras pretty en el archivo de texto.
</pre>

El comando ? buscará en el texto pero empezando por el final, por lo que el primer pretty del ejemplo anterior aparecerá primero.
<pre>
My pretty file is very pretty.

?pretty

encontrará las palabras pretty en el archivo de texto.
</pre>

## Exercise

Experimenta con los comandos de búsqueda, abre un archivo en vim con: vim [archivo de texto] y busca algo.

## Quiz Question

¿Qué tecla se usa para buscar en vim?

## Quiz Answer

/
