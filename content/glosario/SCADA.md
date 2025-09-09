---
title: "SCADA"
date: 2023-10-26
draft: false
weight: 1
---

### **Sistemas SCADA (Supervisory Control and Data Acquisition)**

Un sistema **SCADA** es una arquitectura de software y hardware que se utiliza para monitorizar y controlar procesos industriales de forma remota. A diferencia de los sistemas de control distribuido (DCS), un sistema SCADA proporciona una visión de alto nivel del proceso.

#### **Componentes clave**

La arquitectura SCADA integra varios componentes:

* **Sensores y actuadores**: Dispositivos de campo que miden y controlan variables del proceso, como la temperatura, la presión o el flujo.
* **PLCs (Controladores Lógicos Programables) y RTUs (Unidades de Terminal Remota)**: Ordenadores industriales que recogen datos de los sensores y envían comandos a los actuadores, controlando directamente la maquinaria y los procesos.
* **Servidor SCADA (Estación maestra)**: Un potente ordenador que recopila, procesa y almacena los datos de los PLCs y RTUs, actuando como el centro de control del sistema.
* **HMI (Interfaz Humano-Máquina)**: Una interfaz gráfica que permite a los operadores visualizar los datos del proceso en tiempo real, recibir alarmas si algo falla y enviar comandos.
* **Red de comunicación**: La infraestructura que conecta los dispositivos de campo con el servidor SCADA, a menudo utilizando protocolos industriales como DNP3 o Modbus.

#### **Funcionamiento**

El funcionamiento de un sistema SCADA se basa en un ciclo continuo de recopilación, procesamiento y visualización de datos:

1.  Los **sensores** miden variables del proceso y envían los datos a los **PLCs** o **RTUs**.
2.  Los **PLCs** y **RTUs** ejecutan las instrucciones de control programadas localmente y envían los datos a la estación maestra a través de la red de comunicación.
3.  El **servidor SCADA** recopila los datos de todos los dispositivos y los presenta de forma clara en la **HMI**.
4.  Desde la **HMI**, el operador puede monitorizar el estado del proceso, recibir alarmas y enviar comandos al sistema.

**Ejemplo de uso**: En una planta de energía, un sistema SCADA monitoriza los generadores, las turbinas y los transformadores. Si se detecta una anomalía en un transformador, el sistema genera una alarma en la HMI, y el operador puede enviar un comando para desconectarlo de forma remota.

---

### **Diagrama de arquitectura SCADA**

Aquí tienes un diagrama simple en formato Mermaid que ilustra la arquitectura de un sistema SCADA, mostrando la conexión entre sus diferentes componentes.

```mermaid
graph TD
    subgraph "Proceso Industrial"
        P1[Sensores] --> PLC1(PLC/RTU);
        PLC1 --> A1[Actuadores];
        P2[Sensores] --> PLC2(PLC/RTU);
        PLC2 --> A2[Actuadores];
    end

    subgraph "Red de Comunicación"
        PLC1 -- Protocolos Industriales --> Servidor(Servidor SCADA);
        PLC2 -- Protocolos Industriales --> Servidor;
    end

    subgraph "Centro de Control"
        Servidor --> HMI(HMI del Operador);
        HMI --> Servidor;
    end
