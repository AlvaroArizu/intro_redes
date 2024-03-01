# Modulo 2
- Dirreccion IP
- Mascara de red
- ID del Host
- Segmentacion

# Dirección IP

Una dirección IP es una etiqueta numérica que identifica de manera lógica y jerárquica una interfaz en la red de un dispositivo que utiliza el protocolo Internet Protocol (IP).

## Estructura de una Dirección IP

Una dirección IP se compone de cuatro octetos separados por puntos, donde cada octeto está formado por 8 bits. Los valores de los octetos van desde 0 hasta 255, lo que se puede representar en sistema binario.

### Conversión de Binario a Decimal

La conversión de binario a decimal se realiza multiplicando el valor de cada bit por la base numérica (2) elevada a una potencia, y luego sumando los valores resultantes. Por ejemplo:

- Binario: 101
- Decimal: (1 * 2^2) + (0 * 2^1) + (1 * 2^0) = 5

## Representación Binaria y Decimal

Para representar una dirección IP en binario y decimal, se desglosa cada octeto en su forma binaria y se calcula su valor decimal correspondiente.

Ejemplo:
| Octeto | Valor Binario | Valor Decimal |
|--------|---------------|---------------|
|   192  |   11000000    |      192      |
|   168  |   10101000    |      168      |
|    0   |   00000000    |       0       |
|    1   |   00000001    |       1       |


La dirección IP 192.168.0.1 se representa en binario como 11000000.10101000.00000000.00000001 y en decimal como 192.168.0.1.

## Conclusión

Las direcciones IP se expresan como números de notación decimal, donde cada octeto se divide en 8 bits y se representa en sistema binario. Cada octeto puede tomar valores de 0 a 255, lo que permite un rango de direcciones posibles desde 0.0.0.0 hasta 255.255.255.255.

# Máscara de red

Las direcciones IP además de identificar un dispositivo de red contienen otro tipo de información, que es la red o subred de pertenencia.

## Redes lógicas

Como se desarrolló anteriormente, las redes se estructuran a nivel físico y a nivel lógico:

- A nivel físico los hosts se organizan en segmentos de red, de forma jerárquica, en malla o estrella.
- A nivel lógico los hosts se agrupan en lo que se denomina ‘red lógica’. Una porción de la dirección IP representa la red lógica, mientras que la porción restante representa una ID de red única para cada host dentro de la red.

## Introducción a Redes

Pongamos el siguiente ejemplo:

`192.168.1.5 10.20.30.5`


Hay dos hosts cuyas direcciones IP son 192.168.1.5 y 192.168.1.66, ambas tienen algo en común, sus primeros 3 octetos son iguales y lo mismo pasa con los otros dos hosts. Esto nos da la idea que los hosts se agrupan de alguna forma, esos grupos son las redes lógicas, una red es la 192.168.1.xxx y la otra es la 10.20.30.xxx.

## Máscara de red

Las direcciones IP están formadas por 4 octetos de 8 bits cada uno, en total 32 bits. Una cantidad de estos bits representan la red, mientras que el resto representan las ID para asignar a los hosts, y en este punto es donde entra el concepto de máscara de red. Cuando se configura un host se le deben indicar estos dos datos, IP y Máscara:

- IP:192.168.1.100
- MÁSCARA:255.255.255.0

La máscara de red es la cantidad de bits que podemos utilizar de los 32 de una dirección IP para crear una red.

Máscara 255.255.255.0

- Máscara dec.: 255.255.255.0
- Máscara bin.: 11111111.11111111.11111111.00000000

Todos los bits en 1 están reservados para formar redes, los bits en 0 están reservados para asignar ID de hosts.

Con una máscara 255.255.255.0 puedo usar los números del 0 al 255 para crear una red con los bits asignados a red.

Red decimal: 192.168.1.0
Red binario: 11000000.11000000.00000001.00000000

# ID de host

Las direcciones IP junto con la máscara de red expresan dos datos fundamentales:

- Red lógica.
- ID de host dentro de esa red lógica.

Pasemos a la siguiente slide para ver un ejemplo.

## Introducción a Redes

`192.168.1.5/24 192.168.1.102/24`


Estamos en presencia de un segmento de red a nivel físico, todos los hosts pueden conectarse entre sí, y dos segmentos de red a nivel lógico: hay dos redes que utilizan la máscara 255.255.255.0 en combinaciones distintas: RED 192.168.1.0/24 y RED 192.168.3.0/24.

