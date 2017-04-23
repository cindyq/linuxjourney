# TCP/IP Model

## Lesson Content

El modelo OSI dio origen al que eventualmente se convirtió en el modelo TCP/IP. Este último es en el que se se basa Internet. Es la implementación actual de red. El modelo TCP/IP usa la interfaz del protocolo TCP/IP, al que nos referimos comunmente como TCP/IP. Estos protocolos trabajan juntos especificando como deben ser apilados los datos, direccionados, transmitidos y enrutados a través de una red. Mediante el modelo TCP/IP, podemos ver como estos protocolos son usados para mostrar los detalles de como un paquete viaja a través de la red.

<b>Capa de aplicación</b>

Es la primera capa del modelo TCP/IP. Determina como los programas de tu computador (tales como tu navegador web) interaccionan con los servicios de la capa de transporte para ver que datos son enviados o recibidos.

Esta capa usa:
<ul>
<li>HTTP (Hypertext Transfer Protocol, protocolo de transferencia de hipertexto) - usado por las páginas web en Internet.</li>
<li>SMTP (Simple Mail Transfer Protocol, protocolo de transferecia de correo simple) - transmisión de correo electrónico (email) </li>
</ul>

<b>Capa de transporte</b>

Como serán transmitidos los datos, incluyendo la comprobación de los puertos correctos, la integridad de los datos y básicamente la entrega de nuestros paquetes.

Esta capa usa:
<ul>
<li>TCP (Transmission Control Protocol, protocolo de control de transmisión) - entrega fiable de datos</li>
<li>UDP (User Datagram Protocol, protocolo de datagrama de usuario) - entrega no fiable de datos</li>
</ul>

<b>Capa de red</b>

Esta capa especifica como mover paquetes entre hosts y entre redes.

Esta capa usa:
<ul>
<li>IP (Internet Protocol, protocolo de internet) - Ayuda a enrutar paquetes desde una máquina hasta otra.</li>
<li>ICMP (Internet Control Message Protocol, protocolo de mensaje de control de Internet) - Ayuda a decirnos que es lo que está pasando, por ejemplo mediante mensajes de error e información para debuguear.</li>
</ul>

<b>Capa de enlace</b>

Esta capa especifica como enviar datos a través de un hardware específico, tales como el envio de datos a través de Ethernet, fibra, etc.

Los protocolos que usa cada capa de las listadas arriba no son extensivos y te encontrarás muchos otros protocolos que también intervienen.

En las lecciones siguientes, ahondaremos en cada una de estas capas y discutiremos como nuestros paquetes viajan a través de la red a ojos del modelo TCP/IP (hay muchas perspectivas acerca de como un paquete viaja por la red, pero no hablaremos de ellas, aunque hay que ser conscientes de su existencia).

## Exercise

No hay ejercicioes para esta lección.

## Quiz Question

¿Cuál es la primera capa del modelo TCP/IP?

## Quiz Answer

Aplicación
