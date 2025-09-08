---
title: "Zonas y Conductos en Ciberseguridad Industrial"
date: 2023-10-26
draft: false
weight: 1
tags: ["ISA/IEC 62443", "zonificación", "conductos", "PERA", "OT", "ciberseguridad"]
summary: "Descripción de los conceptos de zonas y conductos en sistemas industriales, su relación con estándares como PERA y ISA/IEC 62443, y su implementación en arquitecturas OT."
---

**Definición:** Categorizar y aislar componentes de red en zonas distintas basándose en sus funciones y requisitos de seguridad, con límites y controles de acceso definidos.

La zonificación es una estrategia de seguridad clave en entornos industriales. Va más allá de la simple segmentación de red y se centra en agrupar activos con requisitos de seguridad similares en zonas. El principal objetivo de la zonificación es que si un atacante logra comprometer una zona, el daño no se propague al resto del sistema, lo que permite contener los incidentes de seguridad.

## Zonas y Conductos

### Zonas
Son agrupaciones lógicas de activos (dispositivos, sistemas o componentes) que comparten los mismos requisitos de seguridad. Estos activos pueden estar relacionados funcional, lógica y físicamente.

**Ejemplo:**  
En una planta de manufactura, la red de control de calidad y la red de los robots de ensamblaje pueden formar zonas separadas, incluso si están en el mismo espacio físico.

### Conductos
Son los canales de comunicación que conectan dos o más zonas y que tienen requisitos de seguridad definidos. Actúan como una interfaz controlada que gestiona y protege el flujo de datos entre las zonas mediante medidas de seguridad como el filtrado de tráfico, el cifrado y los controles de acceso.

**Ejemplo:**  
Un firewall configurado para permitir solo el tráfico necesario entre la red de producción y la red de supervisión actúa como un conducto, garantizando que los datos críticos no sean interceptados.

---

## Relación con Estándares Industriales

### Modelo PERA (Purdue Enterprise Reference Architecture)
El Modelo de Referencia de Arquitectura Empresarial de Purdue (PERA) fue un marco pionero que proporcionó una estructura jerárquica para segmentar las redes de control industrial (OT) y las redes empresariales (TI) en los años 90.

Este modelo divide la red en niveles:

- **Nivel 0:** Proceso físico  
- **Nivel 1–2:** Control básico y supervisión  
- **Nivel 3:** Gestión de producción  
- **Nivel 3.5:** Zona Desmilitarizada Industrial (IDMZ)  
- **Nivel 4–5:** Red empresarial y planificación

El concepto de zonas y conductos del estándar ISA/IEC 62443 es una evolución de este modelo, que ofrece un enfoque más flexible y no necesariamente jerárquico.

### Estándar ISA/IEC 62443
Este estándar formaliza la zonificación y los conductos como pilares de la ciberseguridad industrial para los sistemas de automatización y control (IACS).

#### Evaluación de Riesgos
Antes de la zonificación, se debe realizar una evaluación de riesgos para identificar amenazas y vulnerabilidades.

#### Niveles de Seguridad (Security Levels)
El estándar define cuatro niveles de seguridad que se aplican a las zonas y los conductos:

- **SL-1:** Protección contra violaciones accidentales o no intencionadas  
- **SL-2:** Protección contra ataques intencionales con recursos básicos  
- **SL-3:** Protección contra ataques sofisticados con recursos moderados y herramientas avanzadas  
- **SL-4:** Protección contra amenazas avanzadas con recursos extensos, como organizaciones criminales

#### Implementación
Una vez que se definen las zonas y los conductos, se aplican contramedidas de ciberseguridad correspondientes a los niveles de seguridad deseados para proteger cada segmento de la red.

---

## Diagrama de Zonificación y Conductos

> El siguiente diagrama simplificado ilustra cómo un sistema industrial puede ser dividido en zonas y conductos, con los niveles de seguridad aplicados según el estándar ISA/IEC 62443.

```mermaid
graph TD
    subgraph Internet
        A[Nube/Proveedor]
    end

    subgraph Zona Empresarial - SL-1
        B[Servidor de IT]
        C[Estación de trabajo]
    end

    subgraph DMZ Industrial - IDMZ
        D{Firewall / Proxy};
    end

    subgraph Zona de Supervisión - SL-2
        E[Servidor SCADA]
        F[HMI de Operador]
    end

    subgraph Zona de Control de Procesos - SL-3
        G[PLC Principal]
        H[PLC de Reserva]
    end

    subgraph Zona de Seguridad SL-4
        I[Sistema de Seguridad]
    end

    A -- "Conducto Externo" --> D;
    B -- "Conducto IT" --> D;
    C -- "Conducto IT" --> D;
    D -- "Conducto de IDMZ (SL-2)" --> E;
    D -- "Conducto de IDMZ (SL-2)" --> F;
    E -- "Conducto de Supervisión (SL-3)" --> G;
    E -- "Conducto de Supervisión (SL-3)" --> H;
    F -- "Conducto de Supervisión (SL-3)" --> G;
    G -- "Conducto de Control (SL-4)" --> H;
    H -- "Conducto de Control (SL-4)" --> I;

    style A fill:#e6f3ff,stroke:#333,stroke-width:2px;
    style B fill:#fff2e6,stroke:#333,stroke-width:2px;
    style C fill:#fff2e6,stroke:#333,stroke-width:2px;
    style D fill:#f2e6ff,stroke:#333,stroke-width:2px;
    style E fill:#e6ffe6,stroke:#333,stroke-width:2px;
    style F fill:#e6ffe6,stroke:#333,stroke-width:2px;
    style G fill:#ffcccc,stroke:#333,stroke-width:2px;
    style H fill:#ffcccc,stroke:#333,stroke-width:2px;
    style I fill:#ccffcc,stroke:#333,stroke-width:2px;