`192.168.3.18/24 192.168.3.22/24`


Cabe mencionar que la imagen presenta 2 tipos de topologías, una física y otra lógica de una manera poco convencional. La imagen es solo ilustrativa y tiene el fin de mostrar y diferenciar 3 aspectos: una red física y dos redes lógicas.

### IDs utilizables para hosts

La máscara de red nos indica qué porción de la dirección es para la red y qué porción para asignar a host, por lo tanto saber la máscara nos permite saber cuántos hosts pueden caber en una red lógica, aunque no todas las direcciones que permite la máscara se pueden asignar a hosts. Hay dos direcciones que están reservadas, la primera y la última.

Para la dirección IP 192.168.1.5/24 podemos conocer:

| Máscara       | ID de red     | Primer IP host | Última IP de host | Broadcast      |
|---------------|---------------|----------------|-------------------|----------------|
| 255.255.255.0| 192.168.1.0   | 192.168.1      | 192.168.1.254     | 192.168.1.255  |

Con la máscara sabemos que los primeros 3 octetos corresponden a la red, el último puede ser cualquier valor para asignar a los hosts pertenecientes a la red, pero hay dos que no se pueden utilizar, la primera que es la 192.168.1.0 y la última que es la dirección 192.168.1.255 quedando el intervalo 192.168.1.1-192.168.1.254 para repartir entre los hosts.

### ID de red y Broadcast

La ID de red es la primera dirección en una red y, como dice su nombre, identifica la red, en ese punto ésta comienza.

La dirección de broadcast es la última de la red y es una dirección que comparten todos los hosts de la red. La comunicación por broadcast es la topología lógica que se usa actualmente, quedando atrás la comunicación por tokens que era la topología lógica utilizada antiguamente. Los avances tecnológicos en materia de dispositivos de red y medios físicos permitieron incorporar mejoras, mayores velocidades y estabilidad gracias a esta forma de comunicación.

Considerando que estas direcciones son reservadas, el cálculo de hosts posibles por red es: El valor decimal de los bits asignados a hosts menos dos.

La red 192.168.1.0/24:

8 bits asignados a ID de hosts = 2^8 - 2 = 254 hosts

La red 10.10.0.0/16:

16 bits asignados a ID de hosts = ( 2^8 x 2^8 ) - 2 = 2^16 - 2 = 65534

### Algunos ejemplos de redes con distintas máscaras:

| Máscara       | ID de red     | Primer IP host | Última IP de host | Broadcast      |
|---------------|---------------|----------------|-------------------|----------------|
| 255.255.255.0| 192.168.1.0   | 192.168.1.1    | 192.168.1.254     | 192.168.1.255  |
| 255.255.255.0| 192.168.10.0  | 192.168.10.1   | 192.168.10.254    | 192.168.10.255 |
| 255.255.255.0| 190.80.0.0    | 190.80.0.1     | 190.80.0.254      | 190.80.0.255   |
| 255.255.0.0  | 190.1.0.0     | 190.1.0.1       | 190.1.255.254     | 190.1.255.255  |
| 255.255.0.0  | 10.20.0.0     | 10.20.0.1       | 10.20.255.254     | 10.20.255.255  |
| 255.0.0.0    | 127.0.0.0     | 127.0.0.1       | 127.255.255.254  | 127.255.255.255|

### Difusión por Broadcast y dominio de Broadcast

**Difusión por Broadcast:**

El protocolo IP en su versión 4 (IPv4) también permite la difusión de datos, esto quiere decir que los mensajes en lugar de ir dirigidos a un host en particular pueden enviarse a todos los hosts que estén bajo una red lógica, y esto se hace a través de la dirección de Broadcast, que es la última dirección posible dentro de una red lógica.

**Dominio de broadcast:**

Para que esto suceda todos los hosts deben estar bajo la misma red lógica, compartir la misma máscara y dirección de Broadcast, y esto nos lleva a otro concepto: Dominio de Broadcast.

Cuando hablamos de Dominio de Broadcast estamos hablando del segmento de red lógico que se desprende de él, en cierta forma hablar de ID de red y Dominio de Broadcast es lo mismo, ambos se refieren al mismo segmento de red:

- ID de red 192.168.1.0/24 - Broadcast 192.168.1.255
- Broadcast 190.66.255.255/16 - ID de red 190.66.0.0

