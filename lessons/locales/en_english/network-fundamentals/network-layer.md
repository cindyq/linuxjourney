# Network Layer

## Lesson Content

La capa de red determina la ruta de nuestros paquetes desde nuestro host hacia el host de destino. Por suerte en nuestro ejemplo, nuestro paquete solo viaja por la misma red, pero Internet está formado por muchas redes. Estas redes más pequeñas que componen Internet son conocidas como subredes. Todas las subredes se conectan entre sí de algún modo, motivo por el cual podemos conectarnos a www.google.com incluso estando este en su propia red. No entraré en los detalles ya que hay un curso entero dedicado a las subredes, pero por ahora, con respecto a nuestra capa de de red, saber que las direciones IP definen las reglas para acceder a las distintas subredes.

En la capa de red, se recibe el segmento que viene de la capa de transporte, encapsulándose este en un paquete IP para ser adjuntado a la dirección IP del host principal y la dirección IP del host de destino a la cabecera del paquete. Por lo que en este punto, nuestro paquete tiene información sobre a donde va y de donde viene. Ahora nuestro paquete puede enviarse a la capa del hardware. 


## Exercise

No hay ejercicios para esta lección.

## Quiz Question

¿Cómo se llaman las redes más pequeñas que componen Internet?

## Quiz Answer

subredes
