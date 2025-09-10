+++
title = "Normas y standard"
+++

Al igual que en los ejemplos anteriores, los estándares industriales son conjuntos de normas y directrices que establecen criterios uniformes y específicos para la implementación y operación de tecnologías, procesos y productos en diversas industrias. Estos estándares, como las normas de seguridad industrial y ciberseguridad (por ejemplo, ISA/IEC 62443), aseguran que las organizaciones cumplan con requisitos mínimos de seguridad, interoperabilidad, calidad y eficiencia, facilitando la colaboración y el comercio a nivel global. Las normas industriales son desarrolladas por organismos de estandarización como ISO, IEC, o ANSI, y son clave para mantener la consistencia y garantizar la seguridad en sistemas críticos.

### **Profundización en Estándares y Marcos de Continuidad Operativa**

La continuidad operativa en los Sistemas de Control Industrial (ICS) no se gestiona de forma aislada, sino que se basa en un ecosistema de estándares y regulaciones que abordan desde la gestión general del riesgo hasta los requisitos técnicos de ciberseguridad.

---

#### **ISO 31000 (Gestión de Riesgos)**

**Qué es**: La **ISO 31000** es un estándar internacional para la gestión de riesgos que proporciona principios y directrices para ayudar a las organizaciones a integrar la gestión de riesgos en sus procesos de toma de decisiones. Su naturaleza es generalista, por lo que no especifica medidas concretas, sino que establece un marco de "cómo hacerlo".

* **Puntos clave del estándar**: La norma se estructura en torno a tres elementos principales:
    * **Principios**: Recomienda principios como la creación de valor, la integración en los procesos de la organización y la adaptabilidad al cambio.
    * **Marco**: Proporciona una estructura para implementar la gestión de riesgos en toda la empresa.
    * **Proceso**: Describe un proceso iterativo de comunicación y consulta, establecimiento de contexto, evaluación de riesgos (identificación, análisis y evaluación) y tratamiento de riesgos.

* **Aplicación en ICS**: La ISO 31000 es la base de cualquier plan de continuidad. Un plan de continuidad exitoso comienza identificando los riesgos de una interrupción (por ejemplo, el riesgo de un ciberataque a los PLCs que detenga la producción). La ISO 31000 proporciona la metodología para realizar esta evaluación de riesgos y definir la prioridad de las contramedidas.

---

#### **NIST (National Institute of Standards and Technology)**

**Qué es**: El **NIST** es una agencia de EE. UU. que desarrolla y promueve estándares para la tecnología, la ciencia y la ciberseguridad. Sus marcos y guías son adoptados globalmente y se centran en un enfoque basado en riesgos para la seguridad.

* **Puntos clave del marco**: El **NIST Cybersecurity Framework (CSF)** es un ejemplo destacado y se organiza en cinco funciones principales:
    * **Identificar**: Comprender los riesgos para los sistemas, activos, datos y capacidades.
    * **Proteger**: Implementar salvaguardias para asegurar los servicios críticos.
    * **Detectar**: Identificar la ocurrencia de un evento de ciberseguridad.
    * **Responder**: Actuar ante un incidente de ciberseguridad detectado.
    * **Recuperar**: Mantener la resiliencia y restaurar los servicios afectados.
* **Publicaciones especiales (Special Publications)**: Para ICS, las publicaciones como **NIST SP 800-82** se centran específicamente en la seguridad de los sistemas de control industrial.

* **Aplicación en ICS**: Los marcos del NIST son una referencia importante para los ICS porque proporcionan un método estructurado para la planificación de la continuidad. La función de **Recuperación** de su CSF es un pilar de cualquier plan de continuidad, ya que guía a las organizaciones en la restauración de los servicios y la infraestructura críticos después de un incidente, minimizando su impacto.

---

#### **ISA/IEC 62443 (Ciberseguridad para ICS)**

**Qué es**: **ISA/IEC 62443** es el estándar de ciberseguridad más importante para los Sistemas de Automatización y Control Industrial (IACS). Es una serie de documentos que abordan la ciberseguridad desde una perspectiva holística, cubriendo desde políticas y procedimientos hasta los requisitos técnicos de los componentes.

* **Estructura del estándar**: Se compone de cuatro partes principales, que abordan diferentes aspectos de la seguridad:
    * **Parte 1 (Generalidades)**: Define conceptos y terminología comunes.
    * **Parte 2 (Políticas y Procedimientos)**: Guía a los propietarios de activos sobre la implementación y la gestión de programas de ciberseguridad.
    * **Parte 3 (Requisitos del Sistema)**: Aborda los requisitos de seguridad de los sistemas y las redes, incluyendo la definición de **Zonas y Conductos** y los **Niveles de Seguridad (SL)**.
    * **Parte 4 (Requisitos de los Componentes)**: Define los requisitos de seguridad para los productos y componentes individuales, como PLCs y dispositivos de campo.

* **Aplicación en ICS**: Es el estándar técnico de referencia. Un plan de recuperación ante desastres (DRP) en un ICS debe basarse en las medidas de seguridad del estándar ISA/IEC 62443 para proteger los activos críticos y garantizar que la recuperación sea rápida y segura.

---

#### **Directiva NIS (Seguridad de las redes y sistemas de información)**

**Qué es**: La **Directiva NIS** (NIS Directive) es una ley de la Unión Europea que exige a los operadores de servicios esenciales y a los proveedores de servicios digitales que mejoren la seguridad de sus redes y sistemas de información. A diferencia de la ISO 31000 y el IEC 62443, la NIS es una regulación de obligado cumplimiento que establece las responsabilidades legales.

* **Puntos clave del marco legal**: La directiva especifica las obligaciones de seguridad en varios artículos:
    * **Artículo 14**: Establece los requisitos de seguridad que los operadores de servicios esenciales deben cumplir.
    * **Artículo 16**: Exige la notificación de incidentes graves a las autoridades competentes.

* **Aplicación en ICS**: La directiva obliga a los operadores a implementar medidas técnicas y organizativas adecuadas para gestionar los riesgos de seguridad y a informar de los incidentes graves. Esto hace que la planificación de la continuidad, la ciberseguridad y la respuesta a incidentes sean requisitos legales, lo que garantiza que los servicios esenciales puedan seguir funcionando a pesar de los ciberataques.

---

#### **ISO/IEC 27001 (Gestión de la Seguridad de la Información)**

**Qué es**: La **ISO/IEC 27001** es el estándar internacional para establecer, implementar, mantener y mejorar un **Sistema de Gestión de la Seguridad de la Información (SGSI)**. Su objetivo principal es ayudar a las organizaciones a proteger la **confidencialidad**, la **integridad** y la **disponibilidad** de su información.

* **Puntos clave del marco**: El estándar se centra en un enfoque basado en procesos de gestión de riesgos. Un SGSI incluye políticas, procedimientos, controles técnicos y organizativos para gestionar los riesgos de seguridad de la información. La norma no especifica qué controles técnicos se deben usar, sino que establece un marco para elegirlos y aplicarlos.

* **Aplicación en ICS**: La ISO 27001 es aplicable a los ICS porque los sistemas de control y los datos de los procesos son activos de información críticos. La **disponibilidad** es un pilar fundamental en OT y es uno de los tres objetivos de la seguridad de la información según el estándar. El marco de ISO 27001 complementa a la ISA/IEC 62443:
    * **ISO 27001** proporciona el marco de gestión de alto nivel para toda la organización (el "qué gestionar").
    * **ISA/IEC 62443** proporciona los controles técnicos y operativos detallados específicos para la tecnología de control industrial (el "cómo asegurar los sistemas OT").
