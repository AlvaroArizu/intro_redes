# Modulo 3 
- Modelo de capas
- Modelo de capas OSI
- Modelo de capas TCP/IP

# Modelo de Capas

Los modelos en capas se utilizan para visualizar la interacción entre diversos protocolos. Describen el funcionamiento de los protocolos en cada capa y su interacción con las capas superiores e inferiores, así como el flujo de información en la comunicación.

## Beneficios

- **Diseño de Protocolos:** Los protocolos en una capa específica tienen información definida para actuar y una interfaz definida para capas superiores e inferiores.
- **Competencia:** Productos de distintos proveedores pueden trabajar juntos.
- **Resistencia al Cambio:** Los cambios en una capa no afectan otras.
- **Lenguaje Común:** Describe funciones y capacidades de redes.

## Modelo de Protocolo

Describe la estructura de un conjunto de protocolos. Representa toda la funcionalidad requerida para elementos de una red de datos, tanto software como hardware. Ejemplo: modelo TCP/IP.

## Modelo de Referencia

Coherente con todos los servicios y protocolos de red. No especifica implementación ni proporciona detalles precisos de servicios y protocolos. Su objetivo es ayudar a comprender funciones y procesos.

Ejemplo: modelo OSI, utilizado en diseño de redes, especificaciones y resolución de problemas.

# Modelo de Capas OSI

El modelo OSI describe las etapas en un proceso de comunicación, pero no especifica cómo se realiza. Proporciona beneficios tales como:

- **Facilita la Comprensión:** Divide problemas complejos en partes más simples.
- **Evita Problemas de Compatibilidad:** Detalla las capas para un mejor aprendizaje.
- **Estándares para Interoperabilidad:** Proporciona un conjunto de estándares para una mayor compatibilidad e interoperabilidad.

## Capas del Modelo OSI

El modelo OSI se divide en 7 capas, organizadas en dos grupos:

### Capas de Host
- Aplicación
- Presentación
- Sesión
- Transporte

### Capas de Medio
- Red
- Enlace de Datos
- Física

### Nivel de Host vs Nivel de Red

Es esencial distinguir entre los niveles de host y red, ya que implican procesos diferentes.

### Capa 7: Aplicación

- Aplicaciones que utilizan servicios de red.
- Genera e interpreta mensajes.
- Ejemplos: correo electrónico, navegadores web, servidores, videojuegos, streaming.

### Capa 6: Presentación

- Representa la información para una comunicación reconocible.
- Ejemplo: protocolo SMTP para correos electrónicos.

### Capa 5: Sesión

- Establece, administra y finaliza conexiones entre aplicaciones locales y remotas.
- Cifra y comprime datos.

### Capa 4: Transporte

- Comunicaciones de extremo a extremo entre dispositivos.
- Control de flujo y errores.

### Capa 3: Red

- Direccionamiento lógico y dominio del enrutamiento.
- Encapsula segmentos en paquetes de datos.

### Capa 2: Enlace de Datos

- Proporciona direccionamiento físico y acceso a medios.
- Genera tramas para la transferencia de datos en una misma red física.

### Capa 1: Física

- Especificaciones eléctricas y físicas de los dispositivos.
- Define medios de transmisión: cables de cobre, fibra óptica, ondas de radio.

## Conclusión

El modelo OSI describe el proceso de comunicación en capas, permitiendo aislar problemas y resolverlos desde la capa física hasta la de aplicación.

# Modelo de capas TCP/IP

El modelo TCP/IP es un modelo de protocolo usado para comunicaciones en redes y, como todo protocolo, describe un conjunto de guías generales de operación para permitir que un equipo pueda comunicarse en una red. TCP/IP provee conectividad de extremo a extremo especificando cómo los datos deberían ser formateados, direccionados, transmitidos, enrutados y recibidos por el destinatario. Las redes de datos actuales se describen bajo el modelo de protocolo TCP/IP el cual está ampliamente difundido e implementado prácticamente en todas las infraestructuras de redes, tanto redes LAN como Internet.

