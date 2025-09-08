---
title: "DHCP"
date: 2023-10-26
draft: false
weight: 1
---

**Definición:** Un protocolo que asigna automáticamente direcciones IP y otros detalles de configuración de red a los dispositivos. Un protocolo que asigna dinámicamente direcciones IP a los dispositivos en una red. Un protocolo que asigna automáticamente direcciones IP y otros detalles de configuración de red a los dispositivos en una red.

**Ejemplo:** Este es un ejemplo de cómo configurar un router como servidor DHCP para asignar direcciones IP a los clientes en la red 192.168.1.0/24.

```
Router(config)#ip dhcp pool home-lan
Router(config-dhcp)#network 192.168.1.0 255.255.255.0
Router(config-dhcp)#default-router 192.168.1.1
Router(config-dhcp)#dns-server 8.8.8.8 8.8.4.4
Router(config-dhcp)#exit
Router(config)#ip dhcp excluded-address 192.168.1.1
