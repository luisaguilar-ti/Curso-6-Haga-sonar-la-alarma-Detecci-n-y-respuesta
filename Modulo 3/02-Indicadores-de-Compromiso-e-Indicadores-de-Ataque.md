# Indicadores de Compromiso (IoC) e Indicadores de Ataque (IoA)

## Introducción

Durante la investigación de un incidente de seguridad, los analistas buscan evidencias que les permitan determinar si un sistema ha sido comprometido o si un ataque está en progreso. Estas evidencias se conocen como **Indicadores de Compromiso (IoC)** e **Indicadores de Ataque (IoA)**.

Aunque ambos conceptos están relacionados con la detección de amenazas, representan momentos diferentes dentro del ciclo de un ataque.

---

# ¿Qué es un Indicador de Compromiso (IoC)?

Un **Indicador de Compromiso (Indicator of Compromise - IoC)** es una evidencia que indica que un sistema **ya ha sido comprometido**.

Los IoC ayudan a los analistas a confirmar que ocurrió una actividad maliciosa y facilitan la investigación del incidente.

### Ejemplos de IoC

- Direcciones IP maliciosas.
- Hashes de archivos maliciosos.
- Dominios utilizados por atacantes.
- Correos electrónicos de phishing.
- Archivos infectados.
- Procesos sospechosos.
- Cambios no autorizados en archivos.
- Registros (logs) con actividad anómala.

---

# Características de los IoC

- Son evidencia de un compromiso.
- Se utilizan durante investigaciones.
- Permiten identificar ataques conocidos.
- Pueden compartirse entre organizaciones mediante inteligencia de amenazas.

---

# ¿Qué es un Indicador de Ataque (IoA)?

Un **Indicador de Ataque (Indicator of Attack - IoA)** identifica comportamientos o acciones que indican que un ataque **está ocurriendo o está a punto de ocurrir**.

A diferencia de un IoC, un IoA no depende de conocer previamente un archivo o una dirección IP maliciosa, sino del comportamiento observado.

---

# Ejemplos de IoA

- Elevación inusual de privilegios.
- Intentos repetidos de autenticación.
- Creación inesperada de cuentas.
- Ejecución de comandos sospechosos.
- Movimiento lateral dentro de la red.
- Escaneo de puertos.
- Conexiones inusuales entre equipos.
- Uso anómalo de herramientas administrativas.

---

# Diferencias entre IoC e IoA

| Indicador de Compromiso (IoC) | Indicador de Ataque (IoA) |
|-------------------------------|---------------------------|
| Indica que el sistema ya fue comprometido. | Indica que un ataque está ocurriendo. |
| Basado en evidencias. | Basado en comportamientos. |
| Ayuda en investigaciones posteriores. | Ayuda a detectar ataques en tiempo real. |
| Detecta ataques conocidos. | Puede detectar ataques desconocidos. |

---

# La Pirámide del Dolor (Pyramid of Pain)

La **Pirámide del Dolor**, propuesta por David Bianco, muestra el impacto que tiene para un atacante cuando los defensores detectan diferentes tipos de indicadores.

Mientras más alto se encuentra un indicador en la pirámide, mayor es el esfuerzo que debe realizar el atacante para modificar su comportamiento.

## Niveles de la Pirámide del Dolor

1. Hashes
2. Direcciones IP
3. Nombres de dominio
4. Artefactos de red
5. Herramientas
6. TTP (Tácticas, Técnicas y Procedimientos)

Los niveles superiores generan un mayor impacto sobre el atacante, ya que modificar sus tácticas y procedimientos requiere mucho más esfuerzo que cambiar una dirección IP o un hash.

---

# TTP (Tácticas, Técnicas y Procedimientos)

Las **TTP (Tactics, Techniques and Procedures)** describen la forma en que los atacantes llevan a cabo sus operaciones.

## Tácticas

Representan el objetivo del atacante.

Ejemplos:

- Acceso inicial.
- Persistencia.
- Movimiento lateral.
- Exfiltración de datos.

## Técnicas

Son los métodos utilizados para cumplir una táctica.

Ejemplos:

- Phishing.
- Fuerza bruta.
- PowerShell.
- Explotación de vulnerabilidades.

## Procedimientos

Son la implementación específica de una técnica por parte de un atacante o grupo de amenazas.

---

# ¿Por qué son importantes los IoC e IoA?

Permiten a los equipos de seguridad:

- Detectar amenazas.
- Priorizar investigaciones.
- Correlacionar eventos.
- Compartir inteligencia.
- Mejorar las reglas de detección.
- Reducir el tiempo de respuesta.

---

# Buenas prácticas

- Correlacionar múltiples IoC antes de confirmar un incidente.
- No depender únicamente de IoC para detectar amenazas.
- Complementar IoC con IoA y análisis de comportamiento.
- Actualizar continuamente las listas de indicadores.
- Compartir indicadores mediante plataformas de Threat Intelligence.

---

# Resumen

Los **Indicadores de Compromiso (IoC)** permiten identificar evidencias de que un sistema ya fue comprometido, mientras que los **Indicadores de Ataque (IoA)** ayudan a detectar comportamientos sospechosos antes o durante un ataque. Ambos son fundamentales para la detección de amenazas y el trabajo diario de un analista SOC. La Pirámide del Dolor y las TTP ayudan a comprender qué indicadores generan un mayor impacto sobre los atacantes y cómo fortalecer las capacidades de defensa de una organización.

---

# Conceptos clave

- IoC
- IoA
- Pirámide del Dolor
- TTP
- Tácticas
- Técnicas
- Procedimientos
- Threat Intelligence
- Comportamiento malicioso
- Evidencia digital

---

> **Siguiente tema:** [03 - Herramientas de Investigación y VirusTotal](03-Herramientas-de-Investigacion-y-VirusTotal.md)