## Introducción a Redes

El modelo TCP/IP describe el proceso de comunicación y los protocolos utilizados y a diferencia del modelo OSI, este posee 4 capas:

- La capa de aplicación del modelo TCP/IP es similar a las capas 5, 6, 7 combinadas del modelo OSI, esta capa reúne todo lo que tenga que ver con la generación y formateado del mensaje y cómo se comunican las aplicaciones entre sí.

- La capa de transporte de TCP/IP abarca las responsabilidades de la capa de transporte OSI e intervienen los protocolos TCP y UDP y algunas de las responsabilidades de la capa de sesión OSI.

- La capa de red o también llamada Internetworking utiliza los protocolos de enrutamiento IP.

- La capa de acceso a la red del modelo TCP/IP abarca el enlace de datos y las capas físicas del modelo OSI.

## Modelo OSI vs Modelo TCP/IP

| Modelo OSI     | Modelo TCP/IP          |
|----------------|------------------------|
| Capa de aplicación   | Capa de aplicación      |
| Capa de presentación |                        |
| Capa de sesión       |                        |
| Capa de transporte   | Capa de transporte      |
| Capa de red          | Capa de red            |
| Capa de enlace de datos | Capa de acceso de red |
| Capa física          |                        |

## Capa 4: Aplicación

Esta capa describe los protocolos utilizados por la mayor parte de las aplicaciones para proporcionar servicios de usuario o intercambiar datos de aplicaciones a través de las conexiones de red establecidas por los protocolos de las capas inferiores. Esto puede incluir servicios básicos de soporte de red, como protocolos de enrutamiento y configuración de host. Algunos ejemplos de esto son el protocolo HTTP o Protocolo de Transferencia de Hipertexto, el protocolo FTP o Protocolo de Transferencia de Archivos, el protocolo SMTP o protocolo de Transferencia de Correo y el Protocolo DHCP o Protocolo de Configuración Dinámica de Host. La capa de aplicación en el modelo TCP/IP corresponde a una combinación de la quinta (sesión), sexta (presentación) y séptima capa (aplicación) del modelo OSI.

## Capa 3: Transporte

Esta capa se alinea con la capa 4 del modelo OSI. En la capa de transporte se establecen canales de datos mediante puertos de red que es lo que hace posible el intercambio de datos. Además establece la conectividad de host a host en forma de servicios de transferencia de mensajes de extremo a extremo independientes de las redes subyacentes e independientes de la estructura de los datos del usuario y la logística del intercambio de información. Las conexiones entre hosts se basan en 2 tipos de protocolos: orientados a conexión bajo el protocolo TCP (Transfer Control Protocol) con control de errores y no orientado a la conexión bajo el protocolo UDP (User Datagram Protocol) sin control de errores. Los protocolos de esta capa pueden proporcionar control de errores, segmentación, control de flujo, control de congestión y direccionamiento de aplicaciones.

## Relación Cliente-Servidor

Las aplicaciones que envían o reciben información de la red de datos tienen roles:

- Cliente: un programa que se conecta y transfiere datos contra otra aplicación que puede estar en un host remoto o de forma local.
- Servidor: un programa que ofrece un servicio a la red y al que se conectan los clientes.

## Puertos de red

Los servicios reciben las solicitudes de los clientes, que básicamente son mensajes generados en la capa de aplicación, formateados bajo un protocolo en la misma capa y segmentados en la capa de transporte. Pero para que el servicio pueda recibirlos, estos segmentos tienen que ser entregados por un canal de transmisión específico. La capa de transporte establece el concepto de puerto de red. A través de estos puertos se recibirán las solicitudes y se procederá al intercambio de datos. Un puerto es una construcción lógica numerada que es asignada de forma específica para cada uno de los canales de comunicación que necesita un determinado servicio. Para muchos tipos de servicios, estos números de puerto se han estandarizado para que las computadoras cliente puedan abordar servicios específicos de una computadora servidor sin la participación de servicios de directorio o descubrimiento de servicios.

