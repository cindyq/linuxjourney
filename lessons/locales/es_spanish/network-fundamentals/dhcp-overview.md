# DHCP Overview

## Lesson Content

Un concepto importante sobre redes que todavía no hemos visto es DHCP (Dynamic Host Configuration Protocol, protocolo de configuración de host dinámico).

DHCP asigna direcciones IP, máscaras de subred y puertas de enlace a nuestras máquinas. Por ejemplo, digamos que tienes un teléfono móvil para hablar con la gente. Tienes que darte de alta con tu operador para que te asignen un número. Mientras pagues tus facturas, puedes seguir usando tu teléfono. DHCP es el operador telefónico en este caso, que te da una dirección IP para que puedas comunicarte con otras direcciones IP. Te prestan una dirección IP durante un tiempo determinado que puede ser renovada dependiendo de como configures tu sistema.

DHCP esta muy útil por distintos motivos. Permite al administrador de redes no preocuparse a la hora de asignar direcciones IP, previniendo también el que se configuren duplicados de estas. Cada red física debe tener su propia servidor DHCP al que cada host le pedirá una dirección IP. En una red doméstica típica, es el router el que actúa como servidor DHCP.

La manera en que DHCP obtiene toda la información de host dinámica es:

<ol>
<li>DHCP DISCOVER - Este mensaje es transmitido para buscar un servidor DHCP.</li>
<li>DHCP OFFER - El servidor DHCP en la red responde con un mensaje de ofrecimiento, que contiene un paquete con el tiempo de cesión, máscara de subred, dirección IP, etc.</li>
<li>DHCP REQUEST - El cliente envia otra transmisión para hacerles saber a todos los servidores DHCP que ofrecemiento ha aceptado.</li>
<li>DHCP ACK - El consentimiento es enviado por el servidor.</li>
</ol>

DHCP tiene más funciones, pero esto es lo fundamental.

## Exercise

No hay ejercicios para esta lección.

## Quiz Question

¿Cúales son los pasos en un requerimiento DHCP?

## Quiz Answer

DISCOVER, OFFER, REQUEST, ACK
