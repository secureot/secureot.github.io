---
title: "HART"
date: 2023-10-26
draft: false
weight: 1
---

### HART (Highway Addressable Remote Transducer)

El protocolo **HART** (Highway Addressable Remote Transducer) es un protocolo de red industrial que permite la **comunicación digital bidireccional** de información de dispositivos inteligentes, superpuesta sobre el estándar analógico tradicional de **4-20 mA**. 

#### Tecnología Híbrida 4-20 mA

HART es un protocolo de comunicación abierto y globalmente aceptado, diseñado para aplicaciones de medición y control de procesos. Su principal característica es su **naturaleza híbrida**, que le permite coexistir e integrarse en la infraestructura de automatización existente.

| Tipo de Señal | Uso | Tecnología |
| :--- | :--- | :--- |
| **Analógica (4-20 mA)** | Transmite la **variable principal** de control de forma continua. El valor de la corriente (4 a 20 mA) es directamente proporcional a la variable de proceso (ej., presión, temperatura). | Corriente eléctrica estándar. |
| **Digital** | Transmite datos secundarios, diagnóstico, estado del dispositivo, calibración y parámetros de configuración. Utiliza **FSK (Frequency Shift Keying)**, superponiendo la señal digital a la analógica sin interrumpirla. | Modulación FSK (1200 Hz y 2200 Hz). |

#### Modos de Comunicación y Estructura

El protocolo define las siguientes formas de interacción:

* **Maestro-Esclavo**: El modo de comunicación más común. Un dispositivo maestro (ej., DCS, PLC, configurador portátil) inicia la comunicación con un dispositivo esclavo (ej., transmisor, actuador).
* **Multidrop**: Permite que varios dispositivos esclavos se conecten al mismo par de cables, reduciendo el cableado.
* **Maestros Duales**: Permite la conexión de hasta dos dispositivos maestros (primario y secundario) al mismo lazo. El maestro primario suele ser el sistema de control (DCS/PLC) y el secundario un dispositivo de configuración o monitorización (*handheld*).

HART utiliza un conjunto de **Comandos** estructurados en tres clases para la interoperabilidad entre fabricantes:

* **Universales**: Comandos que todo dispositivo HART debe implementar (ej., leer variable primaria y unidades, identificar el dispositivo).
* **Práctica Común**: Comandos aplicables a muchos dispositivos (ej., cambiar rango, realizar autodiagnóstico).
* **Específicos del Dispositivo**: Comandos que solo son reconocidos por un tipo de dispositivo específico de un fabricante (ej., funciones avanzadas de diagnóstico).

#### Ventajas del Protocolo HART

* **Compatibilidad**: Utiliza el cableado analógico 4-20 mA ya instalado en la mayoría de las plantas, lo que facilita la migración a la comunicación digital.
* **Diagnóstico Avanzado**: Proporciona información de salud y estado de los instrumentos, permitiendo el mantenimiento predictivo y la optimización del rendimiento.
* **Interoperabilidad**: Al ser un estándar abierto (administrado por la HART Communication Foundation, HCF), asegura que los dispositivos de diferentes fabricantes funcionen juntos.
