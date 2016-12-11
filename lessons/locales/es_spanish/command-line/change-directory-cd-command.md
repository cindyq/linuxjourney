# cd (Change Directory)

## Lesson Content

Ahora que sabes donde estas, veamos si podemos movernos alrededor del sistema un
poco. Recordá que vamos a necesitar usar paths para la navegación. Hay dos
formas diferentes de especificar un path, mediante rutas absolutas y relativas.

<ul>
<li>Path absoluto: Este es el camino desde la carpeta raíz. La raíz es la cabeza del sistema. La carpeta root o raíz es comúnmente simbolizada por un slash. Cada vez que la ruta comienza con / significa que empezamos desde la carpeta raíz. Por ejemplo, /home/pete/Desktop.</li>

<li>Path Relativo: Este es el camino desde donde estas ahora en el sistema. Si yo estaba en /home/pete/Documents y quería ir a una carpeta dentro de Documents llamada taxes, no tengo que especificar la ruta completa desde la raíz como /home/pete/Documents/taxes, puedo solamente ir a taxes/ en su lugar.</li>
</ul>

Ahora que sabes como funcionan los paths, solamente necesitamos algo que nos
ayude a ir hacia la carpeta que queremos. Por suerte, tenemos cd o "cambiar
directorio" para eso.

<pre>$ cd /home/pete/Pictures</pre> 

Entonces ahora cambié la carpeta de mi ubicación a /home/pete/Pictures.

En esta carpeta, tengo un directorio dentro llamado Hawaii; puedo ir allí
con:

<pre>$ cd Hawaii</pre>


¿Viste cópmo solo usé el nombre de la carpeta? Eso es porque ya estaba en /home/pete/Pictures.

Puede volverse agotador navegar las carpetas con paths absolutos y relativos
todo el tiempo; afortunadamente hay algunos atajos para ayudarte:

<ul>
<li>. (directorio actual). Esta es la carpeta en la que estas actualmente. </li>
<li>.. (directorio superior). Un nivel más arriba de la carpeta actual.</li>
<li>~ (directorio home). Este atajo te lleva a la carpeta "home". Por ejemplo, /home/pete.</li>
<li>- (directoryio previo. Este atajo te lleva al directorio en el que estabas previamente.</li>
</ul>

<pre>$ cd .
$ cd ..
$ cd ~
$ cd -
</pre>
Probalos!

## Exercise

<ol>
<li>Ejecutar el comando cd, sin ninguna opción, ¿dónde te lleva?</li>
</ol>

## Quiz Question

Si vos estas en /home/pete/Pictures y queres ir a /home/pete, ¿cuál es un buen atajo para usar?

## Quiz Answer

cd ..
