# Modulo 5
- Medios
- Ancho de banda
- Velocidad de transmicion
- Medios de transmicion guiados
- Medios de transmicion no guiados
- Servidor de red 

# Medios de Transmisión

Los medios de transmisión son las vías físicas por las cuales se transportan las tramas de datos. Según el modelo OSI, corresponden a la capa 1 (física). Pueden clasificarse en dos grandes grupos:

- **Medios de transmisión guiados o alámbricos.**
- **Medios de transmisión no guiados o inalámbricos.**

## Tipos de Medios de Transmisión

Según el sentido de la transmisión, existen tres tipos:

- **Simplex**
- **Semi-duplex (half-duplex)**
- **Duplex completo (full-duplex)**

Otra característica importante es el **ancho de banda**, que determina la cantidad de información que puede transportar y la velocidad de transmisión.

## Señalización

La información se representa generando señales mediante la variación de voltaje, intensidad lumínica u ondas de radio, que se vuelcan en un medio de transmisión adecuado.

## Enviando Bits

En las redes, la interfaz de red toma una trama (secuencia de bits) y genera la señal correspondiente para representar esos bits en el medio de transmisión.

## Señales Digitales

Las señales digitales son discretas, con valores finitos, representadas típicamente como pulsos eléctricos que pueden ser 1 o 0 en sistemas binarios.

## Señales Analógicas

Las señales analógicas varían de forma continua entre sus puntos más altos y más bajos, como las ondas senoidales, que se encuentran en la transmisión inalámbrica por ondas de radio.

## Conclusión: Analógico vs. Digital

Cada tipo de señal tiene características propias y su uso está determinado por el tipo de información, medio, dispositivos, etc. Los dispositivos están diseñados para trabajar según estándares específicos, por lo que conectar dispositivos que esperan tipos de señal diferentes puede causar problemas.

# Ancho de Banda

El ancho de banda se define como la cantidad máxima de información (bits) que puede ser transmitida a través de un medio en un momento dado. Se puede visualizar utilizando el símil de un caño de agua, donde un caño más grande permite el paso de más agua en el mismo período de tiempo que uno más pequeño.

## Medición del Ancho de Banda

En networking, las mediciones de ancho de banda se hacen en bits por segundo (bps). Es importante distinguir entre bits y bytes: 1 byte = 8 bits. Las unidades comunes incluyen:

- **1 bps**
- **1 Kbps** (1.000 bps)
- **1 Mbps** (1.000.000 bps)
- **1 Gbps** (1.000.000.000 bps)

Para convertir de bits a bytes, se divide la cantidad de bits entre 8. Por ejemplo, una conexión de 1 Gbps podría transferir un archivo de 125 MB en un segundo en condiciones ideales.

## Ancho de Banda y Topología de Red

El ancho de banda es crucial para determinar el tipo de conexiones entre segmentos de red. Las conexiones deben ser capaces de soportar el volumen de datos transmitidos entre los dispositivos. Los backbones, que conectan los segmentos de red, suelen tener un ancho de banda mucho mayor que las conexiones entre dispositivos individuales.

## Estimación del Ancho de Banda

La estimación del ancho de banda necesario para un segmento de red se basa en el tipo y cantidad de información que los hosts necesitan enviar y recibir. Este estimado se multiplica por la cantidad de hosts dentro del segmento para determinar el ancho de banda necesario en el backbone que lo conecta con otros segmentos.

Es importante considerar que rara vez todos los hosts de un segmento de red utilizan simultáneamente toda la capacidad de ancho de banda disponible.

# Velocidad de Transmisión

El término **velocidad de transmisión** se refiere a la rapidez con la que se transmiten los datos a través de una conexión de red. Aunque está relacionado con el ancho de banda, no es lo mismo. El ancho de banda se refiere a la cantidad de información que se puede transmitir en un momento dado, mientras que la velocidad de transmisión se refiere a la rapidez con la que esa información se transmite o descarga.

## Latencia

