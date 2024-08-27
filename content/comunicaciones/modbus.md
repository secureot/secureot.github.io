+++
title = "MODBUS"
+++

Modbus es un protocolo de comunicación serial desarrollado en 1979 por Modicon (ahora Schneider Electric) para su uso en controladores lógicos programables (PLC).
Desde entonces, se ha convertido en uno de los estándares más utilizados en la industria para la comunicación entre dispositivos electrónicos.

## Modbus a Nivel Eléctrico
En su forma más básica, Modbus opera sobre una interfaz serial, con las versiones más comunes siendo Modbus RTU y Modbus ASCII.
Aquí se utiliza la transmisión de datos en serie, donde la información se envía bit por bit a través de un solo canal, lo que resulta en una transmisión confiable y eficiente a largas distancias.

### Modbus RTU (Remote Terminal Unit)
* **Transmisión Diferencial**: Modbus RTU suele implementarse sobre interfaces físicas como RS485, que usa dos líneas de datos para la transmisión diferencial. Esto significa que el voltaje en una línea es el opuesto al de la otra, lo que permite una alta resistencia al ruido eléctrico y la posibilidad de comunicarse en entornos industriales ruidosos.
* **Formato de Datos**: Los datos se transmiten en formato binario, lo que lo hace más compacto y rápido que Modbus ASCII. La información se agrupa en tramas, que incluyen:
  * Un byte de dirección que identifica al dispositivo esclavo.
  * Bytes de función que definen la acción solicitada (como leer o escribir datos).
  * Bytes de datos para transmitir los valores de las variables.
  * Un CRC (Cyclic Redundancy Check) para asegurar la integridad de la comunicación.

### Modbus ASCII
* **Formato de Datos**: A diferencia de Modbus RTU, Modbus ASCII codifica los datos en caracteres ASCII legibles, lo que simplifica la depuración, aunque es menos eficiente en términos de velocidad de transmisión.
* **Transmisión**: También puede operar sobre interfaces como RS232 o RS485, y se utiliza en aplicaciones donde la velocidad no es crítica, pero la simplicidad y la facilidad de lectura son más importantes.

## Modbus a Nivel de Red
Con el avance de las tecnologías de red, Modbus también ha evolucionado para soportar la comunicación sobre redes TCP/IP, dando lugar a Modbus TCP/IP.

### Modbus TCP/IP
* **Protocolo en Capa de Aplicación**: Modbus TCP/IP se implementa sobre una red Ethernet estándar, lo que permite la comunicación entre dispositivos Modbus a través de una infraestructura de red existente. Esto es especialmente útil para integraciones con sistemas de IT y para la conexión remota de dispositivos.
* **Modelo Cliente/Servidor**: En Modbus TCP/IP, la comunicación sigue un modelo cliente/servidor. El cliente (generalmente un sistema SCADA o HMI) envía solicitudes a los servidores (dispositivos Modbus) para leer o escribir datos. Cada dispositivo en la red tiene una dirección IP única, y las solicitudes se encapsulan en tramas TCP/IP estándar.
* **Puertos y Comunicación**: Modbus TCP/IP utiliza el puerto 502 para la transmisión de datos. Las tramas son similares a las de Modbus RTU, pero encapsuladas en paquetes TCP/IP.

### Integración con Redes IT
* **Conectividad**: Gracias a Modbus TCP/IP, los dispositivos de OT pueden integrarse directamente en las redes IT, facilitando la gestión y el monitoreo desde sistemas centralizados.
* **Seguridad y Escalabilidad**: Modbus TCP/IP permite implementar medidas de seguridad modernas, como firewalls y VPNs, y soporta redes más grandes y distribuidas.
