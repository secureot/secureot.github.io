---
title: "ACL"
date: 2023-10-26
draft: false
weight: 1
---

**Definición:** Una función de seguridad en routers y firewalls que define reglas para permitir o denegar tráfico específico basado en direcciones IP, protocolos o puertos. Una serie de declaraciones utilizadas para filtrar el tráfico de red examinando la información de la cabecera del paquete, permitiendo o denegando paquetes basándose en criterios especificados como direcciones IP y números de puerto.

**Ejemplo de uso:** "Para proteger un servidor web, un administrador configura una ACL en un firewall para permitir el tráfico HTTP y HTTPS, pero bloquear todos los demás protocolos."

```mermaid
graph TD
    A[Tráfico entrante] --> B{Firewall con ACL?};
    B -- Sí --> C{Protocolo HTTP/S?};
    C -- Sí --> D[Permitir];
    C -- No --> E[Denegar];
    B -- No --> D;
