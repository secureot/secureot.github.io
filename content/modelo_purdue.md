+++
title = "Modelo Purdue"
+++


El **Modelo Purdue** es un marco arquitectónico utilizado en sistemas de automatización y control industrial. Desarrollado por la Universidad de Purdue, se utiliza para estructurar la comunicación y el control en entornos industriales, además de proporcionar un enfoque para la ciberseguridad.

## Estructura del Modelo Purdue

El modelo está organizado en cinco niveles jerárquicos, cada uno con funciones y tecnologías específicas:

| **Nivel** | **Descripción**                                                                                                                                                            | **Ejemplos de Tecnologías**                           |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **0** | **Proceso**: Involucra los dispositivos de campo que interactúan directamente con el entorno.                                                                           | Sensores, Actuadores, Controladores de Movimiento     |
| **1** | **Control**: Se encarga del control y la automatización mediante dispositivos que ejecutan instrucciones.                                                                  | PLCs (Controladores Lógicos Programables), DCS        |
| **2** | **Supervisión**: Proporciona interfaces de usuario y monitoreo del proceso en tiempo real.                                                                                | HMI (Interfaz Hombre-Máquina), SCADA                  |
| **3** | **Operaciones del Sitio**: Se centra en la gestión de la producción y el almacenamiento de datos para el análisis y la optimización.                                     | Sistemas de Gestión de Producción, Historian de Datos |
| **4** | **Gestión Empresarial**: Se ocupa de la integración de los sistemas de gestión empresarial con las operaciones industriales.                                                | ERP (Planificación de Recursos Empresariales), CRM     |

## Propósitos y Beneficios del Modelo Purdue

### 1. **Seguridad Cibernética**
   - **Segmentación de Redes**: El modelo promueve la segmentación de la red industrial para proteger los sistemas de control de amenazas externas e internas.
   - **Controles de Acceso**: Facilita la implementación de controles de acceso robustos en cada nivel.

### 2. **Interoperabilidad**
   - **Integración de Sistemas**: Permite la interoperabilidad entre diferentes tecnologías y sistemas, facilitando la comunicación entre dispositivos y aplicaciones.

### 3. **Estandarización**
   - **Mejora de la Eficiencia**: Al proporcionar una estructura clara, se facilita la implementación y el mantenimiento de sistemas de control industrial.
   - **Facilita el Cumplimiento Normativo**: Ayuda a las organizaciones a cumplir con normas y estándares industriales.

## Consideraciones Técnicas

- **Protocolo de Comunicación**: Utiliza protocolos estándar de la industria, como **Modbus**, **PROFIBUS**, **OPC** y **Ethernet/IP**, para la comunicación entre dispositivos.
- **Ciberseguridad**: La implementación de medidas de seguridad, como firewalls y sistemas de detección de intrusos, es fundamental para proteger cada nivel del modelo.
- **Mantenimiento y Actualizaciones**: Se deben establecer procedimientos de mantenimiento y actualizaciones regulares para los sistemas a lo largo de todos los niveles, asegurando la continuidad operacional.

