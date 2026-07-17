# Módulo 3: Detección de Incidentes y Respuesta

## Descripción

En este módulo se estudian los procesos, metodologías y herramientas utilizadas para detectar, investigar y responder a incidentes de ciberseguridad. Se exploran técnicas como **Threat Hunting**, **Threat Intelligence**, el análisis de **Indicadores de Compromiso (IoC)** e **Indicadores de Ataque (IoA)**, el proceso de **triaje**, la **continuidad del negocio** y las actividades posteriores a un incidente.

Además, se presentan herramientas ampliamente utilizadas por los analistas SOC, como **VirusTotal**, junto con buenas prácticas de documentación y metodologías para fortalecer la capacidad de respuesta de una organización.

---

# Objetivos de aprendizaje

Al finalizar este módulo serás capaz de:

- Comprender los principales métodos de detección de incidentes.
- Explicar el funcionamiento del Threat Hunting y Threat Intelligence.
- Diferenciar entre IoC e IoA.
- Interpretar la Pirámide del Dolor.
- Analizar indicadores utilizando herramientas de investigación.
- Comprender el proceso de triaje de incidentes.
- Aplicar buenas prácticas de documentación.
- Comprender la importancia de la continuidad del negocio.
- Analizar las actividades posteriores a un incidente.
- Elaborar documentación útil para investigaciones de seguridad.

---

# 📚 Contenido del módulo

| Estado | Documento | Descripción |
|:---:|---|---|
| ⬜ | [01 - Métodos de Detección de Incidentes](01-Metodos-de-Deteccion-de-Incidentes.md) | IDS, SIEM, Threat Hunting, Threat Intelligence, TIP, Honeypots y métodos modernos de detección. |
| ⬜ | [02 - Indicadores de Compromiso e Indicadores de Ataque](02-Indicadores-de-Compromiso-e-Indicadores-de-Ataque.md) | IoC, IoA, Pirámide del Dolor, TTP y análisis de indicadores. |
| ⬜ | [03 - Herramientas de Investigación y VirusTotal](03-Herramientas-de-Investigacion-y-VirusTotal.md) | VirusTotal, OSINT, Crowdsourcing, MalwareBazaar, Jotti y Urlscan.io. |
| ⬜ | [04 - Buenas Prácticas de Documentación](04-Buenas-Practicas-de-Documentacion.md) | Transparencia, cadena de custodia, estandarización y documentación eficaz. |
| ⬜ | [05 - Proceso de Triaje](05-Proceso-de-Triaje.md) | Evaluación, priorización e investigación de alertas e incidentes. |
| ⬜ | [06 - Continuidad del Negocio y Recuperación](06-Continuidad-del-Negocio-y-Recuperacion.md) | Business Continuity Plan (BCP), resiliencia y estrategias de recuperación. |
| ⬜ | [07 - Actividad Posterior al Incidente](07-Actividad-Posterior-al-Incidente.md) | Lessons Learned, recomendaciones e informe final del incidente. |
| ⬜ | [08 - Resumen del Módulo](08-Resumen-del-Modulo.md) | Resumen de todos los conceptos estudiados. |
| ⬜ | [09 - Glosario](09-Glosario.md) | Definiciones de los términos más importantes del módulo. |
| ⬜ | [10 - Preguntas de Repaso](10-Preguntas-de-Repaso.md) | Preguntas para reforzar el aprendizaje. |
| ⬜ | [11 - Preguntas de Entrevista](11-Preguntas-de-Entrevista.md) | Preguntas frecuentes para entrevistas de SOC Analyst, Blue Team e Incident Response. |

---

# 🧪 Laboratorios

| Estado | Laboratorio | Objetivo |
|:---:|---|---|
| ⬜ | [README](labs/README.md) | Introducción a las prácticas del módulo. |
| ⬜ | [Lab 01 - Análisis de IoC con VirusTotal](labs/Lab-01-Analisis-de-IoC-con-VirusTotal.md) | Investigar indicadores de compromiso utilizando VirusTotal. |
| ⬜ | [Lab 02 - Investigación con OSINT](labs/Lab-02-Investigacion-con-OSINT.md) | Obtener inteligencia mediante fuentes abiertas. |
| ⬜ | [Lab 03 - Proceso de Triaje](labs/Lab-03-Proceso-de-Triaje.md) | Analizar, clasificar y priorizar alertas de seguridad. |
| ⬜ | [Lab 04 - Documentación de un Incidente](labs/Lab-04-Documentacion-de-un-Incidente.md) | Elaborar la documentación completa de un incidente de seguridad. |

---

# 🛠️ Herramientas estudiadas

- IDS (Intrusion Detection System)
- SIEM (Security Information and Event Management)
- VirusTotal
- MalwareBazaar
- Urlscan.io
- Jotti Malware Scan
- Threat Intelligence Platforms (TIP)

---

# 📖 Conceptos principales

- Detección
- Análisis
- Threat Hunting
- Threat Intelligence
- Threat Intelligence Platform (TIP)
- Indicadores de Compromiso (IoC)
- Indicadores de Ataque (IoA)
- Pirámide del Dolor
- OSINT
- Crowdsourcing
- Honeypots
- Triaje
- Cadena de Custodia
- Business Continuity Plan (BCP)
- Resiliencia
- Lessons Learned
- Informe Final

---

# 📂 Estructura del módulo

```text
Modulo-3/
│
├── README.md
│
├── 01-Metodos-de-Deteccion-de-Incidentes.md
├── 02-Indicadores-de-Compromiso-e-Indicadores-de-Ataque.md
├── 03-Herramientas-de-Investigacion-y-VirusTotal.md
├── 04-Buenas-Practicas-de-Documentacion.md
├── 05-Proceso-de-Triaje.md
├── 06-Continuidad-del-Negocio-y-Recuperacion.md
├── 07-Actividad-Posterior-al-Incidente.md
├── 08-Resumen-del-Modulo.md
├── 09-Glosario.md
├── 10-Preguntas-de-Repaso.md
├── 11-Preguntas-de-Entrevista.md
│
├── labs/
│   ├── README.md
│   ├── Lab-01-Analisis-de-IoC-con-VirusTotal.md
│   ├── Lab-02-Investigacion-con-OSINT.md
│   ├── Lab-03-Proceso-de-Triaje.md
│   └── Lab-04-Documentacion-de-un-Incidente.md
│
└── assets/
    └── README.md
```

---

# 📚 Recursos recomendados

- NIST SP 800-61 Computer Security Incident Handling Guide
- MITRE ATT&CK Framework
- MITRE D3FEND
- VirusTotal
- MalwareBazaar
- Urlscan.io

---

# 🎯 Conclusión

Este módulo desarrolla las competencias necesarias para detectar, investigar y responder a incidentes de seguridad utilizando metodologías, herramientas y buenas prácticas empleadas por equipos **SOC**, **Blue Team** e **Incident Response**. Los conocimientos adquiridos servirán como base para comprender procesos avanzados de investigación y fortalecer la capacidad de respuesta ante amenazas dentro de una organización.
