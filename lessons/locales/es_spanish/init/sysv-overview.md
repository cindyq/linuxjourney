# System V Overview

## Lesson Content

El propósito principal de init es iniciar y detener procesos esenciales del sistema. Existen tres grandes implementaciones de init en Linux: System V, Upstart y systemd. En esta lección, veremos la versión mas tradicional de init: System V init o Sys V (pronunciado como 'System Five')

Para saber si estás utilizando la implementación de init Sys V, verifica que tienes el fichero /etc/inittab. 

Sys V inicia y detiene procesos en forma secuencial, por lo que si quieres iniciar un servicio llamado foo-b, antes de que foo-b pueda funcionar, tienes que asegurarte de que foo-a ya se encuentra corriendo. Sys V hace esto con scripts, los cuales inician y detienen servicios por nosotros, podemos escribir nuestros propios scripts o usar los que ya vienen implementados en el sistema operativo y que son usados para cargar servicios esenciales. 

Las ventajas de utilizar esta implementación de init, es que es relativamente fácil resolver dependencias, ya que sabes que foo-a viene antes de foo-b, sin embargo la performance no es muy buena ya que generalmente una cosa es iniciada o detenida a la vez.

Cuando usas Sys V, el estado de la máquina es definido por una serie de niveles de ejecución que van del 0 al 6. Estos diferentes modos van a variar dependiendo de la distribución, pero la mayoría de las veces se verán de la siguiente manera:

<ul>
<li>0: Apagado</li>
<li>1: Modo monousuario</li>
<li>2: Modo multiusuario sin soporte de red</li>
<li>3: Modo multiusuario con soporte de red</li>
<li>4: No usado</li>
<li>5: Modo multiusuario con soporte de red e interfaz gráfica</li>
<li>6: Reiniciado</li>
</ul>

Cuando tu sistema inicia, busca en que nivel de ejecución estás y ejecuta los scripts localizados dentro la configuración de dicho nivel de ejecución. Los scripts se encuentran en <b>/etc/rc.d/rc[número del nivel de ejecución].d/</b> o <b>/etc/init.d</b>. Los scripts que empiezan con S (start) o K (kill) correrán en el inicio y el apagado respectivamente. El número que precede a esos caracteres determina la secuencia en la que se ejecutarán.

Por ejemplo:

<pre>
pete@icebox:/etc/rc.d/rc0.d$ ls
K10updates  K80openvpn
</pre>

Vemos que cuando cambiamos al nivel de ejecución 0 o modo apagado, nuestro equipo correrá primero el script para matar los servicios de actualización y luego openvpn. Para saber o modificar el nivel de ejecución por defecto con el que nuestro sistema bootea, puedes mirar el fichero /etc/inittab.

Para tener en cuenta, System V esta siendo reemplazado lentamente aunque quizás no ocurra hoy ni en unos años. Sin embargo, es posible que veas niveles de ejecución en otras implementaciones de init, principalmente para dar soporte a aquellos servicios que solamente son iniciados o detenidos utilizando System V init scripts. 

## Exercise

Si estás corriendo System V, cambia el nivel de ejecución por defecto de tu máquina a otra cosa y ve que sucede.

## Quiz Question

Qué nivel de ejecución es usado generalmente para apagar el sistema?

## Quiz Answer

0