La **latencia** es el tiempo que tarda un paquete de datos en viajar desde el origen hasta el destino. Se mide en milisegundos y puede afectar a actividades como los juegos en línea o las videollamadas. El protocolo ICMP y el comando 'ping' son herramientas comunes para medir la latencia.

## Factores que Influyen en la Velocidad

Varios factores pueden influir en la velocidad de transmisión, incluyendo:

- **Procesamiento**: Tiempo que tardan los routers en examinar y dirigir los paquetes.
- **Cola**: Tiempo de espera de un paquete antes de ser transmitido.
- **Transmisión**: Tiempo que tarda un paquete en llegar a su destino.
- **Propagación**: Tiempo que tarda un bit en viajar de un punto a otro, generalmente limitado por la velocidad de la luz.
- **Ancho de Banda de las Conexiones Intermedias**: Puede crear cuellos de botella y afectar la velocidad.

## Tasa de Transferencia

La **tasa de transferencia de datos (DTR)** es la velocidad a la que los datos pueden ser transmitidos entre dispositivos. Se expresa comúnmente en kilobits o megabits por segundo (kbps o mbps).

## Ejemplo de Cálculo de Velocidad de Transferencia

La velocidad de transferencia se calcula dividiendo la cantidad de datos entre el tiempo de transferencia. Por ejemplo, si se transfieren 25 MB en 2 minutos, la velocidad de transferencia sería de aproximadamente 1.208 Mbps.

## Full Duplex y Half Duplex

- **Full Duplex**: Permite la transmisión y recepción simultáneas de datos a través de un canal, lo que mejora las velocidades de transferencia.
- **Half Duplex**: Solo puede transmitir en una dirección a la vez, lo que reduce el rendimiento pero permite la comunicación bidireccional.

En resumen, la velocidad de transmisión depende de varios factores, incluyendo la latencia, el procesamiento, el ancho de banda y el tipo de conexión (Full Duplex o Half Duplex).

# Medios de transmisión guiada

Los medios de transmisión guiados están constituidos por cables que se encargan de la conducción (o guiado) de las señales desde un extremo al otro. Las principales características de los medios guiados son el tipo de conductor utilizado, la velocidad máxima de transmisión, las distancias máximas que puede ofrecer entre repetidores, la facilidad de instalación, la inmunidad frente a interferencias electromagnéticas y la capacidad de soportar diferentes tecnologías de nivel de enlace. La velocidad de transmisión depende directamente de la distancia entre los terminales, y de si el medio se utiliza para realizar un enlace punto a punto o un enlace multipunto. Debido a esto, los diferentes medios de transmisión tendrán diferentes velocidades de conexión que se adaptarán a utilizaciones dispares. Dentro de los medios de transmisión guiados, los más utilizados en el campo de las telecomunicaciones y la interconexión de computadoras son tres: cable de par trenzado, cable coaxial y fibra óptica.

## Cable de par trenzado UTP

El cable de par trenzado es el tipo de cable más utilizado en redes LAN y está tipificado en el estándar Ethernet. Se trata de pares de hilos trenzados de manera helicoidal, estos hilos están hechos de aleaciones de cobre o aluminio y conducen corrientes eléctricas.

## Cable coaxial

El cable coaxial consiste de un conductor de cobre rodeado de una capa aislante flexible. El conductor central también puede ser hecho de aluminio para una fabricación más económica, sobre el material aislante existe una malla de cobre tejida que actúa como el segundo hilo del circuito y como un blindaje para el conductor interno, así también esta capa reduce la cantidad de interferencias electromagnéticas externas.

## Cable de fibra óptica

El cableado de fibra óptica utiliza fibras de plástico o de vidrio para guiar los impulsos de luz desde el origen hacia el destino. Los bits se codifican en la fibra como impulsos de luz. El cableado de fibra óptica puede generar velocidades muy superiores de ancho de banda para transmitir datos sin procesar. La mayoría de los estándares actuales de transmisión aún necesitan analizar el ancho de banda potencial de este medio.

