+++
title = "Monitoreo modbus sobre TCP"
tags: ["Modbus", "Wireshark", "Industrial", "OT", "Ciberseguridad"]
+++

En esta guía te compartimos algunos **tips clave para analizar tráfico Modbus TCP** utilizando **Wireshark**, útil para diagnosticar problemas de comunicación o entender cómo funcionan los protocolos industriales.

---

## **1. Filtrar Tráfico Modbus TCP**

Modbus TCP utiliza el puerto **502** por defecto. Aquí algunos filtros útiles para enfocarte solo en este tráfico:

### **Filtros básicos**
- **Filtrar todo el tráfico Modbus TCP:**
  ```
  tcp.port == 502
  ```
