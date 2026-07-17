# NIST Incident Response Lifecycle

Uno de los marcos de trabajo más utilizados para responder a incidentes de seguridad fue desarrollado por el **National Institute of Standards and Technology (NIST)**.

Su objetivo es proporcionar una metodología estructurada para preparar a una organización antes, durante y después de un incidente.

El ciclo consta de cuatro fases principales.

---

# Fase 1 - Preparación (Preparation)

La preparación consiste en implementar controles, herramientas y procedimientos antes de que ocurra un incidente.

Una organización preparada responde mucho más rápido y reduce considerablemente el impacto de un ataque.

## Actividades principales

- Crear políticas de seguridad.
- Elaborar el Plan de Respuesta a Incidentes (IRP).
- Capacitar al personal.
- Configurar herramientas SIEM, IDS, IPS y EDR.
- Definir roles y responsabilidades.
- Realizar simulacros.

---

# Fase 2 - Detección y Análisis (Detection and Analysis)

En esta fase se identifica una posible amenaza y se determina si realmente se trata de un incidente.

Las herramientas de monitoreo generan alertas que son investigadas por el equipo de seguridad.

## Actividades principales

- Monitorear eventos.
- Analizar logs.
- Validar alertas.
- Identificar falsos positivos.
- Evaluar el alcance del incidente.
- Priorizar el incidente (Triage).

---

## Triage

El **Triage** consiste en priorizar los incidentes según su impacto y urgencia.

No todos los incidentes requieren la misma atención.

Ejemplo:

| Prioridad | Ejemplo |
|-----------|----------|
| Crítica | Ransomware en servidores de producción |
| Alta | Robo de credenciales de administrador |
| Media | Malware en una estación de trabajo |
| Baja | Intentos fallidos de inicio de sesión |

---

# Indicadores utilizados durante el análisis

## IoC (Indicators of Compromise)

Son evidencias observables que indican que un sistema pudo haber sido comprometido.

Ejemplos:

- Dirección IP maliciosa.
- Hash de malware.
- Dominio sospechoso.
- Archivo infectado.
- Usuario comprometido.

---

## IoA (Indicators of Attack)

Los IoA describen el comportamiento del atacante mientras ejecuta el ataque.

Ejemplos:

- Movimiento lateral.
- Escalada de privilegios.
- Persistencia.
- Exfiltración de datos.

Mientras un **IoC** muestra evidencia de un compromiso, un **IoA** ayuda a comprender cómo se desarrolla el ataque.

---

# Threat Intelligence

La inteligencia de amenazas consiste en recopilar y analizar información sobre amenazas conocidas y emergentes.

Permite identificar:

- Malware.
- Campañas activas.
- Grupos APT.
- Técnicas utilizadas por atacantes.
- Indicadores de compromiso.

Fuentes comunes:

- VirusTotal.
- MITRE ATT&CK.
- CISA.
- CERT.
- Open Source Intelligence (OSINT).

---

# Threat Hunting

El Threat Hunting es una búsqueda proactiva de amenazas dentro de una infraestructura.

A diferencia del monitoreo tradicional, el analista no espera una alerta, sino que busca evidencia de actividades maliciosas.

---

# Fase 3 - Contención, Erradicación y Recuperación

Después de confirmar el incidente, comienza la respuesta técnica.

## Contención

Objetivo:

Evitar que el incidente continúe propagándose.

Ejemplos:

- Aislar un equipo.
- Bloquear una dirección IP.
- Deshabilitar cuentas comprometidas.
- Desconectar un servidor de la red.

---

## Erradicación

Consiste en eliminar completamente la causa del incidente.

Ejemplos:

- Eliminar malware.
- Aplicar parches.
- Corregir configuraciones inseguras.
- Eliminar cuentas maliciosas.

---

## Recuperación

Una vez eliminado el problema, se restauran los servicios afectados.

Incluye:

- Restaurar respaldos.
- Validar sistemas.
- Supervisar posibles reinfecciones.
- Confirmar el funcionamiento normal.

---

# Fase 4 - Actividad posterior al incidente

Después del incidente se realiza una revisión completa.

El objetivo es aprender y mejorar.

## Lessons Learned Meeting

Reunión donde participan todos los involucrados para analizar:

- Qué ocurrió.
- Qué funcionó correctamente.
- Qué errores existieron.
- Qué controles deben mejorarse.
- Cómo evitar incidentes similares.

---

# Documentación

Durante todo el proceso debe registrarse cada acción realizada.

Una buena documentación permite:

- Reconstruir el incidente.
- Facilitar auditorías.
- Cumplir requisitos legales.
- Compartir conocimiento.

---

## Incident Handler's Journal

Es el diario del analista.

Debe registrar:

- Fecha y hora.
- Acción realizada.
- Herramienta utilizada.
- Resultado obtenido.
- Próximos pasos.

---

# Chain of Custody

La **Cadena de Custodia** documenta quién tuvo acceso a la evidencia digital desde el momento en que fue obtenida hasta el cierre del caso.

Su objetivo es garantizar que la evidencia no fue modificada.

Una cadena de custodia incorrecta puede invalidar una investigación.

---

# CSIRT

Un **Computer Security Incident Response Team (CSIRT)** es un equipo especializado en responder incidentes de seguridad.

Sus responsabilidades incluyen:

- Investigar ataques.
- Coordinar la respuesta.
- Contener amenazas.
- Recuperar sistemas.
- Elaborar informes.

---

# Business Continuity Plan (BCP)

El **Plan de Continuidad del Negocio** establece cómo mantener las operaciones críticas durante un incidente importante.

Puede incluir:

- Sitios alternos.
- Respaldos.
- Procedimientos de recuperación.
- Comunicación con clientes.
- Priorización de servicios.

---

# Conceptos clave aprendidos

✔ Diferencia entre evento e incidente.

✔ Función del SOC.

✔ Herramientas SIEM, SOAR, IDS, IPS y EDR.

✔ Ciclo de respuesta a incidentes del NIST.

✔ IoC e IoA.

✔ Threat Hunting.

✔ Threat Intelligence.

✔ Triage.

✔ Chain of Custody.

✔ Documentación.

✔ CSIRT.

✔ Business Continuity Plan.

---

# Resumen del Módulo 1

En este módulo aprendiste los fundamentos de la detección y respuesta a incidentes.

Comprendiste cómo un SOC supervisa continuamente la infraestructura mediante herramientas como SIEM, IDS, IPS y EDR para detectar actividades sospechosas.

También conociste el ciclo de vida de respuesta a incidentes del NIST, la importancia de la documentación, la cadena de custodia y el papel del CSIRT en la gestión de incidentes.

Estos conceptos constituyen la base sobre la que se desarrollarán los siguientes módulos del curso, donde aprenderás a analizar tráfico de red, interpretar registros (logs) y utilizar herramientas SIEM para investigar incidentes de seguridad.