# Medios de transmisión no guiados o inalámbricos

Los medios inalámbricos transportan señales electromagnéticas mediante frecuencias de microondas y radiofrecuencias que representan los dígitos binarios de las comunicaciones de datos. Como medio de red, el sistema inalámbrico no se limita a conductores o canaletas, como en el caso de los medios de fibra o de cobre.

## Estándares de WiFi

- **IEEE 802.11a:** opera en una banda de frecuencia de 5 GHz y ofrece velocidades de hasta 54 Mbps. Tiene un área de cobertura menor y es menos efectiva al penetrar estructuras edilicias debido a sus frecuencias superiores.
  
- **IEEE 802.11b:** opera en una banda de frecuencia de 2.4 GHz y ofrece velocidades de hasta 11 Mbps. Los dispositivos que implementan este estándar tienen un mayor alcance y pueden penetrar mejor las estructuras edilicias que los dispositivos basados en 802.11a.

- **IEEE 802.11g:** opera en una frecuencia de banda de 2.4 GHz y ofrece velocidades de hasta 54 Mbps. Tiene un alcance similar al de 802.11b pero con un ancho de banda similar al de 802.11a.

- **IEEE 802.11n:** está en desarrollo y define una frecuencia de 2.4 GHz o 5 GHz. Se espera una velocidad típica de transmisión de datos de 100 Mbps a 210 Mbps con un alcance de hasta 70 metros.

## Acceso al medio

Las interfaces de red inalámbricas vuelcan señales al medio (el aire) mediante el uso de antenas. La capacidad de una antena de recolectar señales se mide en ganancia, en DBi. No debe confundirse ganancia con potencia, ya que este término se refiere al "volumen" de señales evocadas al medio.

## Tipos de antenas

- **Omnidireccionales:** pueden captar y enviar señales en todas direcciones.
  
- **Direccional:** se utilizan para establecer enlaces de punto a punto y a largas distancias, ya que concentra toda la energía hacia un foco.

## Dispositivos inalámbricos

Existen diferentes dispositivos según el tipo de tecnología y solución ofrecida, pero dos tipos comunes son:

- **Access Point:** es el dispositivo al que se conectan las interfaces inalámbricas de los dispositivos de usuario, similar a un "switch" inalámbrico.
  
- **Adaptadores WiFI:** son interfaces de red que utilizan un medio inalámbrico para enviar y recibir señales.

# Servicios de red

## Identificación de hosts en la red: Servicio WINS y NETBIOS

En el caso de las redes con hosts que ejecutan Windows existen dos tipos de servicios que se encargan de anunciar al host e identificar un host en la red:

- **NetBIOS:** Este servicio identifica un host bajo un nombre, es decir el nombre de host.
- **WINS (Windows Internet Naming Service):** Es un servidor de nombres de Microsoft para NetBIOS, que mantiene una tabla con la correspondencia entre direcciones IP y nombres NetBIOS de ordenadores.

## Servicio DNS (Sistema de Nombres de Dominio)

El DNS traduce nombres de dominio a direcciones IP y viceversa. Utiliza servidores DNS para resolver consultas de nombres de dominio. Se puede configurar un servidor DNS en la red local para evitar el uso excesivo de ancho de banda de Internet y mejorar los tiempos de respuesta.

## Funcionamiento del DHCP (Protocolo de Configuración Dinámica de Host)

El DHCP asigna dinámicamente direcciones IP y otros parámetros de configuración de red a dispositivos en una red. Permite una configuración automática de red, minimizando la necesidad de configuración manual en cada host. Utiliza un proceso de solicitud y respuesta entre el cliente DHCP y el servidor DHCP para asignar direcciones IP.

## Pool de direcciones y direcciones estáticas

El servidor DHCP administra un conjunto de direcciones IP disponibles para asignar a los dispositivos en la red (pool de direcciones). Algunos dispositivos pueden requerir direcciones IP estáticas para mantener una configuración constante, como los servidores que ofrecen servicios a la red externa.


