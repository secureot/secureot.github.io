---
title: "STP"
date: 2023-10-26
draft: false
weight: 1
---

**Definición:** Un tipo de cableado con blindaje para reducir la interferencia para una transmisión de datos fiable. Un cable diseñado con blindaje para proteger contra la interferencia electromagnética. Un protocolo de red que previene bucles en redes Ethernet al crear una estructura de árbol de expansión. Un protocolo que previene bucles en redes Ethernet al bloquear rutas redundantes, ajustándose dinámicamente a las fallas de enlaces para garantizar la estabilidad de la red.

**Ejemplo:** STP previene bucles en la red. Si bien está habilitado por defecto, puedes configurarlo para dar prioridad a un switch como raíz.

```
Switch(config)#spanning-tree vlan 20 root primary
