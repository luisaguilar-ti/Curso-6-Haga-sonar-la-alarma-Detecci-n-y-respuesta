# Métodos de Detección de Incidentes

## Introducción

La detección de incidentes es una de las funciones más importantes dentro de un Centro de Operaciones de Seguridad (SOC). Consiste en identificar actividades anómalas o maliciosas que puedan comprometer la confidencialidad, integridad o disponibilidad de los sistemas de una organización.

Detectar un incidente de forma temprana permite reducir el impacto del ataque, disminuir el tiempo de respuesta y evitar que una amenaza continúe propagándose por la infraestructura.

---

# ¿Qué es un método de detección?

Un método de detección es cualquier proceso, tecnología o técnica utilizada para identificar eventos que puedan representar un incidente de seguridad.

La detección puede realizarse de forma:

- Automática
- Manual
- Proactiva
- Reactiva

Generalmente las organizaciones utilizan varias técnicas al mismo tiempo para aumentar la probabilidad de detectar amenazas.

---

# Principales métodos de detección

## Intrusion Detection System (IDS)

Un **IDS (Intrusion Detection System)** supervisa continuamente el tráfico de red o la actividad de un sistema para identificar comportamientos sospechosos.

Su función principal es:

- Detectar amenazas.
- Generar alertas.
- Notificar al equipo de seguridad.

Un IDS **no bloquea** el ataque; únicamente informa que existe una posible actividad maliciosa.

### Ventajas

- Detecta comportamientos sospechosos.
- Genera evidencia para investigaciones.
- Puede detectar ataques conocidos.

### Limitaciones

- No impide el ataque.
- Puede generar falsos positivos.
- Requiere mantenimiento constante.

---

## Security Information and Event Management (SIEM)

Un SIEM centraliza los registros (logs) generados por diferentes dispositivos y aplicaciones de la organización.

Posteriormente:

- Correlaciona eventos.
- Detecta patrones.
- Genera alertas.
- Facilita investigaciones.

Los SIEM ayudan a los analistas SOC a identificar incidentes que serían difíciles de detectar revisando registros manualmente.

---

## Threat Hunting

El **Threat Hunting** consiste en buscar amenazas de manera proactiva.

En lugar de esperar una alerta automática, el analista investiga la infraestructura para encontrar evidencia de actividades maliciosas que hayan pasado desapercibidas.

Este proceso requiere:

- Hipótesis de investigación.
- Conocimiento de amenazas.
- Análisis de registros.
- Experiencia del analista.

---

## Threat Intelligence

La inteligencia de amenazas consiste en recopilar, analizar y compartir información sobre amenazas actuales.

Su objetivo es comprender:

- Quién ataca.
- Cómo atacan.
- Qué herramientas utilizan.
- Qué organizaciones pueden verse afectadas.

La información obtenida ayuda a fortalecer las defensas antes de que ocurra un incidente.

---

## Threat Intelligence Platform (TIP)

Una **Threat Intelligence Platform (TIP)** centraliza información procedente de múltiples fuentes de inteligencia.

Permite:

- Organizar indicadores.
- Correlacionar amenazas.
- Compartir inteligencia.
- Priorizar riesgos.

Las TIP facilitan el trabajo diario de los equipos SOC.

---

## Honeypots

Un **Honeypot** es un sistema diseñado para atraer atacantes.

Su propósito no es proteger información real, sino observar el comportamiento del atacante y obtener inteligencia sobre nuevas técnicas.

Los honeypots permiten:

- Estudiar ataques.
- Obtener indicadores de compromiso.
- Descubrir herramientas utilizadas por los atacantes.

---

## Cyber Deception

La **Cyber Deception** amplía el concepto de los honeypots.

Consiste en desplegar recursos falsos dentro de la infraestructura para engañar al atacante.

Algunos ejemplos son:

- Servidores falsos.
- Credenciales falsas.
- Bases de datos falsas.
- Documentos señuelo.

Cuando un atacante interactúa con alguno de estos recursos, el equipo de seguridad recibe una alerta inmediata.

---

# Comparación de los métodos de detección

| Método | Función principal |
|----------|------------------|
| IDS | Detectar actividades sospechosas. |
| SIEM | Correlacionar eventos y generar alertas. |
| Threat Hunting | Buscar amenazas de forma proactiva. |
| Threat Intelligence | Obtener información sobre amenazas. |
| TIP | Administrar inteligencia de amenazas. |
| Honeypot | Atraer atacantes para estudiarlos. |
| Cyber Deception | Engañar atacantes mediante recursos falsos. |

---

# Buenas prácticas

- Utilizar varias técnicas de detección al mismo tiempo.
- Correlacionar eventos provenientes de distintas fuentes.
- Actualizar constantemente las reglas de detección.
- Validar las alertas antes de responder.
- Documentar todos los hallazgos durante la investigación.

---

# Resumen

La detección de incidentes combina herramientas automáticas y procesos de análisis humano para identificar amenazas antes de que provoquen daños significativos. Tecnologías como los IDS y los SIEM, junto con estrategias como el Threat Hunting, Threat Intelligence y Cyber Deception, permiten mejorar significativamente la capacidad de respuesta de una organización.

---

# Conceptos clave

- IDS
- SIEM
- Threat Hunting
- Threat Intelligence
- Threat Intelligence Platform (TIP)
- Honeypot
- Cyber Deception
- Detección de incidentes

---

> **Siguiente tema:** [02 - Indicadores de Compromiso e Indicadores de Ataque](02-Indicadores-de-Compromiso-e-Indicadores-de-Ataque.md)
