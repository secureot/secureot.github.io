---
title: "NAT"
date: 2023-10-26
draft: false
weight: 1
---

**Definición:** Un proceso que modifica las direcciones IP en tránsito para permitir que múltiples dispositivos compartan una única dirección IP pública. Un método de remapeo de direcciones IP utilizado para permitir que múltiples dispositivos en una red privada compartan una única dirección IP pública.

**Ejemplo:** la red interna 192.168.1.0/24 se traduce a la dirección IP pública del router.

```
Router(config)#access-list 1 permit 192.168.1.0 0.0.0.255
Router(config)#ip nat inside source list 1 interface gigabitEthernet 0/1 overload
Router(config)#interface gigabitEthernet 0/0
Router(config-if)#ip nat inside
Router(config-if)#interface gigabitEthernet 0/1
Router(config-if)#ip nat outside
```

```mermaid
graph LR
    A[Red Interna<br/>192.168.1.0/24] --> B{Router<br/>con NAT};
    B --Tráfico privado (192.168.1.x)--> C[Interfaz Inside<br/>GigabitEthernet 0/0];
    C --Proceso de NAT--> D[Interfaz Outside<br/>GigabitEthernet 0/1];
    D --Tráfico público--> E[Internet<br/>Red Pública];
