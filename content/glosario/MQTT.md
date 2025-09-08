---
title: "MQTT"
date: 2023-10-26
draft: false
weight: 1
---

**Definición:** Un protocolo ligero de publicar-suscribir diseñado para dispositivos con recursos limitados y redes de bajo ancho de banda, comúnmente utilizado en aplicaciones de IoT e industriales. Un protocolo ligero de publicar-suscribir utilizado para una mensajería eficiente en IIoT y IACS, especialmente en dispositivos con recursos limitados.

**Ejemplo de uso:** "Los sensores de temperatura en un edificio inteligente utilizan MQTT para enviar datos a un servidor de la nube. Debido a su naturaleza ligera, es ideal para dispositivos con batería y redes de bajo ancho de banda."

```mermaid
graph TD
    A[Sensor de Temperatura] -- Publicar (Topic: temp/edificio/piso1) --> B[Broker MQTT];
    C[Aplicación de monitoreo] -- Suscribir (Topic: temp/edificio/piso1) --> B;
    B -- Notificar --> C;
