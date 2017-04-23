# Link Layer

## Lesson Content

Al final del modelo TCP/IP se encuentra la capa de enlace, esta capa es la capa específica del hardware.

En la capa de enlace, nuestro paquete es encapsulado una vez más en algo llamado frame, la cabecera del frame contiene las direcciones MAC de la fuente y del destino de nuestros hosts, las sumas de verificación y los separadores de paquetes para que el recibidor pueda saber cuando termina un paquete.

Por suerte estamos en la misma red, por lo que nuestro paquete no tendrá que viajar muy lejos. Primero, la capa de enlace adjunta la dirección MAC de origen a la cabecera del frame, pero necesita saber también la dirección MAC de Patty, ¿cómo la sabe y cómo la busco si no está en Internet? Para ello usamos ARP.

<b>ARP (Address Resolution Protocol, protocolo de resolución de direcciones)</b>

ARP encuentra la dirección MAC asociada con una dirección IP. ARP se usa dentro de la misma red, pero si Patty no esta en la misma red, usaríamos un sistema de enrutamiento para determinar el siguiente router que recibiría el paquete y una vez estemos en la misma red, podríamos usar ARP.

Una vez estemos en la misma red, los sistemas usan en primer lugar las tablas de búsqueda ARP que guardan información sobre qué direcciones IP están asociadas con qué direcciones MAC. Si el valor no está allí, se usa ARP. Luego el sistema transmitirá un mensaje a la red usando el protocolo ARP para averiguar que host tiene la IP 10.10.1.4. Dicho mensaje transmitido es un mensaje especial que se envía a todos los hosts de una red (acertadamente llamado para enviar una transimisión), cualquier máquina con la dirección IP requerida contestará con un paquete ARP que contiene la dirección IP y la dirección MAC.

Ahora que tenemos todos los datos que necesitamos, las direcciones IP y MAC, nuestra capa de enlace deja pasar este frame a través de nuestra tarjeta de red al siguiente dispositivo para encontrar la red de Patty. Este paso es un poco más complejo de lo que he explicado, pero ahondaremos un poco más cuando hablemos de la etapa de enrutamiento.

Y hay va otro simple (o no tan simple) paquete recorriendo la capa TCP/IP. Ten en cuenta que los paquetes no viajan en un solo sentido. Todavía no hemos llegado a la red de Patty. Cuando los paquetes viajan por las redes, estos deben hacer lo descrito en el modelo TCP/IP al menos dos veces antes de ser enviados o recibidos. De hecho, en realidad la manera en que viaja un paquete es algo así como esto:

<b>Recorrido del paquete</b>

<ol>
<li>Pete envia a Patty un email: los datos llegan a la capa de transporte.</li>
<li>La capa de transporte encapsula los datos en una cabecera TCP o UDP para formar un segmento, el segmento adjunta el puerto TPC o UDP de destino y fuente, para entonces ser enviado a la capa de red.</li>
<li>La capa de red encapsula el segmento TCP en un paquete IP, que adjunta la dirección IP de destino y de la fuente. Luego enruta el paquete a la capa de enlace.</li>
<li>El paquete llega al hardware físico de Pete y se encapsula en un frame. Las direcciones MAC de la fuente y del destino se añaden a dicho frame.</li>
<li>Patty recibe este frame de datos mediante su capa física y comprueba la integridad de los datos de cada frame, luego desencapsula el contenido de este y envia el paquete IP a la capa de red.</li>
<li>La capa de red lee el paquete para encontrar la IP de la fuente y la del destino que fueron añadidas. Comprueba si esta IP es la misma que la IP de destino, confirmándolo. Desencapsula el paquete y envia el segmento a la capa de transporte.</li>
<li>La capa de transporte desencapsula los segmentos, comprueba los puertos TCP y UDP y hace una conexión con la capa de aplicación basada en dichos puertos.</li>
<li>La capa de aplicación recibe los datos de la capa de transporte en el puerto que fue especificado y lo presenta a Patty como el mensaje de email original.</li>
</ol>

## Exercise

No hay ejercicios para esta lección.

## Quiz Question

¿Qué se usa para encontrar la dirección MAC en la propia red?

## Quiz Answer

ARP
