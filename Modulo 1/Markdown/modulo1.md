# Modulo 1
- Redes de datos
- Elementos de una red
- Tipos de redes
- Topologias de red

# Introducción a Redes de Datos

## Desarrollo Histórico
Las redes de datos surgieron de la necesidad de las aplicaciones comerciales para compartir datos de manera eficaz, impulsando así la productividad y economía en el desarrollo empresarial. Desde principios de los años 80, la tecnología de redes experimentó una expansión significativa, con avances tanto en hardware como en software.

## Concepto de Red de Datos
Una red de datos es una infraestructura que conecta equipos informáticos y de comunicaciones mediante dispositivos físicos (nodos), utilizando señales eléctricas, ondas de radio, entre otros, para el intercambio de información y recursos, y la prestación de servicios.

### Ejemplo de una Red de Datos
- Medios de conexión
- Impresora
- Terminal
- Switch
- Servidor

## Elementos de la Comunicación en Redes
- **Emisor:** Quien construye el mensaje.
- **Mensaje:** Información que se transmite.
- **Protocolo:** Estructura y codificación del mensaje.
- **Medio:** Canal por donde circula el mensaje.
- **Receptor:** Quien recibe y decodifica el mensaje.

### Finalidad de las Redes de Datos
- Compartir recursos e información a distancia.
- Asegurar la confiabilidad y disponibilidad de la información.
- Acelerar la transmisión de datos.
- Incrementar la eficiencia y reducir costos.

## Impacto en la Vida Humana
La comunicación por redes ha revolucionado la manera en que compartimos ideas e información, integrando voz, video, texto y gráficos en una plataforma común que permite interacciones casi instantáneas.

## Aplicaciones Actuales de las Redes
Las tecnologías de red se aplican en diversos ámbitos, desde el consumo doméstico hasta la industria 4.0, impulsando la automatización y mejora de procesos en múltiples sectores. La era de la información se caracteriza por un flujo rápido y extenso de datos, facilitado por las

# Elementos Básicos de una Red de Datos

En una red de datos, se pueden identificar cuatro grupos principales de elementos, cada uno desempeñando un rol específico en el proceso de comunicación:

1. **Dispositivos:** Incluyen hosts y dispositivos de red.
2. **Mensajes:** La información que se transporta por la red.
3. **Reglas:** Conjunto de reglas o protocolos que rigen el envío y recepción de mensajes.
4. **Medios:** El medio físico a través del cual se transporta la información.

## Modelo de Capas OSI

El Modelo de Interconexión de Sistemas Abiertos (OSI) es un estándar que describe las etapas del proceso de comunicación y los protocolos involucrados en cada una de ellas.

- **Nivel de Aplicación:** Servicios de red a aplicaciones.
- **Nivel de Presentación:** Representación de los datos.
- **Nivel de Sesión:** Comunicación entre dispositivos de la red.
- **Nivel de Transporte:** Conexión de extremo a extremo y control de flujo de datos.
- **Nivel de Red:** Determinación de ruta y direccionamiento lógico (IP).
- **Nivel de Enlace de Datos:** Direccionamiento físico (MAC y LLC).
- **Nivel Físico:** Señal y transmisión binaria.

## Mensajes (Capas de Anfitrión)

Los mensajes son la información que se transporta por la red, generada por aplicaciones o usuarios. Los protocolos de aplicación determinan el formato del mensaje y otra información relevante.

## Reglas (Protocolos)

Los protocolos son conjuntos de reglas que especifican cómo se envían los mensajes a través de la red y cómo las aplicaciones intercambian información.

## Dispositivos

### Hosts
Los hosts son equipos conectados a la red que ofrecen y utilizan servicios. Pueden ser dispositivos de usuario final o servidores.

### Dispositivos de Usuario Final
Son dispositivos que generan e interpretan la información que se envía o recibe. Incluyen computadoras, smartphones, impresoras, entre otros.

### Servidores
Son hosts que ponen a disposición de los usuarios distintos servicios, como archivos, impresión, correo, web, y streaming.

### Dispositivos de Red
Conectan dispositivos de usuario y servidores, agrupándolos en segmentos de red. Ejemplos incluyen switches, NICs, routers, bridges, hubs, y repeaters.

