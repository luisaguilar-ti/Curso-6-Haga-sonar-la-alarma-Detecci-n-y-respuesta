# Preguntas de Entrevista

## 1. ¿Qué es un Indicador de Compromiso (IoC) y en qué se diferencia de un Indicador de Ataque (IoA)?

**Respuesta:**

Un **Indicador de Compromiso (IoC)** es una evidencia que indica que un sistema ya pudo haber sido comprometido, como un hash malicioso, una dirección IP sospechosa o un dominio utilizado por un atacante.

Un **Indicador de Ataque (IoA)** describe comportamientos sospechosos que pueden indicar que un ataque está ocurriendo o está por ocurrir, incluso antes de que exista un compromiso confirmado.

---

## 2. ¿Qué herramientas utilizarías para investigar un archivo sospechoso?

**Respuesta:**

Dependiendo del caso utilizaría herramientas como:

- VirusTotal
- MalwareBazaar
- Jotti Malware Scan

Estas permiten analizar el archivo mediante múltiples motores antivirus, consultar su reputación y obtener información adicional sobre posibles amenazas.

---

## 3. ¿Qué información puede proporcionar VirusTotal durante una investigación?

**Respuesta:**

VirusTotal permite consultar:

- Hashes
- Archivos
- Direcciones IP
- Dominios
- URL

Además proporciona:

- Resultados de múltiples motores antivirus.
- Relaciones entre indicadores.
- Información histórica.
- Inteligencia compartida por la comunidad.

---

## 4. ¿Qué es OSINT y por qué es importante?

**Respuesta:**

OSINT (Open Source Intelligence) consiste en recopilar información utilizando fuentes públicas como sitios web, registros DNS, WHOIS, blogs especializados y repositorios públicos.

Es importante porque permite enriquecer una investigación sin necesidad de acceder a información privada.

---

## 5. ¿Cuál es el propósito de documentar un incidente de seguridad?

**Respuesta:**

La documentación permite:

- Registrar todas las acciones realizadas.
- Mantener una cronología del incidente.
- Facilitar investigaciones futuras.
- Compartir información con otros analistas.
- Cumplir requisitos legales y regulatorios.

---

## 6. ¿Qué es la Cadena de Custodia?

**Respuesta:**

La Cadena de Custodia es el proceso que garantiza la integridad de una evidencia digital documentando quién la obtuvo, quién tuvo acceso a ella, dónde fue almacenada y cualquier transferencia realizada.

Es fundamental cuando la evidencia puede utilizarse en auditorías o procesos legales.

---

## 7. ¿Qué es el proceso de triaje en un SOC?

**Respuesta:**

El triaje es el proceso mediante el cual las alertas de seguridad son evaluadas, clasificadas y priorizadas para determinar cuáles requieren atención inmediata.

Su objetivo es optimizar los recursos del SOC y responder primero a los incidentes de mayor impacto.

---

## 8. ¿Qué factores considerarías para priorizar un incidente?

**Respuesta:**

Entre los factores más importantes se encuentran:

- Impacto sobre el negocio.
- Criticidad del sistema afectado.
- Sensibilidad de la información.
- Alcance del incidente.
- Riesgo para la organización.
- Probabilidad de explotación.

---

## 9. ¿Cuál es la diferencia entre Business Continuity y Disaster Recovery?

**Respuesta:**

**Business Continuity** busca mantener operativas las funciones críticas del negocio durante una interrupción.

**Disaster Recovery** se enfoca en restaurar la infraestructura tecnológica y los sistemas afectados después del incidente.

---

## 10. ¿Qué importancia tienen los respaldos (backups) en la respuesta a incidentes?

**Respuesta:**

Los respaldos permiten recuperar información y restaurar sistemas después de un incidente como ransomware, fallas de hardware o errores humanos.

Deben realizarse periódicamente y probarse para asegurar que puedan restaurarse correctamente.

---

## 11. ¿Qué es un Root Cause Analysis (RCA)?

**Respuesta:**

Es un proceso utilizado para identificar la causa principal que permitió que ocurriera un incidente.

Su objetivo es eliminar el problema desde su origen y evitar que vuelva a repetirse.

---

## 12. ¿Qué ocurre durante una Post-Incident Review (PIR)?

**Respuesta:**

Durante una Post-Incident Review el equipo analiza:

- Qué ocurrió.
- Cómo ocurrió.
- Qué acciones funcionaron correctamente.
- Qué procedimientos deben mejorarse.
- Qué lecciones fueron aprendidas.

Esta revisión fortalece la capacidad de respuesta de la organización.

---

## 13. ¿Qué buenas prácticas seguirías al investigar un incidente?

**Respuesta:**

- Documentar todas las acciones realizadas.
- Validar la información utilizando varias fuentes.
- Conservar la evidencia digital.
- Mantener la cadena de custodia.
- Seguir procedimientos establecidos.
- Compartir información relevante con el equipo.

---

## 14. ¿Qué beneficios aporta una revisión posterior al incidente?

**Respuesta:**

Permite:

- Detectar oportunidades de mejora.
- Actualizar procedimientos.
- Implementar nuevos controles de seguridad.
- Capacitar al personal.
- Reducir la probabilidad de incidentes futuros.

---

## 15. Como analista SOC, recibes una alerta por una conexión sospechosa desde una dirección IP desconocida. ¿Qué harías?

**Respuesta:**

Seguiría un proceso estructurado:

1. Validar la alerta para descartar un falso positivo.
2. Revisar los registros (logs) relacionados.
3. Investigar la dirección IP utilizando herramientas como VirusTotal u otras fuentes de inteligencia.
4. Buscar Indicadores de Compromiso (IoC) e Indicadores de Ataque (IoA).
5. Evaluar el impacto y la criticidad del sistema afectado.
6. Priorizar el incidente según el riesgo.
7. Documentar todas las acciones realizadas.
8. Escalar el incidente si es necesario.
9. Participar en la revisión posterior al incidente para identificar mejoras.
