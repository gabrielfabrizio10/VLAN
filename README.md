# VLAN
Vlan 
Es una red de área local virtual que es una colección de computadoras en una o varias LAN que se agrupan en un solo dominio de difusión, independientemente de su ubicación física. 
Esto permite agrupar dispositivos de acuerdo con patrones de tráfico en lugar de proximidad física.
Sirven para que nos permitan dividir la red en grupos con una agrupación o estructura jerárquica lógica en lugar de una física así esto ayuda a liberar al personal de TI de las restricciones del diseño de red y la infraestructura de cableado existente. 
De ahí que las VLAN faciliten el diseño, la implementación y la administración de la red
[![image.png](https://i.postimg.cc/cH4Sp02M/image.png)](https://postimg.cc/TySFmMRp)

Configuración en Packet tracer 
Para tenerlo es necesario crearlo desde el GUI 
Es bastante sencillo, la red consistirá en 6 ordenadores, 2 switches y la red dividida en 3 VLANS
[![image.png](https://i.postimg.cc/c1vHCBk7/image.png)](https://postimg.cc/K4yFsB24)

Debemos realizar la conexión de los Switches y las PCs.
Los switches se conectan por la interfaz Fa3/1 de cada uno de ellos con cable cruzado y en modo trunk 

[![image.png](https://i.postimg.cc/QC7hbSvR/image.png)](https://postimg.cc/MfzCZ06D)

Para asignar las IPs y la máscara de Red de nuestros equipos haremos doble click en la interfaz gráfica en cada uno de ellos en IP configuration introducimos la IP y su máscara de red.
El Gateway y DNS no son necesarios en este ejemplo.
Así usaremos una máscara de red /24 por lo tanto 255.255.255.0 
De esa forma así tendremos las máscaras de red:

[![image.png](https://i.postimg.cc/gJXWzNcn/image.png)](https://postimg.cc/2bDJTdZD)

Configuración de red en máquinas virtuales.
La configuración son las opciones que nos permiten definir si una máquina virtual debe tener acceso a Internet y acceso a la red local doméstica o si por el contrario queremos aislar el tráfico de red de esa máquina virtual en cuestión para que no tenga comunicación con otros equipos de la red local y únicamente con el equipo real.

[![image.png](https://i.postimg.cc/TYxZFRby/image.png)](https://postimg.cc/4n8LhRBZ)

Diferentes configuraciones de los adaptadores de red
Según el protocolo de transmisión, los adaptadores de red se pueden dividir en tres tipos: tarjeta Ethernet, tarjeta FC y tarjeta IB.
Tarjeta Ethernet (adaptador Ethernet)
Al utilizar el protocolo IP como protocolo de transmisión, generalmente se conecta al conmutador Ethernet a través de un cable de fibra óptica o un cable de par trenzado. 
El puerto óptico utiliza cable de fibra óptica para la transmisión de datos y la interfaz del módulo correspondiente suele ser SFP, QSFP, etc. 
Las interfaces de fibra óptica correspondientes son LC, SC, MPO, etc. 
El tipo de interfaz común del puerto eléctrico es RJ45, que generalmente se conecta con cable de par trenzado y también hay una pequeña cantidad de interfaces conectadas con cable coaxial.

[![image.png](https://i.postimg.cc/yxsvQ8Gs/image.png)](https://postimg.cc/jw3HCtKF)

tarjeta CF
Su nombre científico es Fibre Channel, utiliza el protocolo de transmisión Fibre Channel y se conecta al conmutador Fibre Channel a través de cables ópticos. 
Tiene dos tipos de interfaces las cuales son ópticas y eléctricas. 
Los modos de transmisión y los módulos correspondientes de los puertos ópticos son similares a los de las tarjetas Ethernet, pero los puertos correspondientes son solo SC y LC. 
El tipo de interfaz eléctrica es DB9 o HSSDC.


[![image.png](https://i.postimg.cc/wj83SRVX/image.png)](https://postimg.cc/9rbW9Ms0)

Tarjeta IB
 Infiniband se utiliza para conectar dispositivos FC/IP SAN, dispositivos NAS y servidores y se utiliza como protocolo de almacenamiento de iSCSI RDMA. 
Las tarjetas Infiniband ofrecen una latencia ultra baja, un rendimiento ultra alto y motores informáticos de red innovadores que brindan la aceleración, la escalabilidad y las tecnologías ricas en funciones necesarias para las cargas de trabajo modernas de hoy.


[![image.png](https://i.postimg.cc/SR4kgcqR/image.png)](https://postimg.cc/JDpfnDsC)