## Protocolo con control de transferencia TCP

TCP es un protocolo orientado a la conexión que aborda numerosos problemas de confiabilidad al proporcionar un flujo de bytes confiable. Los datos llegan ordenados, tienen la cantidad mínima de errores, no llegan duplicados, asegura que los paquetes lleguen a su destino y incluye control de congestión de tráfico. Cuando los mensajes pasan de la capa de aplicación a la de transporte, la cantidad de bytes que forman el mensaje se dividen en segmentos más pequeños. Esto sucede siempre en la capa de transporte, ya sea bajo el protocolo TCP o UDP.

## Cabecera o Header TCP

A cada segmento se le asigna una cabecera, un conjunto de bytes que precede el conjunto de bytes que contiene parte del mensaje. Esta cabecera contiene información relevante para garantizar la integridad del mensaje, los puertos de origen y puertos destino y estados de conexión, entre otros.

## Control de transferencia: número de secuencia y acuse recibo.

El mensaje se puede dividir en miles de segmentos, estos se envían de uno en uno y de forma secuencial. La cabecera incluye dos campos: Número de secuencia y Número de acuse recibo. El control de transferencia se logra con estos dos campos.

Existen muchos motivos por los que el emisor no recibe el acuse recibo:

- Exceso de tráfico en la red.
- El firewall del destino está bloqueando un puerto o protocolo de transporte.
- Los saltos de red exceden los tiempos de respuesta.

En los casos que no haya respuesta, el emisor seguirá enviando el mismo segmento hasta que pasen
unos segundos (Tiempo de espera) sin recibir una confirmación. Luego reenvía el paquete. Si continúa

## Orientado a conexión

TCP es un protocolo orientado a la conexión que aborda numerosos problemas de confiabilidad al proporcionar un flujo de bytes confiable. Entre el host que envía y el host que recibe hay una conexión estable y confiable donde se envían mutuamente segmentos: el host de origen envía segmentos que acarrean el mensaje y el host destino devuelve segmentos confirmando la recepción.

Básicamente bajo este protocolo se genera un canal de comunicación de puerto a puerto donde se intercambian datos, pero para lograr esto existen unos pasos previos en donde ambos hosts se reconocen mutuamente, se habilitan mutuamente para proceder al intercambio de datos y finalizan dicha conexión terminado el intercambio de datos y con ello la conexión.

Para esto, el segmento TCP tiene un conjunto de campos de 1 bit cada uno, también denominados ‘flags’, que determinan cada estado en el proceso de conexión.

## Saludo de 3 vías

El protocolo TCP es orientado a conexión y para lograr esa conexión antes de enviarse los segmentos que contienen el mensaje debe establecerse la conexión, y esto se logra mediante un mecanismo llamado “Saludo de 3 vías” o “3 way handshake”.
1. **Solicitud de conexión:** el emisor envía un segmento con el campo o flag ‘SYN’ activado.
2. **Aceptación de conexión:** el receptor recibe la solicitud y la aprueba devolviendo un segmento con el flag ‘ACK’ activado, y simultáneamente solicita conexión al emisor con el flag ‘SYN’ activado.
3. **El emisor responde:** al recibir la confirmación de conexión aprobada por el receptor, el emisor responde la solicitud de conexión del receptor con un segmento con el flag ‘ACK’ activado.
4. **Conexión establecida:** en este punto ambos hosts proceden al intercambio de datos. Cuando el intercambio finaliza se procede a la desconexión, un proceso similar al ‘SYN-ACK/SYN-ACK’ pero con el flag ‘FIN’.

## Protocolo de datagramas de usuario UDP

