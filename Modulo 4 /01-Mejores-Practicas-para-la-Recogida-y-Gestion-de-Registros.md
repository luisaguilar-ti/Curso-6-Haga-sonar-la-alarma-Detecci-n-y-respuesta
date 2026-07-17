# 01. Mejores Prácticas para la Recogida y Gestión de Registros

## Descripción

Los registros (**logs**) son una de las fuentes de información más importantes durante una investigación de ciberseguridad. Permiten reconstruir eventos, identificar actividades sospechosas y comprender cómo ocurrió un incidente.

Una gestión adecuada de los registros mejora la capacidad de detección, facilita el análisis forense y ayuda a cumplir con los requisitos normativos de una organización.

---

# ¿Qué es un registro (Log)?

Un **registro (log)** es un archivo o conjunto de datos que almacena los eventos generados por sistemas, aplicaciones, dispositivos de red y herramientas de seguridad.

Cada evento registrado se denomina **entrada de registro (log entry)** y representa una acción específica ocurrida en un determinado momento.

Originalmente, los registros se utilizaban principalmente para solucionar problemas técnicos. Actualmente, constituyen una de las principales fuentes de información para el monitoreo de seguridad, la detección de amenazas y la respuesta ante incidentes.

---

# Importancia de los registros en Ciberseguridad

Los analistas utilizan los registros para:

- Detectar actividades sospechosas.
- Investigar incidentes de seguridad.
- Identificar ataques.
- Reconstruir la línea de tiempo de un incidente.
- Obtener evidencia digital.
- Cumplir con regulaciones y auditorías.

Las herramientas **SIEM** recopilan registros de múltiples fuentes y los centralizan para facilitar su análisis.

---

# Las cinco preguntas de una investigación (5W)

El análisis de registros ayuda a responder las cinco preguntas fundamentales de una investigación:

| Pregunta | Información obtenida |
|----------|----------------------|
| **Who? (¿Quién?)** | Usuario o dispositivo involucrado. |
| **What? (¿Qué?)** | Acción o evento ocurrido. |
| **When? (¿Cuándo?)** | Fecha y hora del evento. |
| **Where? (¿Dónde?)** | Sistema, aplicación o dispositivo afectado. |
| **Why? (¿Por qué?)** | Posible causa o motivo del incidente. |

---

# Tipos de registros

Dependiendo del origen de los datos, existen diferentes tipos de registros.

## 1. Registros de Red (Network Logs)

Son generados por dispositivos de red como:

- Firewalls
- Routers
- Switches
- IDS/IPS

Permiten analizar:

- Conexiones
- Direcciones IP
- Puertos
- Protocolos
- Tráfico de red

---

## 2. Registros del Sistema (System Logs)

Son creados por los sistemas operativos como:

- Windows
- Linux
- macOS
- ChromeOS

Incluyen información sobre:

- Inicio del sistema
- Errores
- Servicios
- Procesos
- Cambios de configuración

---

## 3. Registros de Aplicaciones (Application Logs)

Generados por aplicaciones y servicios.

Ejemplos:

- Servidores web
- Bases de datos
- Aplicaciones móviles
- Aplicaciones empresariales

Registran eventos específicos relacionados con el funcionamiento de cada aplicación.

---

## 4. Registros de Seguridad (Security Logs)

Generados por herramientas de seguridad como:

- Antivirus
- IDS
- IPS
- EDR
- Firewalls

Incluyen información relacionada con:

- Malware
- Eliminación de archivos
- Cambios de permisos
- Alertas de seguridad
- Ataques detectados

---

## 5. Registros de Autenticación (Authentication Logs)

Registran todos los procesos relacionados con la autenticación.

Por ejemplo:

- Inicio de sesión exitoso.
- Inicio de sesión fallido.
- Cambio de contraseña.
- Bloqueo de cuenta.
- Cierre de sesión.

---

# Información contenida en un registro

Generalmente un registro incluye:

- Fecha
- Hora
- Usuario
- Sistema
- Acción realizada
- Resultado del evento

Ejemplo:

```text
Login Event [05:45:15] User1 Authenticated successfully
```

---

# Registros Verbose

El **registro verbose** contiene información mucho más detallada que un registro normal.

