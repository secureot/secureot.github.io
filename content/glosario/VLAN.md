---
title: "VLAN"
date: 2023-10-26
draft: false
weight: 1
---

**Definición:** Una segmentación lógica de una red para separar y organizar dispositivos para una gestión y seguridad mejoradas. Una red lógica creada dentro de un switch para aislar dispositivos en dominios de broadcast separados, mejorando el control del tráfico y la seguridad. Una segmentación lógica de una red física que permite agrupar dispositivos, independientemente de su ubicación física, para una mejor gestión, seguridad y rendimiento. Una segmentación lógica de una red física en redes más pequeñas y aisladas para mejorar la seguridad y el rendimiento.

**Ejemplo:** Para crear y asignar una VLAN en un switch, se usan los siguientes comandos. Este ejemplo crea la VLAN 20 y la asigna al puerto FastEthernet 0/1.

```
Switch(config)#vlan 20
Switch(config-vlan)#name administracion
Switch(config-vlan)#exit
Switch(config)#interface fastEthernet 0/1
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 20
