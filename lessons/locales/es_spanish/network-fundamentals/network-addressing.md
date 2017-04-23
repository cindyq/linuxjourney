# Network Addressing

## Lesson Content

Antes de ver como viaja un paquete a través de una red, debemos familiarizarnos con la terminología que usaremos. Cuando envias por correo una carta, debes de saber a quien se la mandas y de donde viene. Los paquetes necesitan la misma información. Nuestros hosts y los otros hosts se identifican usando direcciones MAC (media access control, control de acceso de medios) y direcciones IP. Para facilitarnos la vida, usamos hostnames para identificar a un host en vez de números.

<b>Direcciones MAC</b>

Una dirección MAC es un identificador único que se usa como dirección del hardware. Esta dirección nunca cambiará. Cuando quieres acceder a Internet, tu máquina necesita tener un dispositivo llamado tarjeta de interfaz de red. Este adaptador de red tiene su propia dirección de hardware que es usada para identificar tu máquina. Una dirección MAC para un dispositivo Ethernet es algo así 00:C4:B5:45:B2:43. Las direcciones MAC son asignadas a los adaptadores de red cuando estos son fabricados. Cada fabricante tiene un identificador único organizativo (OUI, organizationally unique identifier) para identificarse como fabricante, este OUI se denota por los tres primeros bytes de la dirección MAC. Por ejemplo, Dell es 00-14-22, por lo que un adaptador de red de Dell podría tener una dirección MAC tal que así: 00-14-22-34-B2-C2.

<b>Direcciones IP</b>

Una dirección IP se usa para identificar un dispositivo en una red. Dichas direcciones son independientes del hardware y pueden variar su sintaxis dependiendo de si esta usando IPv4 o IPv6 (lo veremos más adelante). Por ahora asumiremos que estás usando IPv4, por lo que una dirección IP típica es algo así: 10.24.12.4. Las direcciones IP son usadas con la parte software de la red, siempre que un sistema se conecta a Internet debe tener una dirección IP. Estas pueden cambiar si tu red cambia y son únicas en todo Internet (este no es siempre así una vez que aprendamos sobre NAT).

Recuerda que mover paquetes en las redes implica software y hardware, por lo que tenemos dos identicadores para cada equipo, MAC (hardware) e IP (software).

<b>Hostnames</b>

Una última forma de identificar tus máquinas es mediante el hostname. Este toma tu dirección IP y te permiten enlazar esa dirección a nombre legible. En vez de recordar 192.12.41.4 es más fácil recordar myhost.com.

## Exercise

No hay ejercicios para esta lección

## Quiz Question

¿Cuántos bytes hay en una dirección IPv4?

## Quiz Answer

4
