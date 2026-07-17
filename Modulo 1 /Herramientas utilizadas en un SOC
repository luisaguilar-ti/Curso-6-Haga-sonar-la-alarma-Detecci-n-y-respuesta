# Herramientas utilizadas en un SOC

Una de las principales responsabilidades de un analista de seguridad es supervisar continuamente los sistemas de la organización para detectar comportamientos anómalos y responder rápidamente ante incidentes.

Para lograrlo, un SOC utiliza diversas herramientas que trabajan de forma complementaria. Aunque cada una tiene una función específica, juntas forman una arquitectura capaz de detectar, analizar y responder a amenazas.

---

# SIEM (Security Information and Event Management)

## ¿Qué es un SIEM?

Un **SIEM (Security Information and Event Management)** es una plataforma que recopila, centraliza, almacena y analiza registros (logs) provenientes de diferentes dispositivos y aplicaciones.

Su objetivo es ofrecer una visión centralizada de la actividad de seguridad de toda la infraestructura.

En lugar de revisar manualmente miles de registros provenientes de servidores, firewalls, aplicaciones y equipos de usuario, el SIEM reúne toda esa información en un solo lugar.

---

## ¿Qué información recopila?

Un SIEM puede recibir registros provenientes de:

- Firewalls
- Routers
- Switches
- Servidores Windows
- Servidores Linux
- Active Directory
- Antivirus
- EDR
- Aplicaciones Web
- Bases de datos
- Servicios en la nube
- Dispositivos de red

---

## Funciones principales

Un SIEM permite:

- Centralizar registros.
- Buscar eventos específicos.
- Correlacionar información.
- Detectar amenazas.
- Generar alertas.
- Crear reportes.
- Apoyar investigaciones forenses.

---

## Flujo de trabajo

```text
Firewall
        │
Windows Server
        │
Linux Server
        │
Active Directory
        │
Aplicaciones
        │
───────────────► SIEM
                     │
                     ▼
            Correlación de eventos
                     │
                     ▼
                 Generación de alertas
                     │
                     ▼
               Analista SOC
```

---

## Ventajas

- Centraliza la información.
- Reduce el tiempo de investigación.
- Permite correlacionar eventos de múltiples fuentes.
- Facilita auditorías.
- Conserva evidencia histórica.

---

## Limitaciones

- Requiere una configuración adecuada.
- Puede generar falsos positivos.
- Consume recursos de almacenamiento.
- Necesita mantenimiento continuo.

---

## Ejemplos de SIEM

| Herramienta | Tipo |
|-------------|------|
| Splunk Enterprise Security | Comercial |
| Google SecOps (Chronicle) | Comercial |
| Microsoft Sentinel | Comercial |
| IBM QRadar | Comercial |
| Elastic Security | Open Source / Comercial |
| Wazuh | Open Source |

---

# SOAR (Security Orchestration, Automation and Response)

## ¿Qué es SOAR?

Un sistema **SOAR** automatiza tareas repetitivas durante la respuesta a incidentes.

Mientras un SIEM detecta una amenaza, un SOAR ayuda a ejecutar automáticamente acciones previamente definidas.

---

## Ejemplo

Sin automatización:

1. Se detecta malware.
2. El analista revisa la alerta.
3. Bloquea la IP.
4. Aísla el equipo.
5. Notifica al usuario.
6. Documenta el incidente.

Con SOAR:

```text
Alerta SIEM
      │
      ▼
SOAR ejecuta automáticamente

✓ Aísla el equipo
✓ Bloquea la IP
✓ Crea ticket
✓ Envía correo
✓ Notifica al SOC
```

El analista supervisa el proceso y toma decisiones cuando es necesario.

---

## Beneficios

- Reduce tiempos de respuesta.
- Automatiza tareas repetitivas.
- Disminuye errores humanos.
- Estandariza procedimientos.
- Integra múltiples herramientas.

---

# IDS (Intrusion Detection System)

## ¿Qué es?

Un IDS es una herramienta diseñada para detectar actividades sospechosas.

Su función principal es **alertar**, pero no detener un ataque.

---

## Funcionamiento

```text
Ataque
   │
   ▼
IDS detecta actividad
   │
   ▼
Genera alerta
   │
   ▼
Analista SOC
```

---

## Tipos de IDS

### HIDS (Host-based Intrusion Detection System)

Se instala directamente en un equipo.

Supervisa:

- Procesos
- Archivos
- Usuarios
- Cambios en el sistema
- Registros locales

Ejemplos:

- Wazuh Agent
- OSSEC

---

### NIDS (Network Intrusion Detection System)

Supervisa el tráfico de red.

Analiza:

- Paquetes
- Protocolos
- Conexiones
- Comunicaciones sospechosas

Ejemplos:

- Suricata
- Snort
- Zeek

---

# IPS (Intrusion Prevention System)

Un IPS funciona de forma similar a un IDS, pero además puede bloquear automáticamente actividades maliciosas.

```text
Ataque
   │
   ▼
IPS detecta
   │
   ▼
Bloquea tráfico
   │
   ▼
Ataque detenido
```

---

## Diferencias entre IDS e IPS

| IDS | IPS |
|------|-----|
| Detecta amenazas | Detecta y bloquea amenazas |
| Solo genera alertas | Puede detener ataques automáticamente |
| No modifica el tráfico | Interviene en el tráfico de red |
| Menor riesgo de afectar servicios | Requiere una configuración cuidadosa |

---

# EDR (Endpoint Detection and Response)

## ¿Qué es?

Un EDR protege dispositivos individuales (endpoints), como:

- Computadoras
- Laptops
- Servidores
- Estaciones de trabajo

Monitorea continuamente su actividad para detectar comportamientos maliciosos.

---

## Información que analiza

- Procesos
- Archivos
- Memoria
- Registro de Windows
- Usuarios
- Conexiones
- Ejecución de programas

---

## Acciones que puede realizar

- Aislar un equipo.
- Finalizar procesos.
- Eliminar archivos maliciosos.
- Bloquear conexiones.
- Generar alertas.

---

## Ejemplos

- Microsoft Defender for Endpoint
- CrowdStrike Falcon
- SentinelOne
- Sophos Intercept X

---

# Comparativa rápida

| Herramienta | Función principal |
|-------------|------------------|
| SIEM | Centraliza y analiza registros. |
| SOAR | Automatiza la respuesta. |
| IDS | Detecta amenazas. |
| IPS | Detecta y bloquea amenazas. |
| EDR | Protege dispositivos individuales. |

---

# Cómo trabajan juntas

```text
Endpoints
Servidores
Firewalls
Routers
Switches
      │
      ▼
     SIEM
      │
      ▼
Genera alerta
      │
      ▼
 Analista SOC
      │
      ▼
     SOAR
      │
      ▼
Automatiza acciones

Mientras tanto:

IDS supervisa la red.

IPS bloquea ataques.

EDR protege cada equipo.
```

---

# Ideas clave

- El SIEM es el centro de monitoreo.
- El SOAR automatiza tareas de respuesta.
- El IDS detecta actividades sospechosas.
- El IPS puede detener ataques automáticamente.
- El EDR protege cada endpoint de la organización.