Ejemplo:

```text
Login Event
[2022/11/16 05:45:15.892673]
auth_performer.cc:470
User1 Authenticated successfully
from device1 (192.168.1.2)
```

Los registros verbose permiten conocer información adicional como:

- Dirección IP
- Nombre del archivo
- Proceso responsable
- Marca temporal precisa
- Identificador del proceso

Aunque proporcionan más contexto, también generan un mayor volumen de información.

---

# Gestión de Registros (Log Management)

La **gestión de registros** es el proceso de:

1. Recopilar registros.
2. Almacenarlos.
3. Analizarlos.
4. Eliminarlos cuando finaliza su período de retención.

Una buena estrategia de gestión permite mantener únicamente la información necesaria para las operaciones y las investigaciones.

---

# ¿Qué registros deben almacenarse?

Cada organización debe decidir qué información registrar según:

- Riesgos existentes.
- Infraestructura.
- Requisitos legales.
- Necesidades operativas.
- Tipo de incidentes que desea detectar.

No todos los eventos requieren ser almacenados.

---

# Información Personal Identificable (PII)

Algunos registros pueden contener **Información Personal Identificable (PII)** como:

- Nombre completo.
- Correo electrónico.
- Número telefónico.
- Dirección.
- Identificaciones personales.

Dependiendo de la legislación aplicable, esta información puede requerir protección especial o incluso no poder registrarse.

---

# Overlogging

Uno de los errores más comunes es registrar absolutamente todo.

A esta práctica se le conoce como **Overlogging**.

## Desventajas

- Incrementa los costos de almacenamiento.
- Consume más recursos del sistema.
- Reduce el rendimiento.
- Dificulta encontrar eventos importantes.
- Incrementa el tiempo de investigación.

Registrar más información no siempre significa obtener mejores resultados.

---

# Retención de registros

Las organizaciones deben definir cuánto tiempo conservarán los registros.

Este período depende de:

- Políticas internas.
- Requisitos legales.
- Normativas del sector.

Algunos ejemplos son:

- **FISMA** (sector público)
- **HIPAA** (sector salud)
- **PCI DSS** (tarjetas de pago)
- **GLBA** (servicios financieros)
- **SOX** (Ley Sarbanes-Oxley)

---

# Protección de los registros

Los atacantes pueden intentar modificar o eliminar registros para ocultar sus actividades.

Por ello es importante proteger la integridad de los registros.

Una práctica recomendada consiste en almacenarlos en un **servidor centralizado**, evitando que permanezcan únicamente en los equipos donde fueron generados.

Entre sus ventajas se encuentran:

- Mayor integridad de la información.
- Dificulta la manipulación por parte de un atacante.
- Facilita las investigaciones.
- Centraliza el monitoreo.
- Simplifica el análisis mediante herramientas SIEM.

---

# Buenas prácticas para la gestión de registros

- Registrar únicamente la información necesaria.
- Definir políticas de retención.
- Proteger los registros contra modificaciones.
- Centralizar el almacenamiento.
- Revisar periódicamente la configuración de registro.
- Evitar el overlogging.
- Considerar los requisitos legales y regulatorios.
- Proteger la información sensible (PII).
- Utilizar herramientas SIEM para facilitar el análisis.

---

# Resumen

Los registros constituyen una de las principales fuentes de evidencia durante una investigación de ciberseguridad. Una estrategia adecuada de gestión de registros permite recopilar únicamente la información necesaria, proteger su integridad y conservarla durante el tiempo requerido por las políticas y regulaciones aplicables. Asimismo, el uso de almacenamiento centralizado y herramientas SIEM mejora la capacidad de detección, investigación y respuesta ante incidentes.

---

# Conceptos clave

- Registro (Log)
- Entrada de registro (Log Entry)
- Gestión de registros (Log Management)
- Análisis de registros (Log Analysis)
- Registros Verbose
- Registros de Red
- Registros del Sistema
- Registros de Aplicación
- Registros de Seguridad
- Registros de Autenticación
- Información Personal Identificable (PII)
- Overlogging
- Retención de registros
- Integridad de registros
- Servidor centralizado de registros
- SIEM
- Evidencia digital
- 5W de una investigación
