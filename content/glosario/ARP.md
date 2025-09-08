---
title: "ARP"
date: 2023-10-26
draft: false
weight: 1
---

**Definición:** Un protocolo que mapea direcciones IP a direcciones MAC físicas dentro de una red local. Un protocolo utilizado para mapear una dirección IP a una dirección MAC física dentro de una red local. Un protocolo utilizado para mapear una dirección IPv4 a una dirección MAC dentro de la misma red. Un protocolo utilizado para mapear una dirección IP a una dirección MAC física en una red local, permitiendo que los dispositivos se comuniquen dentro de la misma subred.

**Ejemplo de uso:** "Cuando una computadora quiere enviar un paquete a otra computadora en la misma red local, utiliza ARP para encontrar la dirección MAC de la computadora de destino, usando su dirección IP."

```mermaid
graph TD
    A[PC1 (IP: 10.0.0.1)] --> B{¿Conoce MAC de 10.0.0.2?};
    B -- No --> C[Envía Broadcast ARP];
    C --> D[PC2 (IP: 10.0.0.2)];
    D -- Responde con su MAC --> C;
    C --> B;
    B -- Sí --> E[Envía Unicast];
