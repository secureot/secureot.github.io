---
title: "HMI"
date: 2023-10-26
draft: false
weight: 1
---

### **Interfaz Humano-Máquina (HMI)**

Una **Interfaz Humano-Máquina (HMI)** es un dispositivo o software que proporciona una interfaz gráfica de usuario para que los operadores monitoricen y controlen los procesos industriales. Las HMI, que se clasifican como dispositivos de **Nivel 2** en la arquitectura de Purdue, actúan como un puente entre la maquinaria del proceso (Nivel 0 y 1) y el operador humano, mostrando datos en tiempo real y permitiendo la interacción con el sistema.

---

#### **Componentes y funcionamiento**

La HMI no controla directamente el proceso; en su lugar, se comunica con los **Controladores Lógicos Programables (PLCs)** y los sistemas **SCADA**. Su funcionamiento se basa en las siguientes funciones principales:

* **Visualización de datos**: Muestra los datos del proceso en un formato fácil de entender, como gráficos, medidores o diagramas de flujo.
* **Control del proceso**: Permite a los operadores enviar comandos a los PLCs o RTUs, como iniciar o detener un motor, abrir una válvula o ajustar un punto de ajuste.
* **Alarmas y eventos**: Notifica a los operadores sobre eventos críticos o fallos en el proceso.
* **Informes y registros**: Registra los datos del proceso para su análisis histórico y la generación de informes.

---

#### **Tipos de HMI y ejemplos**

Existen diferentes tipos de HMI, desde paneles de control simples hasta software complejo para estaciones de trabajo.

1.  **HMI de Siemens**: Siemens ofrece una amplia gama de HMI bajo su marca **SIMATIC**. Un ejemplo es la serie **SIMATIC HMI KTP**, que son paneles táctiles compactos que se utilizan para el control de máquinas locales. Se comunican con los PLCs de Siemens a través de redes como PROFINET.
2.  **HMI de código abierto**: Hay opciones de HMI de código abierto que son populares en el ámbito industrial. Por ejemplo, **Ignition** de Inductive Automation ofrece una versión de código abierto que se puede utilizar para construir sistemas SCADA y HMI.
3.  **HMI basadas en la nube**: Con la convergencia de la IT y la OT, han surgido HMI basadas en la nube que permiten a los operadores monitorizar los procesos desde cualquier lugar. Estas soluciones se comunican con los dispositivos de campo a través de la nube y se pueden acceder desde un navegador web o una aplicación móvil.

**Ejemplo de uso**: Un operador en una sala de control utiliza una HMI para monitorizar la temperatura de un reactor químico. Si la temperatura excede el límite de seguridad, la HMI muestra una alarma y el operador puede enviar un comando para activar el sistema de enfriamiento del reactor.

---

### **Diagrama de un sistema con HMI**

A continuación, se muestra un diagrama simple en formato Mermaid que ilustra el papel de la HMI en un sistema de control.

```mermaid
graph TD
    A[PLC/Controlador] -->|Envía datos| B[Servidor SCADA];
    B -->|Visualización| C[HMI del Operador];
    C -->|Comandos| B;
    B -->|Actualiza estado| A;
