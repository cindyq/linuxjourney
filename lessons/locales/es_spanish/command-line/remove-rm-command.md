# rm (Remove)

## Lesson Content

Creo que tenemos muchos archivos, borremos algunos. Para borrar archivos podes usar el comando rm. El comando rm (de remover) se usa para borrar tanto archivos como carpetas.

<pre>$ rm archivo1</pre>

Precaución con rm, no hay un basurero mágico del cual pescar archivos borrados. Una vez que se fueron, se fueron para siempre, así que tené cuidado.

Afortunadamente hay algunas medidas de seguridad puestas de tal forma que nadie pueda remover muchos archivos importantes. Archivos protegidos contra escritura van a pedirte una confirmación antes de ser borrados. Si una carpeta está protegida contra escritura no va ser borrada fácilmente.

Ahora si no te importa nada de eso, absolutamente podes borrar muchos archivos.

<pre>$ rm -f archivo1</pre>

-f o la opción "forzar" le dice a rm que borre todos los archivos, con o sin protección de escritura, sin preguntarle al usuario (siempre y cuando tengas el permiso apropiado).

<pre>$ rm -i file</pre>

Agregando la opción -i como en otros comandos, va a preguntarte si de hecho querés borrar ese archivo o carpeta.

<pre>$ rm -r carpeta</pre>

No podes rm una carpeta por defecto, vas a tener que agregar la opción -r (recursivo) para borrar todos los archivos y subcarpetas que haya.

Podes borrar una carpeta con el comando rmdir.

<pre>$ rmdir directory</pre>

## Exercise

<ol>
<li>Creá un archivo llamado -file (no te olvides el guión del medio!.</li>
<li>Borrá ese archivo.</li>
</ol>

## Quiz Question

¿Cómo eliminas un archivo que se llama miArchivo?

## Quiz Answer

rm miArchivo


