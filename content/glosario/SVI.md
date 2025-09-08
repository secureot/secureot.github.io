---
title: "SVI"
date: 2023-10-26
draft: false
weight: 1
---

**Definición:** Una interfaz virtual utilizada para gestionar y enrutar el tráfico de VLAN en un switch.

**Ejemplo:** Una SVI es una interfaz virtual que permite el enrutamiento inter-VLAN. Este ejemplo crea una SVI para la VLAN 20.

```
Switch(config)#interface vlan 20
Switch(config-if)#ip address 192.168.20.1 255.255.255.0
Switch(config-if)#no shutdown
