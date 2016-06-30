Network Layer

## Lesson Content

La capa de la red determina que ruta cojen los paquetes desde nuestro sistema a su destino. Para nuestro ejemplo los paquetes estan solo viajando en el mismo red pero el internet esta hecho de differente reds. Estos reds más pequeños que crean el internet son conocido como subnet. All subnets connect to each other in some way, which is why we are able to get to www.google.com even though it's on its own network. I won't go into detail as we have a whole course dedicated to subnets, but for now in regards to our Network layer, know that the IP addresses define the rules to travel to different subnets. 

In the network layer, it receives the segment coming from the transport layer and encapsulates this segment in an IP packet then attaches the IP address of the source host and the IP address of the destination host to the packet header. So at this point, our packet has information about where it is going and where it came from. Now it sends our packet to the physical hardware layer.

## Exercise

No exercises for this lesson.

## Quiz Question

What are smaller networks that make up the Internet called?

## Quiz Answer

subnets
