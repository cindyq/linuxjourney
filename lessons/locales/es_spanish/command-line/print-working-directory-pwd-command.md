# pwd (Print Working Directory)

## Lesson Content

En Linux todo es un archivo, mientras mas dentro de Linux nos metamos en este viaje mas vas a entender esto, pero por ahora solo tené la idea presente. 
Todos los archivos están organizados en un árbol de carpetas jerárquico. El primer directorio en el archivo de sistemas es llamado simplemente raíz (o root). El directorio root tiene varias carpetas y archivos dentro de las cuales podes guardar mas archivos o subcarpetas, etc. Acá hay un ejemplo de cómo se ve el árbol de carpetas:

<pre>/
|-- bin
|   |-- archivo1
|   |-- archivo2
|-- etc
|   |-- archivo3
|   `-- carpeta1
|       |-- archivo4
|       `-- archivo5
|-- home
|-- var
</pre>

Nos referimos a La ubicación de esos archivos y directorios como rutas (paths). Si tenés una carpeta llamada home con una carpeta adentro llamada pepe y otra llamada Películas dentro de esta última, ese path se va a ver así: /home/pepe/Películas, ¿simple no?

La navegación del sistema, similar a la vida real, te ayuda si sabes dónde estas y hacia dónde estas yendo. Para ver dónde estas, podes usar el comando pwd, el nombre de este comando es una sigla referida a "print working directory" (imprimi el directorio actual) y solo te muestra la carpeta en la que estas ubicado, contando siempre desde la carpeta root.

<pre>$ pwd</pre>

¿Dónde estás? ¿Dónde estoy? Probalo...

## Exercise

No hay ejercicios para esta lección.

## Quiz Question

¿Cómo encuentro en qué carpeta estoy ubicado ahora?

## Quiz Answer

pwd
