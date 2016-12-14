# find

## Lesson Content

Con todos estos archivos que tenemos en el sistema se puede volver ajetreado encontrar alguno específico. Hay un comando que podemos usar para esta tarea,
find!

<pre>$ find /home -name cachorritos.jpg</pre>

Con find vas a tener que especificar la carpeta en la que vas a buscar, qué estas buscando y bajo qué criterio. En este caso, estamos intentando encontrar
un archivo con el nombre de cachorritos.jpg.

Podes especificar qué tipo de archivo estas intentando buscar.

<pre>$ find /home -type d -name MiCarpeta</pre>

En este último ejemplo, podes ver que estoy buscando bajo el tipo (d) para directorios y estoy usando el mismo criterio de búsqueda por el nombre MiCarpeta. Algo muy favorable para notar es que find no frena en la carpeta que estas buscando, sino que va a ir a ver dentro de cualquier subcarpeta que la carpeta principal contenga.

## Exercise

<ol>
<li>Encontrá un archivo desde la carpeta raíz que tenga la palabra net en el.</li>
</ol>

## Quiz Question

¿Qué opción hay que especificar para que find busque por nombre?

## Quiz Answer

-name
