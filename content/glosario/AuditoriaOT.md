---
title: "Auditoría de Tecnología Operativa (OT)"
date: 2025-06-17
draft: false
weight: 1
---

### **Auditoría de Tecnología Operativa (OT)**

Una **auditoría de Tecnología Operativa (OT)** es una revisión sistemática de la postura de ciberseguridad de un sistema de control industrial (ICS). Su propósito es identificar vulnerabilidades, evaluar riesgos y verificar el cumplimiento de las políticas de seguridad y los estándares de la industria, como **ISA/IEC 62443**.

---

#### **Diferencias clave con una auditoría de TI**

Aunque ambas buscan mejorar la seguridad, una auditoría de OT se diferencia de una de TI en sus prioridades y metodología:

* **Prioridades**: La auditoría de OT prioriza la **seguridad funcional** y la **disponibilidad** del proceso por encima de la confidencialidad de los datos. Detener una línea de producción puede tener consecuencias graves, por lo que la auditoría debe ser no intrusiva.
* **Metodología**: Las herramientas y técnicas de una auditoría de OT están diseñadas para interactuar de forma pasiva con el entorno de control. Las pruebas de penetración o los escaneos de red activos, comunes en TI, se limitan a entornos de laboratorio o se realizan con extrema precaución.

---

#### **Fases de una auditoría de OT**

Una auditoría de OT generalmente sigue estas fases:

1.  **Planificación**: Se define el alcance, los objetivos y la metodología de la auditoría. Se identifican los estándares de referencia, como **IEC 62443**, y las políticas de seguridad de la organización.
2.  **Recopilación de información**: Se recopila información sobre la arquitectura de red (incluyendo las **zonas** y los **conductos**), los dispositivos de control (PLCs, HMIs), los protocolos utilizados y las configuraciones de seguridad. Se usan herramientas de mapeo pasivo y se revisa la documentación existente.
3.  **Análisis y evaluación**: Se analiza la información recopilada para identificar vulnerabilidades (por ejemplo, dispositivos sin parchear), configuraciones incorrectas y la falta de cumplimiento con los estándares.
4.  **Informe y recomendaciones**: Se elabora un informe detallado con los hallazgos de la auditoría y se proporcionan recomendaciones claras y accionables para mitigar los riesgos identificados, siempre priorizando la continuidad operativa y la seguridad.

---

#### **Estándares, marcos y guías para la auditoría de OT**

| Norma / Guía | Enfoque principal | Público objetivo | Alcance |
| :--- | :--- | :--- | :--- |
| **ISO 31000** | Gestión de riesgos genérica. | Todas las organizaciones. | Proporciona un marco de alto nivel para gestionar cualquier tipo de riesgo, incluyendo el ciber-riesgo en OT. |
| **ISO/IEC 27001** | Sistema de Gestión de la Seguridad de la Información (SGSI). | Todas las organizaciones. | Proporciona un marco de gestión para la seguridad de la información. La **disponibilidad** de los sistemas de OT es un pilar fundamental de esta norma. |
| **NIST SP 800-82** | Guía de seguridad específica para ICS. | Propietarios y operadores de sistemas de control. | Guía a las organizaciones en la aplicación de los controles de ciberseguridad del NIST en entornos OT, con un enfoque flexible y basado en riesgos. |
| **ISA/IEC 62443** | Estándar de ciberseguridad para todo el ciclo de vida de los IACS. | Propietarios de activos, integradores y fabricantes. | Es un estándar prescriptivo que define **Zonas y Conductos**, **Niveles de Seguridad (SL)** y requisitos técnicos específicos para el hardware y el software de OT. |

---

#### **Herramientas y metodologías**

* **Inspección de configuraciones**: Revisión de las configuraciones de firewalls, switches y PLCs para asegurar que se apliquen las políticas de seguridad correctas.
* **Mapeo de red pasivo**: Uso de **sniffers** o herramientas de escucha para descubrir los dispositivos de la red y el flujo de tráfico sin interactuar activamente con ellos.
* **Revisión de la arquitectura**: Evaluación de la segmentación de la red y de la seguridad de las **zonas** y los **conductos**, incluyendo la configuración de la **IDMZ**.

---

#### **Estándares de diseño de la ISA**

Para el diseño de sistemas, el estándar **ISA-95** es fundamental. Define los niveles jerárquicos y las interfaces para la integración de la información entre los sistemas empresariales (TI) y los sistemas de control (OT). Un auditor de OT utiliza el marco ISA-95 para validar la correcta separación lógica y física de las redes y los sistemas en la arquitectura de la organización.

---

#### **Referencias**

* **ISA/IEC 62443-3-2**: Este documento es clave para la zonificación, ya que establece la metodología para la evaluación de riesgos de ciberseguridad en el diseño de un sistema.
* **NIST SP 800-82**: La guía de seguridad para sistemas de control industrial del NIST aborda el concepto de seguridad de los conductos como parte de sus recomendaciones sobre la arquitectura de red y los controles de seguridad.