La diferencia es que la ID de red es una dirección no asignable a host mientras que el broadcast es una dirección que todos los hosts tienen asignadas, además de la propia dirección que es única y no se debe repetir en otro host.

### Asignación de direcciones a hosts

La dirección IP, en realidad, no identifica a un host en la red, identifica a una interfaz de red que es utilizada por un host (pc, tablet, impresora, notebook, etc), por lo tanto, un host puede tener tantas direcciones IP como interfaces de red tenga conectadas a la red, aún dentro del mismo segmento de red lógico.

No importa el tipo de dispositivo, mientras que su forma de conectarse en red sea bajo el mismo modelo, por ejemplo OSI, utilizarán las mismas tecnologías y protocolos, por lo tanto puede cambiar el cómo, pero todos los dispositivos se configurarán de la misma manera:

- Se le determina una dirección IP.
- Se le determina una Máscara.

De lo anterior, por lógica, se desprende la ID de red y la dirección de Broadcast.

- IP: 192.168.1.5
- MASK: 255.255.255.0 BCAST: 192.168.1.255 NET: 192.168.1.0
- IP: 192.168.1.102 MASK: 255.255.255.0 BCAST: 192.168.1.255 NET: 192.168.1.0
- IP: 192.168.1.18 MASK: 255.255.255.0 BCAST: 192.168.1.255 NET: 192.168.1.0
- IP: 192.168.1.22 MASK: 255.255.255.0 BCAST: 192.168.1.255 NET: 192.168.1.0

# Segmentación de redes

Para que las redes funcionen de forma eficiente, sean estables y se puedan aprovechar las tecnologías utilizadas, estas se diseñan y organizan en segmentos pequeños que se comunican con otros segmentos.

En una red de gran tamaño circula una gran cantidad de datos y es más propensa a presentar problemas como las congestiones, lo cual afecta a toda la red. En cambio, en un segmento de red pequeño, el volumen de datos es mucho menor, reduciendo las congestiones. Además, un problema en un segmento no afecta al resto de la red, es más fácil de trabajar, mejora el manejo de la seguridad y permite aislar los problemas en el ámbito del segmento, tanto a nivel físico como lógico.

Segmentar la red no reduce el volumen total de tráfico, sino que lo organiza, establece caminos entre segmentos y dirige el tráfico por criterios diversos, como por ejemplo jerarquías. Los caminos o conexiones que transportan el tráfico a otros segmentos de red se los denomina 'backbones' o segmentos de red 'troncales'.

## Subnetting

Cuando se diseña una red, se deben tener en cuenta muchos factores, como por ejemplo:

- Áreas de la organización, por ejemplo la red de una empresa tendría la red de gerencia, la red de ventas, la red de administración.
- Determinar la cantidad de hosts que podría llegar a haber en cada área.
- Establecer la red que se utilizará y las subredes de cada área.

Establecer un diseño claro antes de implementar la red nos permite:

- Escalar la red (aumentar número de hosts y subredes).
- Reducir el tamaño de los dominios de broadcast.
- Hacer la red más manejable, administrativamente. Entre otros, se puede controlar el tráfico entre diferentes subredes mediante listas de control de acceso (ACL).

## Robando bits

Tomemos la red ‘192.168.0.0/24’, veamos la representación binaria de su máscara:

11111111.11111111.11111111.0000000 = 255.255.255.0 = 24 bits

Tenemos 24 bits para red y 8 bits para hosts. Para dividir la red en subredes tenemos que ‘robarle’ una cantidad de bits a los que están destinados para hosts, por lo tanto aumentamos la cantidad de redes pero reducimos la cantidad de hosts.

Partiendo de la red ‘192.168.0.0/24’ vamos a aumentar la máscara a 28 bits, quedando:

11111111.11111111.11111111.11110000 = 255.255.255.240 = 28 bits

Tenemos 28 bits para crear redes y 4 bits para asignar a hosts (restando id de red y broadcast) por cada red.

## Saltos de red

Establecimos que dividimos la red 192.168.0.1/24 en redes más pequeñas, con una máscara de 28 bits y que la primer subred es la ‘192.168.0.0/28’, por lo tanto:

ID de red: 192.168.0.0
Primer IP de host: 192.168.0.1
Última IP de host: 192.168.0.14
Broadcast: 192.168.0.15

Cuando llegamos al broadcast significa que la subred finaliza en ese punto, por lo tanto los 16 números siguientes por encima del 15 representan la siguiente subred, y así sucesivamente.

