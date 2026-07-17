# 02. Fuentes de Registro e Ingestión de Registros

## Descripción

Las herramientas **SIEM (Security Information and Event Management)** dependen de los datos de registro para detectar amenazas, correlacionar eventos y facilitar las investigaciones de seguridad. Para que esto sea posible, primero deben recopilar información procedente de múltiples fuentes mediante un proceso conocido como **ingestión de registros (Log Ingestion)**.

Comprender cómo se recopilan, transfieren y procesan los registros permite a los analistas conocer el origen de la información que utilizan durante una investigación y comprender cómo una plataforma SIEM transforma esos datos en información útil.

---

# ¿Qué es una fuente de registro?

Una **fuente de registro (Log Source)** es cualquier dispositivo, sistema o aplicación capaz de generar eventos registrados.

Algunos ejemplos son:

- Servidores
- Equipos de usuario
- Firewalls
- Routers
- Switches
- Sistemas Operativos
- Aplicaciones
- IDS/IPS
- Antivirus
- EDR

Cada una de estas fuentes genera registros que posteriormente pueden ser enviados a una plataforma SIEM para su análisis.

---

# ¿Qué es la ingestión de registros?

La **ingestión de registros (Log Ingestion)** es el proceso mediante el cual una herramienta SIEM recopila e importa registros provenientes de diferentes fuentes de datos.

Durante este proceso, el SIEM recibe una copia de los eventos generados por los sistemas originales y los almacena en su propia plataforma para analizarlos posteriormente.

Esto permite:

- Centralizar la información.
- Facilitar las investigaciones.
- Correlacionar eventos.
- Detectar amenazas.
- Generar alertas.

Es importante destacar que el SIEM trabaja sobre una **copia** de los registros, sin modificar los archivos originales.

---

# Proceso general de un SIEM

El funcionamiento de un SIEM puede dividirse en tres etapas principales.

## 1. Recopilación y agregación de datos

El SIEM recibe registros provenientes de múltiples fuentes.

Estas fuentes pueden incluir:

- Equipos de usuario
- Servidores
- Dispositivos de red
- Aplicaciones
- Herramientas de seguridad

El objetivo es concentrar toda la información en un único repositorio.

---

## 2. Normalización de datos

Cada fabricante registra la información utilizando formatos diferentes.

La **normalización** consiste en convertir esos registros a un formato común para facilitar su procesamiento.

Entre sus ventajas destacan:

- Estructura uniforme.
- Búsquedas más sencillas.
- Mejor correlación entre eventos.
- Mayor compatibilidad entre diferentes fuentes.

La capacidad de normalización depende de cada plataforma SIEM.

---

## 3. Análisis de datos

Una vez normalizados, los registros son:

- Organizados.
- Indexados.
- Correlacionados.
- Analizados.

Esto permite identificar:

- Actividades sospechosas.
- Patrones de ataque.
- Comportamientos anómalos.
- Eventos relacionados.

---

# ¿Por qué es importante la ingestión de registros?

Sin registros, un SIEM no puede realizar análisis.

La calidad del monitoreo depende directamente de:

- Las fuentes de datos disponibles.
- La cantidad de registros recopilados.
- La calidad de la información.
- La correcta configuración de la ingestión.

Una mala configuración puede provocar que eventos importantes nunca lleguen a la plataforma SIEM.

---

# Reenviadores de registros (Log Forwarders)

La mayoría de las organizaciones utilizan **reenviadores de registros (Log Forwarders)** para automatizar el envío de registros hacia un SIEM.

Un **Log Forwarder** es un programa que recopila registros desde un dispositivo y los envía automáticamente a una plataforma centralizada.

Entre sus ventajas se encuentran:

- Automatización del proceso.
- Reducción del trabajo manual.
- Envío continuo de información.
- Mayor escalabilidad.
- Administración centralizada.

---

# Funcionamiento de un Log Forwarder

El proceso general consiste en:

1. El dispositivo genera un registro.
2. El reenviador detecta el nuevo evento.
3. El registro es enviado al SIEM.
4. El SIEM almacena una copia.
5. El registro es normalizado.
6. Finalmente es analizado y correlacionado.

---

# Configuración de un reenviador

Después de instalar un reenviador de registros es necesario definir:

- Qué registros serán enviados.
- A qué servidor SIEM serán enviados.
- Con qué frecuencia se enviarán.
- Qué eventos serán ignorados.

Esto permite optimizar el rendimiento y evitar recopilar información innecesaria.

---

# Reenviadores nativos y de terceros

Algunos sistemas operativos incluyen reenviadores propios.

En otros casos es necesario instalar software adicional desarrollado por terceros.

Además, muchas plataformas SIEM proporcionan sus propios agentes o permiten integrarse con soluciones de código abierto.

La elección depende de factores como:

- Infraestructura existente.
- Compatibilidad.
- Escalabilidad.
- Requisitos de la organización.

---

# Beneficios de la ingestión de registros

Una correcta ingestión de registros permite:

- Centralizar la información.
- Reducir el trabajo manual.
- Facilitar las investigaciones.
- Mejorar la detección de amenazas.
- Correlacionar eventos de múltiples dispositivos.
- Automatizar el monitoreo.
- Obtener mayor visibilidad del entorno.

---

# Buenas prácticas

- Definir claramente las fuentes de registro.
- Automatizar la recopilación mediante Log Forwarders.
- Revisar periódicamente la configuración.
- Enviar únicamente la información necesaria.
- Supervisar el funcionamiento de los agentes.
- Verificar que los registros lleguen correctamente al SIEM.
- Mantener sincronizados los relojes de los dispositivos para preservar la precisión de las marcas de tiempo.

---

# Resumen

La ingestión de registros constituye la primera etapa del funcionamiento de una plataforma SIEM. Consiste en recopilar y centralizar registros provenientes de múltiples dispositivos para posteriormente normalizarlos y analizarlos. El uso de reenviadores de registros automatiza este proceso, mejora la eficiencia operativa y proporciona la información necesaria para detectar amenazas e investigar incidentes de seguridad.

---

# Conceptos clave

- Fuente de registro (Log Source)
- Ingestión de registros (Log Ingestion)
- SIEM
- Normalización de datos
- Correlación de eventos
- Log Forwarder
- Agente de registros
- Recopilación de registros
- Análisis de registros
- Eventos
- Telemetría
- Plataforma centralizada
