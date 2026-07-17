# 04. Panorama de Suricata

## Descripción

**Suricata** es una herramienta de código abierto utilizada para el monitoreo de seguridad de red y la detección de amenazas. Puede funcionar como **Sistema de Detección de Intrusiones (IDS)**, **Sistema de Prevención de Intrusiones (IPS)** y como una plataforma de **Monitoreo de Seguridad de Red (NSM)**.

Su principal función es inspeccionar el tráfico de red en tiempo real utilizando un conjunto de reglas (firmas) para identificar actividades sospechosas y generar registros que faciliten el análisis de incidentes.

---

# ¿Qué es Suricata?

Suricata es un motor de análisis de tráfico de red desarrollado por la **Open Information Security Foundation (OISF)**.

Permite inspeccionar paquetes de red para:

- Detectar ataques.
- Identificar comportamientos sospechosos.
- Generar alertas.
- Registrar eventos de seguridad.
- Analizar tráfico de red.

Su funcionamiento se basa en un conjunto de **reglas (rules)** que describen qué tipo de actividad debe detectarse.

---

# Funciones principales de Suricata

Suricata puede desempeñar tres funciones principales.

## Sistema de Detección de Intrusiones (IDS)

Como **Intrusion Detection System (IDS)**, Suricata supervisa el tráfico de red y genera alertas cuando detecta una actividad que coincide con alguna de sus reglas.

En este modo únicamente detecta y registra eventos; no modifica el tráfico.

---

## Sistema de Prevención de Intrusiones (IPS)

Como **Intrusion Prevention System (IPS)**, además de detectar actividades sospechosas, puede actuar sobre el tráfico de red para impedir que determinadas comunicaciones continúen.

---

## Monitoreo de Seguridad de Red (NSM)

El **Network Security Monitoring (NSM)** consiste en recopilar, registrar y analizar información sobre el tráfico de red con el objetivo de detectar amenazas y apoyar investigaciones de seguridad.

Suricata genera registros detallados que permiten reconstruir eventos y analizar incidentes posteriormente.

---

# Reglas (Rules)

Las reglas son el mecanismo mediante el cual Suricata identifica actividades específicas dentro del tráfico de red.

Cada regla describe un patrón que debe buscarse en los paquetes analizados.

Cuando una comunicación coincide con una regla, Suricata ejecuta la acción definida y registra el evento.

---

# Componentes de una regla

Una regla de Suricata está formada por tres elementos principales.

## 1. Acción (Action)

Indica qué debe hacer Suricata cuando una regla coincide con el tráfico analizado.

En el curso se utiliza la acción:

- **alert** → Genera una alerta cuando se detecta una coincidencia.

---

## 2. Encabezado (Header)

Define las características generales del tráfico que será inspeccionado.

Puede incluir información como:

- Protocolo.
- Dirección IP de origen.
- Dirección IP de destino.
- Puerto de origen.
- Puerto de destino.
- Dirección del flujo de comunicación.

---

## 3. Opciones de la regla (Rule Options)

Las opciones contienen información adicional utilizada para identificar el tráfico y describir la alerta generada.

Entre ellas pueden encontrarse:

- Mensaje descriptivo.
- Identificador de la regla.
- Contenido que debe buscarse.
- Información adicional utilizada durante la detección.

---

# Orden de las reglas

Suricata analiza las reglas siguiendo el orden en que se encuentran cargadas.

Una organización adecuada de las reglas facilita:

- El mantenimiento.
- La administración.
- La identificación de conflictos.
- La actualización de firmas.

---

# Reglas personalizadas

Además de utilizar conjuntos de reglas existentes, Suricata permite crear reglas personalizadas adaptadas a las necesidades de una organización.

Estas reglas pueden utilizarse para detectar:

- Actividades internas.
- Comportamientos específicos.
- Aplicaciones propias.
- Patrones particulares de la red.

---

# Archivo de configuración

La configuración principal de Suricata se almacena en el archivo:

```text
suricata.yaml
```

Este archivo controla diferentes aspectos del funcionamiento de la herramienta, como:

- Interfaces de red.
- Ubicación de reglas.
- Configuración de registros.
- Opciones de ejecución.

---

# Archivos de registro

Cuando Suricata analiza tráfico de red genera diferentes archivos de registro.

Los estudiados en este módulo son:

---

## fast.log

Es un registro en formato de texto que contiene un resumen de las alertas generadas.

Cada línea representa una alerta detectada y facilita una revisión rápida de los eventos.

---

## eve.json

Es el principal archivo de registro de Suricata.

Se encuentra en formato **JSON** y almacena información detallada sobre los eventos generados durante el análisis del tráfico.

Este formato facilita su procesamiento mediante herramientas de análisis y plataformas SIEM.

---

# Uso de jq

Durante el laboratorio se utiliza la herramienta **jq** para visualizar y analizar el contenido del archivo **eve.json**.

Al trabajar con archivos JSON, jq permite mostrar la información de forma más legible y facilitar su inspección.

---

# Flujo general de funcionamiento

El funcionamiento básico de Suricata puede resumirse en los siguientes pasos:

1. Captura el tráfico de red.
2. Analiza los paquetes.
3. Compara el tráfico con las reglas configuradas.
4. Detecta coincidencias.
5. Genera alertas.
6. Almacena los eventos en archivos de registro.

---

# Integración con SIEM

Los registros generados por Suricata pueden enviarse a plataformas SIEM para:

- Centralizar la información.
- Correlacionar eventos.
- Detectar amenazas.
- Facilitar investigaciones.
- Generar alertas automatizadas.

Esta integración permite combinar la información de Suricata con registros provenientes de otras fuentes.

---

# Buenas prácticas

- Mantener actualizadas las reglas de detección.
- Revisar periódicamente la configuración de Suricata.
- Analizar de forma continua los archivos de registro.
- Utilizar reglas personalizadas cuando sea necesario.
- Integrar los registros con una plataforma SIEM para mejorar el monitoreo.
- Verificar el funcionamiento de las reglas después de realizar cambios.

---

# Resumen

Suricata es una herramienta de código abierto utilizada para detectar, registrar y analizar actividades de red. Puede operar como IDS, IPS y plataforma de monitoreo de seguridad de red. Su funcionamiento se basa en reglas que permiten identificar patrones específicos dentro del tráfico, generando registros como **fast.log** y **eve.json**, los cuales constituyen una fuente importante de información durante las investigaciones de ciberseguridad.

---

# Conceptos clave

- Suricata
- IDS
- IPS
- NSM
- Reglas (Rules)
- Acción (Action)
- Encabezado (Header)
- Opciones de regla (Rule Options)
- Reglas personalizadas
- suricata.yaml
- fast.log
- eve.json
- JSON
- jq
- Firma (Signature)
- Alerta
- Análisis de tráfico de red
