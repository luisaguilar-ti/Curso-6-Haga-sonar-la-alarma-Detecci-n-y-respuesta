# 07. Preguntas de Repaso

## Introducción

Las siguientes preguntas tienen como objetivo reforzar los conceptos estudiados durante el módulo. Se recomienda intentar responderlas antes de consultar las respuestas para evaluar el nivel de comprensión de los temas.

---

# Gestión de registros

### 1. ¿Qué es un registro (log)?

<details>
<summary>Ver respuesta</summary>

Un registro es un archivo o conjunto de datos que almacena eventos generados por sistemas, aplicaciones o dispositivos durante su funcionamiento.

</details>

---

### 2. ¿Qué información suele contener una entrada de registro?

<details>
<summary>Ver respuesta</summary>

Generalmente incluye la fecha, hora, usuario, sistema, acción realizada y el resultado del evento.

</details>

---

### 3. ¿Cuáles son los cinco tipos principales de registros estudiados en este módulo?

<details>
<summary>Ver respuesta</summary>

- Registros de red.
- Registros del sistema.
- Registros de aplicaciones.
- Registros de seguridad.
- Registros de autenticación.

</details>

---

### 4. ¿Qué significa el término "Overlogging"?

<details>
<summary>Ver respuesta</summary>

Es la práctica de registrar una cantidad excesiva de información, lo que aumenta el consumo de recursos y dificulta el análisis de eventos importantes.

</details>

---

### 5. ¿Por qué es importante proteger los registros?

<details>
<summary>Ver respuesta</summary>

Porque pueden utilizarse como evidencia durante una investigación y los atacantes podrían intentar modificarlos o eliminarlos para ocultar sus actividades.

</details>

---

# SIEM e ingestión de registros

### 6. ¿Qué es la ingestión de registros?

<details>
<summary>Ver respuesta</summary>

Es el proceso mediante el cual una plataforma SIEM recopila registros provenientes de diferentes fuentes para analizarlos posteriormente.

</details>

---

### 7. ¿Cuáles son las tres etapas principales del procesamiento de registros en un SIEM?

<details>
<summary>Ver respuesta</summary>

1. Recopilación.
2. Normalización.
3. Análisis.

</details>

---

### 8. ¿Qué función cumple un Log Forwarder?

<details>
<summary>Ver respuesta</summary>

Recopila automáticamente los registros desde un dispositivo y los envía hacia una plataforma SIEM.

</details>

---

### 9. ¿Por qué es importante normalizar los registros?

<details>
<summary>Ver respuesta</summary>

Porque permite convertir registros de diferentes formatos a una estructura común, facilitando su análisis y correlación.

</details>

---

# Métodos de búsqueda

### 10. ¿Qué significa SPL?

<details>
<summary>Ver respuesta</summary>

Search Processing Language, el lenguaje de búsqueda utilizado por Splunk.

</details>

---

### 11. ¿Qué es un índice (Index) en Splunk?

<details>
<summary>Ver respuesta</summary>

Es el repositorio donde Splunk almacena los registros para que posteriormente puedan consultarse.

</details>

---

### 12. ¿Para qué sirve el operador Pipe (`|`) en Splunk?

<details>
<summary>Ver respuesta</summary>

Permite encadenar varios comandos dentro de una misma consulta, utilizando el resultado de un comando como entrada del siguiente.

</details>

---

### 13. ¿Qué función cumple un Wildcard?

<details>
<summary>Ver respuesta</summary>

Representa uno o varios caracteres para ampliar el alcance de una búsqueda.

</details>

---

### 14. ¿Cuál es el método de búsqueda principal de Google Security Operations?

<details>
<summary>Ver respuesta</summary>

La búsqueda UDM (Unified Data Model).

</details>

---

### 15. ¿Qué diferencia existe entre una búsqueda UDM y una Raw Log Search?

<details>
<summary>Ver respuesta</summary>

La búsqueda UDM trabaja con registros previamente normalizados, mientras que la Raw Log Search consulta directamente los registros originales.

</details>

---

# Suricata

### 16. ¿Qué es Suricata?

<details>
<summary>Ver respuesta</summary>

Es una herramienta de código abierto utilizada para la detección de intrusiones, prevención de intrusiones y monitoreo de seguridad de red.

</details>

---

### 17. ¿Qué significan las siglas IDS?

<details>
<summary>Ver respuesta</summary>

Intrusion Detection System (Sistema de Detección de Intrusiones).

</details>

---

### 18. ¿Qué significan las siglas IPS?

<details>
<summary>Ver respuesta</summary>

Intrusion Prevention System (Sistema de Prevención de Intrusiones).

</details>

---

### 19. ¿Cuáles son las tres partes principales de una regla de Suricata?

<details>
<summary>Ver respuesta</summary>

- Acción.
- Encabezado.
- Opciones de la regla.

</details>

---

### 20. ¿Cuál es el archivo principal de configuración de Suricata?

<details>
<summary>Ver respuesta</summary>

`suricata.yaml`

</details>

---

### 21. ¿Qué información contiene el archivo `fast.log`?

<details>
<summary>Ver respuesta</summary>

Un resumen en formato de texto de las alertas generadas por Suricata.

</details>

---

### 22. ¿Qué información contiene el archivo `eve.json`?

<details>
<summary>Ver respuesta</summary>

Información detallada de los eventos detectados por Suricata en formato JSON.

</details>

---

### 23. ¿Para qué se utiliza la herramienta `jq`?

<details>
<summary>Ver respuesta</summary>

Para visualizar, filtrar y analizar archivos JSON desde la línea de comandos.

</details>

---

# Autoevaluación

Si puedes responder correctamente la mayoría de estas preguntas sin consultar las respuestas, significa que dominas los conceptos fundamentales del módulo y estás preparado para continuar con los siguientes temas del curso.
