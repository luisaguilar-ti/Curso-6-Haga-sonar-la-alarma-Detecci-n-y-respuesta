# 08. Preguntas de Entrevista

## Introducción

Las siguientes preguntas son similares a las que pueden realizarse durante una entrevista para un puesto de **SOC Analyst**, **Cybersecurity Analyst**, **Blue Team Analyst** o cualquier rol relacionado con la supervisión de eventos de seguridad y la respuesta a incidentes.

El objetivo es ayudarte a explicar los conceptos con tus propias palabras y prepararte para entrevistas técnicas.

---

# Preguntas básicas

## 1. ¿Qué es un log y por qué es importante en ciberseguridad?

**Respuesta esperada:**

Un log es un registro que almacena eventos generados por sistemas, aplicaciones o dispositivos. Es importante porque proporciona evidencia de las actividades realizadas, permite detectar incidentes, investigar ataques y reconstruir la secuencia de eventos ocurridos.

---

## 2. ¿Qué tipos de registros conoces?

**Respuesta esperada:**

Los principales tipos de registros son:

- Registros de red.
- Registros del sistema.
- Registros de aplicaciones.
- Registros de seguridad.
- Registros de autenticación.

Cada uno proporciona información diferente para las investigaciones.

---

## 3. ¿Qué es el overlogging?

**Respuesta esperada:**

Es la práctica de registrar una cantidad excesiva de información. Esto incrementa el consumo de almacenamiento, dificulta el análisis y puede afectar el rendimiento de los sistemas.

---

## 4. ¿Qué es una plataforma SIEM?

**Respuesta esperada:**

Es una plataforma que recopila, centraliza, normaliza y analiza registros provenientes de múltiples fuentes para detectar amenazas, correlacionar eventos y facilitar las investigaciones de seguridad.

---

## 5. ¿Cuál es el proceso básico que sigue un SIEM?

**Respuesta esperada:**

El proceso generalmente consiste en:

1. Recopilar registros.
2. Normalizarlos.
3. Analizarlos.
4. Correlacionar eventos.
5. Generar alertas cuando se detectan actividades sospechosas.

---

## 6. ¿Qué es un Log Forwarder?

**Respuesta esperada:**

Es un software encargado de recopilar registros desde un sistema o dispositivo y enviarlos automáticamente hacia una plataforma SIEM.

---

## 7. ¿Por qué es importante la normalización de registros?

**Respuesta esperada:**

Porque permite convertir registros provenientes de diferentes fabricantes y formatos en una estructura común, facilitando las búsquedas, el análisis y la correlación de eventos.

---

# Splunk y Google Security Operations

## 8. ¿Qué es SPL?

**Respuesta esperada:**

SPL (Search Processing Language) es el lenguaje de consultas utilizado por Splunk para buscar, filtrar y analizar registros.

---

## 9. ¿Qué función cumple un índice en Splunk?

**Respuesta esperada:**

Un índice es el repositorio donde Splunk almacena los registros para que posteriormente puedan consultarse mediante SPL.

---

## 10. ¿Para qué sirve el operador Pipe (`|`) en Splunk?

**Respuesta esperada:**

Permite encadenar varios comandos dentro de una misma búsqueda, utilizando el resultado de un comando como entrada para el siguiente.

---

## 11. ¿Qué diferencia existe entre UDM Search y Raw Log Search?

**Respuesta esperada:**

UDM Search consulta registros previamente normalizados, mientras que Raw Log Search trabaja directamente sobre los registros originales sin normalizar.

---

# Suricata

## 12. ¿Qué es Suricata?

**Respuesta esperada:**

Es una herramienta de código abierto utilizada para analizar tráfico de red y detectar actividades sospechosas. Puede funcionar como IDS, IPS y herramienta de monitoreo de seguridad de red.

---

## 13. ¿Qué diferencia existe entre un IDS y un IPS?

**Respuesta esperada:**

- Un **IDS** detecta actividades sospechosas y genera alertas.
- Un **IPS** además puede bloquear o impedir el tráfico considerado malicioso.

---

## 14. ¿Cómo funciona Suricata?

**Respuesta esperada:**

Suricata inspecciona el tráfico de red y lo compara con un conjunto de reglas (firmas). Cuando detecta una coincidencia, ejecuta la acción definida y registra el evento correspondiente.

---

## 15. ¿Cuáles son las partes principales de una regla de Suricata?

**Respuesta esperada:**

Una regla está compuesta por:

- Acción.
- Encabezado.
- Opciones de la regla.

---

## 16. ¿Qué archivo contiene la configuración principal de Suricata?

**Respuesta esperada:**

El archivo `suricata.yaml`.

---

## 17. ¿Qué diferencia existe entre `fast.log` y `eve.json`?

**Respuesta esperada:**

- **fast.log** contiene un resumen de las alertas en formato de texto.
- **eve.json** almacena información mucho más detallada en formato JSON.

---

## 18. ¿Para qué sirve la herramienta `jq`?

**Respuesta esperada:**

Permite visualizar, filtrar y analizar archivos JSON desde la línea de comandos, facilitando la inspección de registros generados por Suricata.

---

# Pregunta de razonamiento

## 19. Un analista recibe una alerta de actividad sospechosa. ¿Cómo utilizaría un SIEM para investigarla?

**Respuesta esperada:**

Buscaría los registros relacionados con el evento utilizando filtros adecuados, revisaría la información normalizada, correlacionaría eventos provenientes de diferentes fuentes, identificaría la línea de tiempo del incidente y recopilaría evidencia para determinar el alcance y el impacto de la actividad detectada.

---

# Consejos para la entrevista

- Explica los conceptos con tus propias palabras.
- Relaciona las respuestas con situaciones reales de monitoreo e investigación.
- Diferencia claramente los conceptos de **detección**, **prevención**, **registro** y **análisis**.
- Si mencionas una herramienta como Splunk o Suricata, explica cuál es su función dentro de un entorno de seguridad.
- Cuando sea posible, utiliza ejemplos sencillos para demostrar que comprendes el flujo completo de una investigación.

---

# Objetivo

Si puedes responder estas preguntas sin consultar las respuestas, tendrás una base sólida sobre los conceptos de gestión de registros, plataformas SIEM y Suricata estudiados en este módulo, lo que te ayudará tanto en evaluaciones técnicas como en entrevistas para puestos de nivel inicial en ciberseguridad.
