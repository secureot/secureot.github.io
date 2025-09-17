---
title: "LLDP"
date: 2023-10-26
draft: false
weight: 1
---

### **LLDP (Link Layer Discovery Protocol)**

El **Link Layer Discovery Protocol (LLDP)** es un protocolo de capa 2 que permite a los dispositivos de red (como switches, routers y puntos de acceso) anunciar su identidad, capacidades y vecinos a otros dispositivos de la red local. LLDP opera de forma unidireccional y es un protocolo fundamental para la gestión, el mapeo y la resolución de problemas de una red.

---

#### **Funcionamiento e información clave**

El funcionamiento de LLDP es simple: los dispositivos envían periódicamente mensajes llamados **LLDP Data Units (LLDPDUs)** a sus vecinos de la red. Estos mensajes contienen información útil sobre el dispositivo de envío:

* **Identificador del dispositivo y del puerto**: El nombre del dispositivo y la descripción del puerto de envío.
* **Capacidades del dispositivo**: La función del dispositivo (por ejemplo, router, switch o punto de acceso).
* **Dirección de gestión**: Las direcciones IP a través de las cuales se puede gestionar el dispositivo.
* **VLANs y PoE**: Información sobre las VLANs a las que pertenece el dispositivo y sus capacidades de alimentación a través de Ethernet (PoE).

---

#### **Beneficios en la gestión de red**

* **Descubrimiento y documentación automáticos**: LLDP permite a las herramientas de gestión de red crear mapas de la topología de la red de forma automática. Esto simplifica la documentación y el inventario de los equipos.
* **Solución de problemas**: Cuando un técnico necesita resolver un problema, puede usar LLDP para identificar rápidamente qué dispositivo está conectado a un puerto específico y cuáles son sus capacidades.
* **Mejora de la compatibilidad**: Permite que dispositivos de diferentes fabricantes interactúen y compartan información de forma estandarizada.

