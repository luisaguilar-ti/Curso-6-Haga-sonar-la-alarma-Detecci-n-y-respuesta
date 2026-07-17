# Proceso de Triaje

## Introducción

El **triaje (Triage)** es el proceso mediante el cual un equipo de seguridad evalúa, clasifica y prioriza los incidentes detectados para determinar cuáles requieren atención inmediata y cuáles pueden atenderse posteriormente.

Debido a que un Centro de Operaciones de Seguridad (SOC) puede recibir cientos o incluso miles de alertas al día, el triaje permite administrar eficientemente los recursos disponibles y concentrar los esfuerzos en los incidentes de mayor impacto para la organización.

---

# ¿Qué es el Triaje?

El triaje consiste en analizar la información inicial de una alerta para determinar:

- Si realmente existe un incidente.
- La gravedad del incidente.
- Los sistemas afectados.
- El impacto potencial.
- La prioridad de respuesta.

El objetivo es responder primero a los incidentes más críticos y reducir el riesgo para la organización.

---

# Objetivos del Triaje

El proceso de triaje busca:

- Validar las alertas recibidas.
- Identificar falsos positivos.
- Priorizar incidentes.
- Asignar recursos de manera eficiente.
- Reducir el tiempo de respuesta.
- Minimizar el impacto de un incidente.

---

# Etapas del Proceso de Triaje

## 1. Recepción de la alerta

El proceso comienza cuando una herramienta de seguridad detecta una actividad sospechosa.

Las alertas pueden provenir de:

- SIEM
- IDS
- Antivirus
- EDR
- Firewalls
- Usuarios
- Sistemas de monitoreo

---

## 2. Validación

El analista revisa la información disponible para determinar si la alerta corresponde a una amenaza real o a un falso positivo.

Durante esta etapa se analizan:

- Registros (logs).
- Indicadores de compromiso (IoC).
- Indicadores de ataque (IoA).
- Eventos relacionados.

---

## 3. Clasificación

Una vez validada la alerta, se clasifica según el tipo de incidente.

Ejemplos:

- Malware.
- Phishing.
- Acceso no autorizado.
- Exfiltración de datos.
- Ataque de fuerza bruta.
- Denegación de servicio.

---

## 4. Priorización

No todos los incidentes representan el mismo riesgo.

Para establecer la prioridad normalmente se consideran factores como:

- Impacto en el negocio.
- Criticidad del sistema afectado.
- Sensibilidad de la información.
- Alcance del incidente.
- Probabilidad de explotación.

---

## 5. Escalamiento

Si el incidente supera las responsabilidades del analista inicial, debe escalarse al equipo correspondiente.

Dependiendo del caso puede intervenir:

- Equipo SOC.
- Incident Response Team.
- Administradores de sistemas.
- Equipo legal.
- Dirección.

---

# Factores para priorizar un incidente

Algunas preguntas utilizadas durante el triaje son:

- ¿Qué activo fue afectado?
- ¿Es un sistema crítico?
- ¿La amenaza continúa activa?
- ¿Existe riesgo para la organización?
- ¿Hay evidencia de compromiso?
- ¿El incidente afecta a varios equipos?

---

# Beneficios del Triaje

Aplicar correctamente el proceso de triaje permite:

- Reducir tiempos de respuesta.
- Evitar la saturación del equipo SOC.
- Atender primero los incidentes más críticos.
- Optimizar recursos.
- Mejorar la toma de decisiones.

---

# Buenas prácticas

- Validar toda alerta antes de actuar.
- Utilizar procedimientos estandarizados.
- Documentar todas las decisiones tomadas.
- Priorizar según el riesgo para el negocio.
- Escalar oportunamente cuando sea necesario.
- Revisar continuamente la información disponible durante la investigación.

---

# Errores comunes

- Asumir que todas las alertas son incidentes.
- Ignorar posibles falsos positivos.
- Priorizar únicamente por cantidad de alertas.
- No documentar las decisiones.
- Retrasar el escalamiento de incidentes críticos.

---

# Resumen

El triaje es un proceso fundamental dentro de la respuesta a incidentes, ya que permite evaluar y priorizar las alertas recibidas para asignar adecuadamente los recursos del equipo de seguridad. Una correcta validación, clasificación y priorización contribuyen a reducir el impacto de los incidentes y mejorar la eficiencia del SOC.

---

# Conceptos clave

- Triaje
- Alerta
- Clasificación
- Priorización
- Escalamiento
- Falso positivo
- Impacto
- Riesgo
- Incidente
- SOC

---

> **Siguiente tema:** [06 - Continuidad del Negocio y Recuperación](06-Continuidad-del-Negocio-y-Recuperacion.md)
