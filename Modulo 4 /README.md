# Módulo 4: Tráfico de Red, Registros y Herramientas SIEM

## Descripción

En este módulo se profundiza en la recopilación, gestión y análisis de registros (logs), una de las principales fuentes de información durante una investigación de ciberseguridad. También se estudia el funcionamiento de las herramientas **SIEM (Security Information and Event Management)**, los métodos de búsqueda utilizados para analizar grandes volúmenes de datos y el sistema de detección de intrusiones **Suricata**, incluyendo la creación y análisis de reglas, así como la interpretación de sus registros.

Además, se realiza un laboratorio práctico utilizando Suricata para comprender cómo se generan alertas y cómo analizar los archivos de registro producidos por esta herramienta.

---

# 🎯 Objetivos

Al finalizar este módulo serás capaz de:

- Comprender la importancia de los registros en una investigación de seguridad.
- Identificar los diferentes tipos de registros utilizados en una organización.
- Aplicar buenas prácticas para la gestión, retención y protección de registros.
- Comprender el proceso de ingestión de registros en una plataforma SIEM.
- Diferenciar los métodos de búsqueda utilizados en Splunk y Google Security Operations (Chronicle).
- Comprender el funcionamiento de Suricata como IDS, IPS y herramienta de monitoreo de seguridad de red.
- Analizar los archivos de registro generados por Suricata.
- Interpretar reglas (firmas) utilizadas para detectar actividad maliciosa.

---

# 📚 Contenido del módulo

| Estado | Tema | Descripción |
|---------|------|-------------|
| ⬜ | [01 - Mejores Prácticas para la Recogida y Gestión de Registros](01-Mejores-Practicas-para-la-Recogida-y-Gestion-de-Registros.md) | Importancia de los registros, tipos de logs, gestión, retención y protección de registros. |
| ⬜ | [02 - Fuentes de Registro e Ingestión de Registros](02-Fuentes-de-Registro-e-Ingestion-de-Registros.md) | Funcionamiento de la ingestión de registros y recopilación de datos en herramientas SIEM. |
| ⬜ | [03 - Métodos de Búsqueda con Herramientas SIEM](03-Metodos-de-Busqueda-con-Herramientas-SIEM.md) | Métodos de búsqueda en Splunk y Google Security Operations (Chronicle). |
| ⬜ | [04 - Panorama de Suricata](04-Panorama-de-Suricata.md) | Introducción a Suricata, reglas, archivos de configuración y registros generados. |
| ⬜ | [05 - Resumen del Módulo](05-Resumen-del-Modulo.md) | Resumen de los conceptos más importantes del módulo. |
| ⬜ | [06 - Glosario](06-Glosario.md) | Definiciones de los términos técnicos estudiados en el módulo. |
| ⬜ | [07 - Preguntas de Repaso](07-Preguntas-de-Repaso.md) | Preguntas para reforzar los conocimientos adquiridos. |
| ⬜ | [08 - Preguntas de Entrevista](08-Preguntas-de-Entrevista.md) | Preguntas frecuentes de entrevistas relacionadas con registros, SIEM y Suricata. |

---

# 🧪 Laboratorios

> **Nota:** El siguiente laboratorio corresponde a una práctica oficial del curso.

| Estado | Laboratorio | Objetivo |
|---------|-------------|----------|
| ⬜ | [README](labs/README.md) | Información general sobre los laboratorios del módulo. |
| ⬜ | [Lab 01 - Suricata: Reglas y Registros](labs/Lab-01-Suricata-Reglas-y-Registros.md) | Configurar reglas en Suricata, generar alertas y analizar los archivos **fast.log** y **eve.json**. |

---

# 🛠️ Herramientas estudiadas

- SIEM (Security Information and Event Management)
- Splunk
- Google Security Operations (Chronicle)
- Suricata
- jq
- YAML
- JSON

---

# 📖 Conceptos principales

- Logs
- Log Management
- Log Analysis
- Ingestión de registros
- SIEM
- SPL (Search Processing Language)
- UDM Search
- Raw Log Search
- Suricata
- IDS
- IPS
- NSM (Network Security Monitoring)
- Firmas (Rules)
- Archivos de configuración
- eve.json
- fast.log
- Telemetría
- Overlogging
- Retención de registros
- PII (Información Personal Identificable)

---

# 📂 Estructura del módulo

```text
Modulo-4/
│
├── README.md
├── 01-Mejores-Practicas-para-la-Recogida-y-Gestion-de-Registros.md
├── 02-Fuentes-de-Registro-e-Ingestion-de-Registros.md
├── 03-Metodos-de-Busqueda-con-Herramientas-SIEM.md
├── 04-Panorama-de-Suricata.md
├── 05-Resumen-del-Modulo.md
├── 06-Glosario.md
├── 07-Preguntas-de-Repaso.md
├── 08-Preguntas-de-Entrevista.md
│
├── assets/
│
└── labs/
    ├── README.md
    └── Lab-01-Suricata-Reglas-y-Registros.md
```

---

# 📚 Recursos recomendados

## Documentación oficial

- Suricata User Guide
- Suricata Rules Documentation
- Splunk Search Reference
- Google Security Operations Documentation
- MITRE ATT&CK Framework

---

# 🎯 Conclusión

La recopilación y el análisis de registros constituyen una parte esencial de las operaciones de seguridad modernas. En este módulo se estudian las mejores prácticas para gestionar registros, el funcionamiento de las plataformas SIEM y el uso de Suricata para detectar y analizar actividades sospechosas. Estos conocimientos proporcionan una base sólida para realizar investigaciones de incidentes, monitorear redes y responder de manera eficiente ante amenazas de ciberseguridad.
