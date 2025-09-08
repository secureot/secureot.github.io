---
title: "API"
date: 2023-10-26
draft: false
weight: 1
---

**Definición:** Un conjunto de protocolos y herramientas que permiten que las aplicaciones de software se comuniquen entre sí. Un conjunto de reglas y herramientas para construir aplicaciones de software que permiten la comunicación entre diferentes sistemas. Un conjunto de reglas y protocolos que permite a diferentes aplicaciones de software comunicarse e interactuar entre sí, permitiendo la integración y el intercambio de funcionalidades.

**Ejemplo de uso:** "El software de un sistema de control de calidad utiliza una API para comunicarse con la base de datos de producción y recuperar información sobre los lotes de productos."

```mermaid
graph TD
    A[Aplicación 1] -- Llamada a la API --> B[API];
    B -- Solicitud de datos --> C[Sistema 2];
    C -- Datos de respuesta --> B;
    B -- Envío de datos --> A;
