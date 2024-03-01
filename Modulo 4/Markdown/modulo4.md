# Modulo 4
- Estandar Ethernet
- Enrutamiento 

# Estándar Ethernet

Ethernet es un estándar de redes de área local para computadoras, por sus siglas en español Acceso Múltiple con Escucha de Portadora y Detección de Colisiones (CSMA/CD).

Según el modelo OSI, las capas se dividen de la siguiente manera:

- **Capa 3 Red:** direccionamiento lógico.
- **Capa 2 Enlace de datos:** direccionamiento físico (LLC y MAC).
- **Capa 1 Física:** señalización y transporte por un medio físico.

Los protocolos de capa Física y de Enlace de datos definen a Ethernet.

## Introducción a Redes

El estándar Ethernet se ocupa de las capas 1 y 2. Todos los dispositivos que se usan en redes LAN en la actualidad se recuestan en esta tecnología:

- Notebooks.
- Smartphones.
- Smart TVs.
- Impresoras.

Aunque fue concebido para redes de área local, la evolución de las tecnologías utilizadas ha permitido su implementación en redes de mayor envergadura como redes MAN y WAN.

El estándar Ethernet define las tecnologías usadas a nivel físico descritas en el modelo OSI.

## Formato de la trama Ethernet

Los paquetes de datos son encapsulados en una unidad de datos denominada ‘trama’ o ‘frame’. Esta trama está conformada por una cadena de bits y contiene varios campos:

- **Preámbulo**
- **Delimitador de inicio de trama**
- **MAC de destino**
- **MAC de origen**
- **802.1Q (opcional)**
- **Ethertype o longitud**
- **Payload**
- **Secuencia de comprobación (CRC)**
- **Gap entre frames**

## Funcionamiento

Ethernet opera a través de dos capas del modelo OSI:

- Capa 1: Se encarga de señales y streams de bits que se transportan en los medios.
- Capa 2: Controla el acceso al medio y la transmisión de tramas entre dispositivos.

## Dispositivos de red

El estándar Ethernet determina el formato de tramas, cómo esas tramas se vuelcan al medio, las tecnologías usadas y sus velocidades, y los dispositivos que transportan las tramas a las NICs, en definitiva, al dispositivo de usuario.

### Interfaz de RED

La Tarjeta de Interfaz de Red (NIC) permite que un dispositivo de usuario acceda a una red local. Cada tarjeta tiene una única dirección MAC que la identifica en la red.

Las interfaces además de poseer una MAC, a nivel de capa de Red del modelo OSI, también se identifican con una dirección IP.

### Repetidor

Un repetidor aumenta el alcance de una conexión física, recibiendo las señales y retransmitiéndolas, para evitar su degradación, a través del medio de transmisión, logrando así un alcance mayor. Opera en la capa física del modelo OSI.

### HUB

Un HUB funciona como un repetidor pero permite la interconexión de múltiples nodos. Recibe una trama de Ethernet por uno de sus puertos y la repite por todos sus puertos restantes sin ejecutar ningún proceso sobre las mismas. Opera en la capa física del modelo OSI.

### Puente de red

Un puente de red interconecta segmentos de red haciendo el cambio de frames entre las redes de acuerdo con una tabla de direcciones que le dice en qué segmento está ubicada una dirección MAC dada. Opera a nivel de capa 2 del modelo OSI.

### Switch o conmutador

Este dispositivo funciona como un puente, pero permite la interconexión de múltiples segmentos de red. Funciona en velocidades más rápidas y es más sofisticado. Básicamente opera en la capa 2 del modelo OSI, manejando información de las tramas y utilizando tablas de dirección.

# Enrutamiento

El enrutamiento es el proceso de reenviar paquetes entre redes, siempre buscando la mejor ruta (la más corta). Se lleva a cabo mediante dispositivos llamados 'router', que operan en el nivel de red del modelo OSI.

## Introducción a Redes

### Router

Un router establece la mejor ruta para que los paquetes de datos lleguen a su destino. Se utiliza ampliamente en redes domésticas y comerciales, proporcionando funciones adicionales como acceso inalámbrico, módem y conmutador.

### Funcionamiento

Los routers reciben paquetes de datos y los encaminan hacia su destino basándose en la información de origen y destino de los datagramas. Utilizan tablas de enrutamiento para determinar la ruta óptima.

