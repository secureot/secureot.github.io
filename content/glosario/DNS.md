---
title: "DNS"
date: 2023-10-26
draft: false
weight: 1
---

**Definición:** Un servicio que traduce nombres de dominio a direcciones IP para dirigir a los usuarios a los sitios web o servicios correctos. Un sistema que traduce nombres de dominio legibles por humanos (por ejemplo, www.example.com) a direcciones IP para enrutar a los usuarios al sitio web o servicio correcto. Un sistema jerárquico para traducir nombres de dominio legibles por humanos en direcciones IP. Un sistema que traduce nombres de dominio legibles por humanos en direcciones IP para enrutar solicitudes en internet.

**Ejemplo de uso:** "Cuando escribes 'www.google.com' en tu navegador, el sistema DNS traduce ese nombre de dominio a la dirección IP del servidor de Google para que tu navegador pueda acceder a él."

```mermaid
graph TD
    A[Usuario navegador] -- Solicita (https://www.ejemplo.com) --> B[Servidor DNS local];
    B -- No encuentra --> C[Servidor DNS raíz];
    C -- Dirección de TLD (.com) --> B;
    B -- Solicita a TLD --> D[Servidor TLD];
    D -- Dirección de DNS autoritativo --> B;
    B -- Solicita a DNS autoritativo --> E[Servidor DNS autoritativo];
    E -- Responde con IP de (https://www.ejemplo.com) --> B;
    B -- Cachea y responde con IP --> A;
    A -- Se conecta a la IP --> F[Servidor web];
