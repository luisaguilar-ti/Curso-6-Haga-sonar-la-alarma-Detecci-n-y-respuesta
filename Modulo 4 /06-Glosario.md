# 06. Glosario

## Introducción

Este glosario reúne los principales términos estudiados durante el Módulo 4. Conocer estos conceptos facilita la comprensión del funcionamiento de las herramientas SIEM, la gestión de registros y el análisis del tráfico de red mediante Suricata.

---

# A

## Análisis de registros (Log Analysis)

Proceso de examinar registros para identificar eventos, detectar actividades sospechosas y apoyar investigaciones de ciberseguridad.

---

# C

## Chronicle

Plataforma SIEM de Google, actualmente denominada **Google Security Operations**, utilizada para recopilar, normalizar y analizar registros de seguridad.

---

# E

## Entidad (Entity)

Elemento identificado dentro del modelo UDM, como un usuario, equipo, dirección IP o dispositivo involucrado en un evento.

## Event Metadata

Información general asociada a un evento, como el tipo de evento, fecha, hora y origen.

## eve.json

Archivo de registro en formato JSON generado por Suricata que contiene información detallada sobre los eventos detectados.

---

# F

## fast.log

Archivo de texto generado por Suricata que almacena un resumen de las alertas detectadas.

---

# I

## IDS (Intrusion Detection System)

Sistema de detección de intrusiones que supervisa el tráfico de red para identificar actividades sospechosas y generar alertas.

## IPS (Intrusion Prevention System)

Sistema de prevención de intrusiones que, además de detectar amenazas, puede bloquear o detener tráfico malicioso.

## Índice (Index)

Repositorio donde Splunk almacena los registros para facilitar su búsqueda mediante SPL.

## Ingestión de registros (Log Ingestion)

Proceso mediante el cual un SIEM recopila e incorpora registros provenientes de diferentes fuentes para su posterior análisis.

---

# J

## jq

Herramienta de línea de comandos utilizada para visualizar, filtrar y analizar archivos JSON.

---

# L

## Log

Registro generado por un sistema, aplicación o dispositivo que documenta un evento ocurrido.

## Log Entry

Cada evento individual contenido dentro de un registro.

## Log Forwarder

Software encargado de recopilar registros desde un dispositivo y enviarlos automáticamente a una plataforma SIEM.

## Log Management

Proceso de recopilar, almacenar, proteger, conservar y administrar registros.

---

# N

## Network Metadata

Información relacionada con la comunicación de red, como direcciones IP, puertos y protocolos.

## NSM (Network Security Monitoring)

Proceso de recopilar y analizar información del tráfico de red para detectar amenazas y apoyar investigaciones.

---

# O

## Overlogging

Práctica de registrar una cantidad excesiva de información, generando mayor consumo de recursos y dificultando el análisis.

---

# P

## Pipe

Símbolo (`|`) utilizado en Splunk para encadenar varios comandos dentro de una misma búsqueda.

## PII (Personally Identifiable Information)

Información Personal Identificable que puede utilizarse para identificar a una persona, como nombre, dirección o correo electrónico.

---

# R

## Raw Log Search

Método de búsqueda en Google Security Operations que consulta directamente los registros originales sin normalizar.

## Rule (Regla)

Conjunto de instrucciones utilizado por Suricata para identificar patrones específicos dentro del tráfico de red.

---

# S

## Security Results

Información sobre el resultado de un evento de seguridad, como malware detectado, archivos en cuarentena o amenazas bloqueadas.

## SIEM (Security Information and Event Management)

Plataforma que recopila, normaliza, correlaciona y analiza registros provenientes de múltiples fuentes para detectar amenazas.

## SPL (Search Processing Language)

Lenguaje de búsqueda utilizado por Splunk para consultar y analizar registros.

## Suricata

Herramienta de código abierto utilizada como IDS, IPS y plataforma de monitoreo de seguridad de red.

## suricata.yaml

Archivo principal de configuración de Suricata.

---

# U

## UDM (Unified Data Model)

Modelo de datos utilizado por Google Security Operations para normalizar registros antes de su análisis.

---

# W

## Wildcard

Carácter especial utilizado para representar uno o varios caracteres durante una búsqueda.
