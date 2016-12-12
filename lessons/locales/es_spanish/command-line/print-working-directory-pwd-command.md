# pwd (Print Working Directory)

## Lesson Content

En Linux todo es un archivo, mientras mas dentro de Linux nos metamos en este viaje mas vas a entender esto, pero por ahora solo tené la idea presente. 
Todos los archivos están organizados en un árbol de carpetas jerárquico. El primer directorio en el archivo de sistemas es llamado simplemente raíz (o root). El directorio root tiene varias carpetas y archivos dentro de las cuales podes guardar mas archivos o subcarpetas, etc. Acá hay un ejemplo de cómo se ve el árbol de carpetas:

<pre>/
|-- bin
|   |-- file1
|   |-- file2
|-- etc
|   |-- file3
|   `-- directory1
|       |-- file4
|       `-- file5
|-- home
|-- var
</pre>

Nos referimos a La ubicación de esos archivos y directorios como rutas (paths). Si tenes una carpeta llamada home con una carpeta adentro llamada pete y otra llamada Movies dentro de esta última, ese path se va a ver así: /home/pete/Movies, ¿simple no?

La navegación del sistema, similar a la vida real, te ayuda si sabes dónde estas y hacia dónde estas yendo. Para ver dónde estas, podes usar el comando pwd, el nombre de este comando es una sigla referida a "print working directory" (imprimi el directorio actual) y solo te muestra la carpeta en la que estas ubciado, contando siempre desde la carpeta root.

<pre>$ pwd</pre>

¿Dónde estás? ¿Dónde estoy? Probalo...

## Exercise

Npo hay ejercicios para esta lección.

## Quiz Question

¿Cómo encuentro en qué carpeta estoy ubicado ahora?

## Quiz Answer

pwd
