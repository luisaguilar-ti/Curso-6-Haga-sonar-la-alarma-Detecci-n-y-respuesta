# Curso 6 - Sound the Alarm: Detection and Response
# Módulo 1 - Fundamentos de la Detección y Respuesta a Incidentes

> **Curso:** Google Cybersecurity Professional Certificate  
> **Módulo:** 1 - Fundamentos de la Detección y Respuesta  
> **Objetivo:** Comprender cómo las organizaciones detectan, investigan y responden a incidentes de seguridad utilizando procesos, equipos y herramientas especializadas.

---

# Objetivos de aprendizaje

Al finalizar este módulo serás capaz de:

- Comprender qué es un incidente de seguridad.
- Diferenciar un evento de un incidente.
- Entender el ciclo de vida de respuesta a incidentes propuesto por NIST.
- Identificar el papel de un analista SOC.
- Comprender cómo funcionan las herramientas SIEM, SOAR, IDS, IPS y EDR.
- Conocer el flujo básico de detección y respuesta dentro de un Centro de Operaciones de Seguridad.

---

# ¿Qué es la respuesta a incidentes?

La **Respuesta a Incidentes (Incident Response, IR)** es el conjunto de procesos utilizados para identificar, investigar, contener, erradicar y recuperar una organización después de un incidente de ciberseguridad.

Su objetivo principal es reducir el impacto del incidente y restaurar las operaciones de forma segura en el menor tiempo posible.

No todos los eventos representan un incidente. Un analista debe determinar si un evento corresponde a una actividad normal o si representa una amenaza real.

---

## Evento vs Incidente

| Evento | Incidente |
|---------|-----------|
| Cualquier acción registrada en un sistema. | Evento que compromete la confidencialidad, integridad o disponibilidad de la información. |
| Puede ser completamente normal. | Requiere investigación y respuesta. |
| Ocurre constantemente. | Es una situación excepcional. |

### Ejemplo

**Evento**

```text
Usuario inicia sesión a las 08:15.
```

No representa ningún problema.

**Incidente**

```text
El mismo usuario intenta iniciar sesión 2,000 veces desde tres países diferentes en cinco minutos.
```

Esto requiere una investigación inmediata.

---

# Objetivos de la respuesta a incidentes

Toda organización busca:

- Detectar amenazas rápidamente.
- Minimizar el daño.
- Proteger la información.
- Restaurar los servicios.
- Evitar que el incidente vuelva a ocurrir.
- Documentar todo el proceso.

---

# Flujo general de respuesta a incidentes

```text
Actividad en la red
        │
        ▼
Generación de eventos
        │
        ▼
Recolección de logs
        │
        ▼
SIEM
        │
        ▼
Generación de alertas
        │
        ▼
Analista SOC
        │
        ▼
Investigación
        │
        ▼
Contención
        │
        ▼
Erradicación
        │
        ▼
Recuperación
```

---

# El Centro de Operaciones de Seguridad (SOC)

Un **Security Operations Center (SOC)** es el equipo responsable de supervisar continuamente la infraestructura tecnológica de una organización.

Su misión consiste en detectar amenazas, investigar incidentes y coordinar la respuesta para minimizar riesgos.

Un SOC opera las 24 horas del día en muchas organizaciones.

## Funciones principales

- Supervisar eventos de seguridad.
- Analizar alertas.
- Investigar actividades sospechosas.
- Coordinar la respuesta a incidentes.
- Mantener herramientas de monitoreo.
- Elaborar informes.

---

# Roles comunes dentro de un SOC

| Rol | Función |
|------|----------|
| Analista SOC Nivel 1 | Monitoreo inicial y clasificación de alertas. |
| Analista SOC Nivel 2 | Investigación profunda de incidentes. |
| Analista SOC Nivel 3 | Amenazas avanzadas y malware. |
| Incident Responder | Coordina la respuesta técnica. |
| Threat Hunter | Busca amenazas que aún no han generado alertas. |
| SOC Manager | Coordina el equipo y define procesos. |

---

# Conceptos importantes

## Detección

Proceso mediante el cual se identifica una posible amenaza.

Puede realizarse mediante:

- SIEM
- IDS
- IPS
- EDR
- Antivirus
- Reglas personalizadas

---

## Análisis

Consiste en determinar si la alerta representa realmente un incidente.

Durante esta etapa el analista responde preguntas como:

- ¿Qué ocurrió?
- ¿Cuándo ocurrió?
- ¿Quién fue afectado?
- ¿Cuál es el alcance?
- ¿Es un falso positivo?

---

## Contención

Busca impedir que el incidente continúe propagándose.

Ejemplos:

- Aislar un equipo.
- Bloquear una IP.
- Deshabilitar una cuenta.
- Cortar una conexión de red.

---

## Erradicación

Elimina completamente la causa del incidente.

Ejemplos:

- Eliminar malware.
- Corregir vulnerabilidades.
- Aplicar parches.
- Restablecer credenciales.

---

## Recuperación

Consiste en restaurar los servicios afectados y verificar que el incidente no vuelva a aparecer.

Ejemplos:

- Restaurar respaldos.
- Reincorporar servidores.
- Validar funcionamiento.
- Supervisar nuevamente el sistema.

---

# Resumen

En este módulo aprendiste:

- La diferencia entre un evento y un incidente.
- Qué es la respuesta a incidentes.
- El propósito de un SOC.
- Los roles principales de un equipo de seguridad.
- El flujo general desde la detección hasta la recuperación.

---

## Próximo tema

En la siguiente parte del módulo profundizaremos en las herramientas utilizadas por un SOC:

- SIEM
- SOAR
- IDS
- IPS
- EDR

Analizaremos cómo funcionan, cuándo se utilizan y cómo trabajan juntas durante un incidente.
