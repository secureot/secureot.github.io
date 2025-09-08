---
title: "Hierarchical-Network-Design"
date: 2023-10-26
draft: false
weight: 1
---

**Definición:** Un modelo que divide una red en tres capas (acceso, distribución y núcleo) para simplificar la gestión, mejorar la escalabilidad y optimizar el rendimiento.

**Ejemplo de uso:** "El diseño jerárquico de una red de campus universitario divide la red en capas de acceso, distribución y núcleo, lo que simplifica la gestión y la resolución de problemas."

```mermaid
graph TD
    A[Capa de Acceso] -- Conecta a --> B[Capa de Distribución];
    B -- Conecta a --> C[Capa de Núcleo];
    C -- Conecta a --> D[Internet];
    style A fill:#bbf,stroke:#333,stroke-width:2px
    style B fill:#bfb,stroke:#333,stroke-width:2px
    style C fill:#fbb,stroke:#333,stroke-width:2px
    style D fill:#ddd,stroke:#333,stroke-width:2px

