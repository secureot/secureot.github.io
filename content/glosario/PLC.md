---
title: "PLC"
date: 2023-10-26
draft: false
weight: 1
---

### **Controlador Lógico Programable (PLC)**

Un **Controlador Lógico Programable (PLC)** es un ordenador industrial reforzado y especializado que se utiliza para controlar y automatizar procesos y maquinaria industriales. A diferencia de los ordenadores de escritorio, los PLCs están diseñados para operar de forma fiable en entornos industriales hostiles, resistiendo vibraciones, temperaturas extremas y ruido eléctrico.

---

#### **Componentes clave**

La arquitectura de un PLC se compone de varios módulos que trabajan juntos para controlar un proceso:

* **CPU (Unidad Central de Procesamiento)**: Es el "cerebro" del PLC. Ejecuta el programa de control que determina cómo se deben manejar las entradas para producir las salidas deseadas.
* **Módulos de Entrada/Salida (E/S)**: Estos módulos son la interfaz del PLC con el mundo físico.
    * **Módulos de entrada**: Reciben señales de sensores y dispositivos de campo, como botones, interruptores y termostatos.
    * **Módulos de salida**: Envían señales de control a actuadores y otros equipos, como motores, válvulas y luces piloto.
* **Memoria**: Almacena el programa de control, los datos del proceso y el estado de los módulos de E/S.
* **Fuente de alimentación**: Proporciona la energía necesaria para que el PLC funcione.

---

#### **Funcionamiento**

El funcionamiento de un PLC se basa en un ciclo de escaneo continuo y repetitivo, que generalmente se ejecuta cientos de veces por segundo. Este ciclo es determinista, lo que significa que el PLC ejecuta las tareas de control de forma predecible y en un tiempo predecible, algo fundamental en la automatización industrial.

El ciclo de escaneo de un PLC consta de los siguientes pasos:

1.  **Lectura de Entradas**: El PLC lee el estado actual de todos sus módulos de entrada, registrando la información en su memoria interna.
2.  **Ejecución del Programa**: La CPU ejecuta el programa de control paso a paso, tomando decisiones lógicas y cálculos basados en la información de entrada leída en el paso anterior.
3.  **Actualización de Salidas**: El PLC actualiza el estado de sus módulos de salida en función de los resultados de la ejecución del programa.
4.  **Mantenimiento Interno**: El PLC realiza tareas de autodiagnóstico y comunicación, asegurándose de que todos los componentes funcionen correctamente.

**Ejemplo de uso**: Un PLC en una cinta transportadora está programado para detener el motor cuando un sensor detecta un objeto en el final de la línea. El PLC lee la entrada del sensor y, si detecta la presencia del objeto, envía una señal de salida al motor para que se apague.

---

### **Diagrama de ciclo de escaneo de un PLC**

```mermaid
graph TD
    A[Inicio de ciclo];
    B(Leer Entradas);
    C{Ejecutar Programa};
    D(Actualizar Salidas);
    E[Fin de ciclo/Inicio de nuevo ciclo];

    A --> B;
    B --> C;
    C --> D;
    D --> E;