El Protocolo de datagramas de usuario (UDP) es un protocolo de datagramas no orientado a conexión. Al igual que IP, es un protocolo poco confiable. La confiabilidad se aborda mediante la detección de errores mediante un algoritmo de checksum. UDP se usa generalmente para aplicaciones como transmisión de medios (audio, video, voz sobre IP, etc.) donde la llegada a tiempo es más importante que la confiabilidad, o para aplicaciones simples de consulta / respuesta como búsquedas de DNS.

El Protocolo de transporte en tiempo real (RTP) es un protocolo de datagramas que se utiliza sobre UDP y está diseñado para datos en tiempo real, como medios de transmisión.

El protocolo UDP no utiliza mecanismos de conexión como el saludo de 3 vías. El objetivo es mantener el tiempo de transmisión lo más bajo posible.

## Características de UDP

- **UDP utiliza puertos:** al igual que el TCP, el protocolo UDP utiliza puertos para permitir que los datagramas se transfieran a los protocolos correctos, es decir, a las aplicaciones elegidas del sistema de destino. Los puertos quedan definidos mediante un número conforme a un rango de valores válidos, estando reservado el rango de 0 a 1023 para los servicios fijos.
- **Comunicación rápida y sin retardos:** el protocolo de transporte es adecuado para una transmisión de datos rápida debido a que no hay que llevar a cabo una configuración de la conexión. Esto resulta también del hecho de que la pérdida de un paquete individual afecta exclusivamente a la calidad de la transmisión. En el caso de conexiones TCP, en cambio, se intenta reenviar de nuevo los paquetes perdidos de forma automática, lo que provoca que todo el proceso de transmisión se detenga.
- **No ofrece garantía de seguridad e integridad de los datos:** la ausencia de acuse de recibo mutuo entre el emisor y el receptor garantiza que la velocidad de transmisión en el protocolo UDP sea excelente; no obstante, el protocolo no puede garantizar la seguridad ni la integridad de los datagramas. Tampoco puede garantizar el orden de los paquetes enviados. Por ello, los servicios que utilizan UDP deben aplicar sus propias medidas de corrección y protección.

## Aplicaciones del protocolo UDP

- **Aplicaciones basadas en best effort delivery:** el escenario típico en el que encontramos el protocolo UDP son las aplicaciones basadas en la entrega de mejor esfuerzo. A este tipo de programas, que utilizan el protocolo de datagramas de usuario como un mecanismo de mejor esfuerzo, les basta con una transmisión confiable de la información, porque la repiten constantemente de igual manera. Encontramos ejemplos en aquellas aplicaciones que transmiten valores medidos o que ejecutan repetidamente las mismas órdenes de trabajo.
- **Aplicaciones ligeras:** la baja sobrecarga del protocolo de transporte proporciona un soporte óptimo para las aplicaciones que tengan un diseño muy sencillo. Lo anterior, junto con el hecho de que no es necesario configurar una conexión, hacen que estas aplicaciones puedan beneficiarse de un rendimiento especialmente alto en el procesamiento y reenvío de datagramas en las redes.
- **Aplicaciones en tiempo real (real time applications):** el UDP también es adecuado como protocolo de transporte para servicios que presentan requisitos de comunicación en tiempo real, como las transmisiones de audio o vídeo. Se trata de protocolos que deben ser capaces de controlar en gran medida el propio flujo de datos en la comunicación, así como la comunicación de comando asociada para el control de los propios servicios.

En resumen, mientras que TCP garantiza la entrega de datos en el orden correcto y maneja la retransmisión de paquetes perdidos, UDP proporciona una comunicación rápida y simple, pero sin garantías de entrega. La elección entre TCP y UDP depende de las necesidades de la aplicación: si la confiabilidad y el orden de entrega son críticos, se utiliza TCP; si la velocidad es más importante y se pueden manejar errores o pérdidas de datos, se utiliza UDP.

