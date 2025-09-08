---
title: "Modelo-Cliente-Servidor"
date: 2023-10-26
draft: false
weight: 1
---

**Definición:** Una arquitectura de red donde los clientes inician solicitudes de servicios o datos, y los servidores responden. Se caracteriza por el control centralizado, la escalabilidad y el intercambio de recursos.

**Ejemplo de uso:** "El modelo cliente-servidor es el estándar para la mayoría de las aplicaciones web. Tu navegador (cliente) solicita una página web, y el servidor web la envía de vuelta."

```mermaid
graph TD
    A[Cliente] -- Solicitud de datos --> B[Servidor];
    B -- Envío de datos --> A;
