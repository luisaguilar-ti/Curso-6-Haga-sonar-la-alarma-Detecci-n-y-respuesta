# 05. Resumen del Módulo

## Introducción

En este módulo se estudió la importancia de los registros (**logs**) como una de las principales fuentes de información utilizadas durante las investigaciones de ciberseguridad. También se analizaron las mejores prácticas para gestionar, proteger y conservar los registros, así como el funcionamiento de las plataformas **SIEM** para recopilar, normalizar y analizar grandes volúmenes de datos.

Además, se conoció el funcionamiento básico de **Suricata**, una herramienta de código abierto utilizada para la detección y el monitoreo de amenazas en redes, incluyendo la estructura de sus reglas y los principales archivos de registro que genera.

---

# 1. Gestión de registros

Los registros permiten documentar las actividades realizadas por usuarios, aplicaciones, dispositivos y sistemas.

Durante una investigación ayudan a responder preguntas como:

- ¿Quién realizó la acción?
- ¿Qué ocurrió?
- ¿Cuándo sucedió?
- ¿Dónde ocurrió?
- ¿Por qué pudo haber sucedido?

También se estudiaron los principales tipos de registros:

- Registros de red
- Registros del sistema
- Registros de aplicaciones
- Registros de seguridad
- Registros de autenticación

Una adecuada gestión de registros implica:

- Recopilar únicamente la información necesaria.
- Definir políticas de retención.
- Evitar el overlogging.
- Proteger la integridad de los registros.
- Centralizar el almacenamiento cuando sea posible.

---

# 2. Fuentes de registro e ingestión de registros

Las plataformas SIEM recopilan información proveniente de múltiples fuentes de datos.

El proceso de ingestión de registros incluye tres etapas principales:

1. Recopilar los registros.
2. Normalizar los datos.
3. Analizarlos para detectar actividades sospechosas.

Para automatizar este proceso se utilizan **Log Forwarders**, encargados de enviar los registros desde los dispositivos hacia la plataforma SIEM.

---

# 3. Métodos de búsqueda en herramientas SIEM

Se estudiaron dos plataformas ampliamente utilizadas:

## Splunk

Utiliza el lenguaje **SPL (Search Processing Language)** para realizar búsquedas dentro de los registros.

Entre sus principales características destacan:

- Índices (Indexes)
- Pipes (`|`)
- Wildcards (`*`)
- Búsquedas exactas

---

## Google Security Operations (Chronicle)

Chronicle utiliza el **Unified Data Model (UDM)** para normalizar los registros antes de realizar búsquedas.

También permite realizar:

- UDM Search
- Raw Log Search

Estas herramientas facilitan la investigación de incidentes y la correlación de eventos.

---

# 4. Suricata

Suricata es una herramienta de código abierto utilizada para:

- Detectar intrusiones (IDS).
- Prevenir intrusiones (IPS).
- Monitorear la seguridad de la red (NSM).

Su funcionamiento se basa en reglas (firmas) que analizan el tráfico de red para identificar patrones específicos.

Una regla de Suricata está formada por:

- Acción.
- Encabezado.
- Opciones.

La configuración principal se almacena en el archivo:

- `suricata.yaml`

Los principales archivos de registro estudiados fueron:

- `fast.log`
- `eve.json`

Durante el laboratorio también se utilizó la herramienta **jq** para visualizar y analizar archivos JSON.

---

# Conceptos más importantes

- Logs
- Log Entry
- Log Management
- Log Analysis
- Log Sources
- Log Ingestion
- Log Forwarder
- SIEM
- SPL
- UDM
- Raw Log Search
- Wildcards
- Suricata
- IDS
- IPS
- NSM
- Rules
- suricata.yaml
- fast.log
- eve.json
- jq

---

# Laboratorio realizado

En este módulo se desarrolló un laboratorio oficial donde se aprendió a:

- Ejecutar Suricata sobre un archivo de captura de red.
- Crear y utilizar reglas personalizadas.
- Analizar las alertas generadas.
- Examinar los archivos **fast.log** y **eve.json**.
- Interpretar los resultados obtenidos.

---

# Conclusión

Los registros constituyen la base de cualquier investigación de seguridad. Comprender cómo se generan, recopilan y analizan permite detectar amenazas con mayor rapidez y obtener evidencia útil durante un incidente. Asimismo, el conocimiento de plataformas SIEM y herramientas como Suricata proporciona las bases necesarias para monitorear redes, analizar eventos y responder de manera más eficiente ante posibles ataques.
