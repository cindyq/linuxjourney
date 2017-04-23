# Application Layer

## Lesson Content

Digamos que quieres mandarle un email a Patty, vamos a ver cada una de las capas TCP/IP en acción.

Recordemos que esos paquetes son usados para transmitir datos a través de las redes. Un paquete consiste en una cabecera y un cuerpo. La cabecera contiene información sobre adonde va el paquete y de donde viene. El cuerpo son los datos que se transfieren. Como nuestro paquete viaja por la red, cada capa añade un poco de información a la cabecera del paquete. Ten en cuenta también que las distintas capas usan un termino distinto para nuestro "paquete", así en la capa de transporte esencialmente encapsulamos nuestros datos en un segmento y en la capa de enlace nos referimos a esto como frame, pero el término paquete se puede usar para hablar de la misma cosa.

Primero empezamos en la capa de aplicación. Cuando enviamos nuestro email mediante nuestro cliente de email, la capa de aplicación encapsulará estos datos. Dicha capa se comunica con la capa de transporte mediante un puerto específico a través del cual se envian los datos. Queremos enviar un email mediante el protocolo de la capa de aplicación SMTP (simple mail transfer protocol, protocolo de transferencia de correo simple). Los datos son mandados a través de dicho protocolo el cual abre una conexión con este puerto (puerto 25 es el que se usa para SMTP). Estos son enviados a la capa de transporte para que sean encapsulados en segmentos.

## Exercise

No hay ejercicios para esta lección.

## Quiz Question

¿Qué capa se usa para mostrar los datos del paquete en un formato amigable para el usuario?

## Quiz Answer

Aplicación
