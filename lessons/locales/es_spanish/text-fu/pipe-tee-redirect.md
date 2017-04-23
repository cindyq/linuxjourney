# pipe y tee

## Lesson Content

Intentemos algo de fontanería ahora, bueno no exactamente. Ejecuta este comando:

<pre>$ ls -la /etc</pre>

Deberías ver una lista muy larga de cosas, bastante díficil de leer por cierto. En vez de redigir la salida a un archivo, ¿no estaría bien si pudiésemos ver la salida con otro comando como less? Bien, podemos hacerlo.

<pre>$ ls -la /etc | less </pre>

El operador pipe |, representado por una barra vertical, nos permite obtener la salida standard de un comando y hacerla entrada standard para otro proceso. En este caso, tomamos la salida standard de ls -la /etc y luego la <i>reconducimos</i> hacia el comando less. El comando pipe es muy útil y lo usaremos muchísimas veces.

Pero, ¿qué pasa si queremos escribir la salida de un comando por dos canales diferentes? Esto es posible con el comando tee:

<pre>$ ls | tee peanuts.txt</pre>

Deberías ver la salida de ls en tu pantalla y si abres el archivo peanuts.txt, deberías ver la misma información.

## Exercise

Intenta ejecutar los siguientes comandos:
<pre>$ ls | tee peanuts.txt banan.txt</pre>

## Quiz Question

¿Qué tecla representa el operador pipe?

## Quiz Answer

|