### Salto de red (hop)

Los paquetes pasan por diferentes redes mientras viajan de la fuente al destino, lo que se conoce como salto de red. Un mayor número de saltos puede afectar el rendimiento.

### Recuento de saltos (hop count)

El recuento de saltos indica cuántos dispositivos de red intermedios atraviesa un paquete. Es una medida de la distancia entre los hosts.

### Métrica

Los protocolos de enrutamiento buscan la mejor ruta hacia la red de destino considerando varios parámetros, como la velocidad y la fiabilidad. Algunos protocolos utilizan el recuento de saltos como métrica.

### Next hop

Cuando un paquete tiene una red de destino diferente a la de origen, se envía a un dispositivo gateway, generalmente otro router. Este dispositivo determina la siguiente ruta para el paquete.

### Tabla de enrutamiento

La tabla de enrutamiento de un router contiene las redes a las que tiene acceso directo y la próxima puerta de enlace para llegar a ellas. También puede incluir una ruta por defecto.

### Trazado de ruta

El comando 'traceroute' se utiliza para determinar el número de saltos de un host a otro, útil para diagnosticar problemas de red.

### Estructura

La tabla de enrutamiento contiene información sobre la red de destino, la máscara, la interfaz de salida, la métrica y la puerta de enlace.

### Funcionamiento

Los routers determinan la mejor ruta para los paquetes utilizando información de enrutamiento estática o dinámica, intercambiada con otros routers.

# Topologías

Los enrutadores son fundamentales para dirigir los paquetes IP entre redes. En ausencia de una ruta, se produce un mensaje de error "destino inalcanzable", indicando que se ha excedido la cantidad de saltos o que ningún enrutador puede alcanzar la red de destino dentro de la red.

## Topología física

La topología física se refiere a la disposición física de los dispositivos de red, como routers, switches y hosts. Puede incluir redundancia, tolerancia a fallos y segmentación de red.

## Topología lógica

La topología lógica describe cómo los dispositivos de red se comunican entre sí a nivel lógico, es decir, cómo los paquetes de datos se mueven a través de la red.

### Gateway

El gateway, o puerta de enlace predeterminada, es esencial para enviar paquetes fuera de la red local. Si la dirección de destino del paquete está fuera de la red del host de origen, el paquete se envía al gateway.

### Network Address Translation (NAT)

La traducción de direcciones de red permite la comunicación entre redes con direcciones incompatibles. En una configuración de NAT, una red privada se conecta a otra red a través de un router que traduce las direcciones IP.

#### Tipos de NAT

- **NAT de cono completo:** Mapea la dirección IP y puerto interno a una dirección y puerto público diferentes, permitiendo la comunicación completa.
- **NAT de cono restringido:** Abre la IP y puerto externos solo cuando el host de la red privada quiere comunicarse con una dirección IP específica fuera de su red.
- **NAT de cono restringido de puertos:** Bloquea todo el tráfico a menos que el host de la red privada haya enviado previamente tráfico a una IP y puerto específico.
- **NAT Simétrica:** La traducción de dirección IP privada a dirección IP pública depende de la dirección IP de destino del tráfico.

# Reenvío de puertos (Port forwarding)

El reenvío de puertos, también conocido como "apertura de puertos" o "mapeo de puertos", permite que servicios específicos de una red privada sean accesibles desde redes externas.

## Funcionamiento

En una red NAT, los hosts dentro de la red privada son inaccesibles directamente desde el exterior. El reenvío de puertos consiste en redirigir los paquetes que llegan a un puerto específico y protocolo en la dirección IP pública del router hacia un host específico dentro de la red privada.

### Ejemplo:

- **Puerto del router:** 80 (HTTP)
- **Servicio:** Web App
- **Host destino:** 192.168.1.100
- **Puerto de escucha del host:** 8000
- **Protocolo:** TCP

## Puertos y protocolos

La apertura de puertos se configura considerando:

- Puertos de escucha en la red pública.
- Puertos de escucha de los hosts dentro de la red.
- Protocolos de transporte TCP/UDP.
- Rango de puertos.

Es importante destacar que el reenvío de puertos es de uno a uno, no es posible abrir un puerto que apunte a múltiples direcciones IP diferentes.









