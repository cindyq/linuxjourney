# cd (Change Directory)

## Lesson Content

Ahora que ya sabes donde estas intentemos movernos un poco por el sistema de archivos. Recuerda que debemos usar rutas para navegar. Existen dos formas de especificar rutas: las absolutas y las relativas.

<ul>
<li>Ruta absoluta: Esta es la ruta que parte del directorio raíz. La raíz es la que manda. El directorio raíz es comúnmente representado por una barra oblicua. Si la ruta comienza con / significa que empieza desde el directorio raíz. Por ejemplo, /home/pete/Escritorio.</li>

<li>Ruta relativa: Esta es la ruta que parte desde tu ubicación actual en el sistema de archivos. Si mi ubicación fuera /home/pete/Documentos y quisiera moverme a una carpeta llamada impuestos ubicada dentro de Documentos, no es necesario que especifique la ruta completa desde la raíz escribiendo /home/pete/Documentos/impuestos, puedo ir directamente a impuestos/ para abreviar.</li>
</ul>

Ahora que ya sabes como funcionan las rutas, necesitamos una herramienta que nos permita cambiar al directorio que deseamos. Por suerte cd o "change directory" (cambia de directorio) hace precisamente eso.

<pre>$ cd /home/pete/Imágenes</pre>

Así cambié mi ubicación a /home/pete/Imágenes.

Dentro de este directorio tengo una carpeta que se llama Hawaii, puedo entrar en ella escribiendo:

<pre>$ cd Hawaii</pre>

¿Te diste cuente que use solamente el nombre del directorio? Es porque ya estaba ubicado en /home/pete/Imágenes.

Puede resultar agotador navegar únicamente con rutas absolutas y relativas, por suerte existen algunas abreviaciones que nos darán una mano.

<ul>
<li>. (directorio actual). Un punto significa el directorio donde estás ubicado.</li>
<li>.. (directorio superior). Dos puntos te llevan al directorio que esta justo por encima del actual.</li>
<li>~ (directorio home). La virgulilla te lleva a tu directorio de usuario, por ejemplo /home/pete.</li>
<li>- (directorio anterior). El símbolo de guión te lleva al directorio donde estuviste justo antes de llegar al actual.</li>
</ul>

<pre>$ cd .
$ cd ..
$ cd ~
$ cd -
</pre>
Pruébalos!

## Exercise 

<ol>
<li>Ejecuta el comando cd sin ningún parámetro, ¿a donde te lleva?</li>
</ol>

## Quiz Question

Si estas en /home/pete/Imágenes y quieres llegar a /home/pete, ¿que atajo sería mejor usar?

## Quiz Answer

cd ..