## Medio
El medio es el medio físico por el cual se transporta la información. Puede ser cableado (cobre u óptico) o inalámbrico (ondas de radio).

## Conclusión

Es esencial comprender los diferentes elementos físicos que componen una red de datos, desde los dispositivos de usuario y servidores hasta los dispositivos de red y el medio físico por el cual se transmiten los datos.

# Tipos de Redes

Las redes de datos se clasifican según su utilización, tipo de infraestructura/arquitectura y el área geográfica que ocupan.

## Redes PAN (Red de Área Personal)

Las redes PAN permiten el intercambio de datos entre dispositivos modernos como smartphones, tablets, y computadoras portátiles. Pueden ser por cable (PAN) o inalámbricas (WPAN) utilizando tecnologías como Bluetooth, Wireless USB, etc. Su alcance se limita a unos pocos metros.

## Redes LAN (Red de Área Local)

Las redes LAN están formadas por dos o más dispositivos de usuario, permitiendo la comunicación entre ellos. Cubren un área geográfica única y proporcionan acceso a servicios y aplicaciones dentro de una estructura organizacional común, como empresas, campus o redes domésticas.

## Nodos de Red

Los nodos de red son puntos de conexión que pueden recibir, crear, almacenar o enviar datos a lo largo de rutas de red distribuidas. En una LAN, un nodo puede ser cualquier dispositivo conectado, como módems, puntos de acceso inalámbrico y ordenadores.

## Redes MAN (Red de Área Metropolitana)

Las redes MAN son redes de telecomunicaciones de banda ancha que conectan varias redes LAN en una zona geográficamente cercana, como sedes de empresas. Utilizan routers de alto rendimiento y fibra óptica para lograr velocidades comparables a las de una LAN.

## Redes WAN (Red de Área Amplia)

Las WAN se extienden por zonas geográficas como países o continentes, conectando múltiples redes locales o terminales individuales. Pueden ser gestionadas de manera privada por organizaciones o empresas, o por proveedores de servicios de Internet para conectar redes corporativas locales y consumidores a Internet.

# Topologías de Red

La topología de una red se refiere a la configuración o relación de los dispositivos de red y las interconexiones entre ellos. Puede describirse en dos niveles: físico y lógico.

## Topología Física

Es la disposición real de los medios de red y la configuración de los nodos, así como las conexiones físicas entre ellos. Las topologías físicas describen cómo se interconectan los dispositivos entre sí.

### Topologías Físicas Comunes:
- **Topología en Estrella:** Los nodos se conectan a un conmutador central, permitiendo la comunicación entre ellos a través de este punto central.
- **Topología en Anillo:** Los nodos se conectan formando un anillo cerrado, donde cada nodo está conectado a exactamente dos nodos vecinos, creando una comunicación en bucle.
- **Topología en Malla:** Todos los dispositivos están conectados entre sí, proporcionando múltiples rutas para la comunicación de datos.
- **Topología de Bus:** Todos los nodos comparten un solo canal de comunicación, en el que los mensajes se transmiten a todos los nodos en el bus.

## Topología Lógica

Es la forma en que los hosts se comunican a través de la red, definida por el protocolo de comunicación utilizado. Los dos tipos más comunes son la topología de broadcast y la transmisión de tokens.

### Características de la Topología Lógica:
- **Broadcast:** Cada host envía sus datos hacia todos los demás hosts del medio de red, sin un orden predefinido.
- **Transmisión de Tokens:** Los hosts solo pueden enviar datos cuando poseen un "token" o permiso de transmisión.

## Ejemplos de Topologías de Red
- **Topología Estrella:** Conexión de nodos a un conmutador central.
- **Topología Jerárquica:** Estructura de red en árbol con un nodo de enlace troncal.
- **Topología en Malla:** Todos los nodos están conectados entre sí, proporcionando redundancia y múltiples rutas de comunicación.

## Backbone de la Red
El backbone es la parte troncal de la red, diseñada para transportar grandes volúmenes de datos entre los segmentos de la red o para proporcionar conectividad a redes externas como Internet.

### Ejemplos de Implementaciones de Backbone:
- **Backbone en Serie:** Conexión secuencial de segmentos de red.
- **Backbone Distribuido:** Utiliza un diseño jerárquico con dispositivos de conectividad central.

