---
title: "DB-9"
date: 2023-10-26
draft: false
weight: 1
---

### **Conector DB-9**

Un **conector DB-9** es un tipo de conector de la familia D-subminiatura, llamado así por su distintiva forma trapezoidal. Se utiliza comúnmente en la comunicación en serie para dispositivos y redes.

---

### **Aplicaciones de protocolos de comunicación**

El conector DB-9 se asocia a menudo con la comunicación serial, que transmite datos bit a bit. Dos de los protocolos más comunes que lo utilizan son **RS-232** y **RS-485**.

* **RS-232**: Este protocolo se usa para la comunicación **punto a punto** entre dos dispositivos. Sus principales características son la señalización no balanceada, que lo hace susceptible al ruido eléctrico, y una distancia de transmisión limitada a unos 15 metros. Es el protocolo principal en los **cables de consola** para la gestión de equipos de red.

* **RS-485**: Es un protocolo más robusto y se usa en entornos industriales. Sus ventajas son la señalización balanceada, que lo hace altamente resistente al ruido, y su capacidad **multi-punto**, que permite conectar hasta 32 dispositivos en un solo bus. Puede transmitir datos a distancias de hasta 1200 metros. Se usa para conectar múltiples PLCs, variadores de frecuencia y sensores a un sistema de control central.

---

### **Diagramas y configuración de pines**

#### **Configuración para RS-232**

El conector DB-9 se utiliza principalmente para el estándar **RS-232**, que define la función de cada pin.

| Fila superior | O | O | O | O | O |
| :---: | :---: | :---: | :---: | :---: | :---: |
| **Pines** | 1 | 2 | 3 | 4 | 5 |
| **Función** | DCD | RxD | TxD | DTR | GND |

| Fila inferior | O | O | O | O |
| :---: | :---: | :---: | :---: | :---: |
| **Pines** | 6 | 7 | 8 | 9 |
| **Función** | DSR | RTS | CTS | RI |

*El uso más básico de un cable de consola solo requiere tres pines: **RxD** (recepción), **TxD** (transmisión) y **GND** (tierra).*

#### **Configuración para RS-485**

El mismo conector físico DB-9 se puede usar para RS-485, pero con una asignación de pines diferente, aprovechando las líneas de datos balanceadas.

| Fila superior | O | O | O | O | O |
| :---: | :---: | :---: | :---: | :---: | :---: |
| **Pines** | 1 | 2 | 3 | 4 | 5 |
| **Función** | - | Datos A (-) | Datos B (+) | - | GND |

| Fila inferior | O | O | O | O |
| :---: | :---: | :---: | :---: | :---: |
| **Pines** | 6 | 7 | 8 | 9 |
| **Función** | - | - | - | - |
