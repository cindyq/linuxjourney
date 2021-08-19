# pwd (Print Working Directory)

# Lesson Content

En linux todo es un archivo, comprenderás mejor esto a medida que nos adentremos mas en el mismo, pero por ahora solo recuerdalo. Cada archivo esta organizado en un árbol de directorios jerárquico. El nombre del primer directorio del sistema de archivos es "root" (raíz). El directorio raíz contiene varias carpetas y archivos donde puedes almacenar más carpetas y archivos y así sucesivamente. He aquí un ejemplo de como se veria un árbol de directorios:

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

A la ubicación de estos archivos y directorios se les llama "paths" (caminos). Si hubiera una carpeta llamada home con una carpeta adentro llamada pete que a su vez contenga una carpeta llamada Películas, el path se vería así: /home/pete/Películas, bastante simple ¿no es verdad?

Al navegar el sistema de archivos, como en la vida real, hay que saber cual la ubicación actual y a donde queremos llegar. Para saber donde nos encontramos podemos usar el comando pwd, este comando significa "print working directory" (imprimir directorio actual) y te indica en que directorio estás. Nótese que el path debe comenzar en el directorio raiz.

<pre>$ pwd</pre>

¿A donde te estás? ¿A donde estoy? Ahora inténtalo.

## Exercise

No hay ejercicios para esta lección.

## Quiz Question

¿Como averiguo en que directorio me encuentro?

## Quiz Answer

pwd
