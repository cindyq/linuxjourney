# Transport Layer

## Lesson Content

La capa de transporte nos ayuda a transferir nuestros datos para que las redes puedan leerlos. Fracciona nuestros datos en paquetes que serán transportados y recompuestos en orden. Estos paquetes son conocidos como segmentos los cuales facilitan el transporte de nuestros datos en las redes.

<b>Puertos</b>

Incluso sabiendo donde estamos enviando nuestros datos via direcciones IP, estas no son lo suficientemente específicas si queremos enviar nuestros datos a ciertos procesos o servicios. Servicios como el HTTP usan un canal de comunicación via puertos. Por lo que si queremos enviar datos de páginas web, necesitamos enviarlos al puerto HTTP (puerto 80). Así, además de los anteriores segmentos, la capa de transporte también adjuntará los puertos de origen y destino al segmento, para que cuando el recibidor obtenga el paquete final sepa que puerto usar.

<b>UDP</b>

Hay dos protocolos de transporte populares, UDP y TCP. Discutiremos brevemente sobre el UDP y lo haremos profundamente sobre el TCP, ya que es el más usado.

UDP no es un método de transporte de datos en el que se pueda confiar. De hecho no le importa si obtienes todos tus datos originales. Esto puede parecer terrible, pero tiene sus usos, tales como el streaming de contenidos ya que ahí no importa si pierdes algunos frames si se gana un poco de velocidad.

<b>TCP</b>
TCP proporciona un flujo de datos de confianza orientado a la conexión. TCP usa puertos para enviar datos desde y hacia hosts. Una aplicación abre una conexión desde un puerto en su host hasta otro puerto en un host remoto. Para establecer la conexión, usamos la conexión TCP.

<ul>
<li>El cliente (proceso de conexión) envia un segmento SYN al servidor demandando una conexión</li>
<li>El servidor envia al cliente un segmento SYN-ACK permitiendo el acceso a la conexión del cliente</li>
<li>El cliente envia un ACK al servidor reconociendo el acceso a la conexión del servidor</li>
</ul>

Una vez que esta conexión está establecida, se pueden intercambiar datos mediante una conexión TCP. Los datos son enviados en distintos segmentos y son seguidos mediante números de secuencia TCP para que sean organizados en el orden correcto cuando son enviados. En nuestro ejemplo del email, la capa de transporte adjunta el puerto de destino (25) y también el puerto de origen desde el que vino.

## Exercise

No hay ejercicios para esta lección.

## Quiz Question

¿Cuál es un protocolo de transporte confiable?

## Quiz Answer

TCP
