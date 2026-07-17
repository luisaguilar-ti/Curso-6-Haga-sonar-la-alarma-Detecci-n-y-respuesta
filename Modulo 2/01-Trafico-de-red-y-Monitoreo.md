# Tráfico de Red y Monitoreo

## Introducción

Cada vez que un usuario abre una página web, envía un correo electrónico, reproduce un video o descarga un archivo, miles de paquetes de datos viajan entre dispositivos a través de una red. Este intercambio constante de información se conoce como **tráfico de red**.

Para un analista de ciberseguridad, el tráfico de red representa una de las fuentes de información más importantes durante una investigación. Analizar cómo se comunican los dispositivos permite detectar comportamientos anómalos, identificar intentos de intrusión y responder oportunamente ante incidentes de seguridad.

En este capítulo aprenderás qué es el tráfico de red, por qué debe monitorearse continuamente y cuáles son las principales herramientas utilizadas para detectar actividades sospechosas.

---

# Objetivos de aprendizaje

Al finalizar este capítulo serás capaz de:

- Comprender qué es el tráfico de red.
- Diferenciar tráfico de red y datos de red.
- Entender la importancia del monitoreo continuo.
- Explicar qué es una línea base (Baseline).
- Identificar Indicadores de Compromiso (IoC).
- Comprender cómo funcionan los IDS y los analizadores de protocolos.

---

# ¿Qué es el tráfico de red?

El **tráfico de red** es la cantidad de datos que circulan entre dispositivos conectados a una red.

Cada comunicación genera tráfico:

- Abrir una página web.
- Ver un video.
- Enviar un mensaje.
- Descargar un archivo.
- Realizar una videollamada.
- Sincronizar archivos con la nube.

Todo esto produce paquetes de datos que viajan constantemente entre dispositivos.

No solamente importa la cantidad de datos, sino también:

- Qué protocolo utilizan.
- Desde dónde provienen.
- Hacia dónde van.
- En qué momento fueron enviados.
- Qué puerto utilizan.

Toda esta información ayuda a comprender el comportamiento de una red.

---

# Datos de red

Los **datos de red** son la información que realmente viaja entre los dispositivos.

Ejemplo:

Un empleado envía un correo electrónico.

Los datos de red incluyen:

- El contenido del mensaje.
- Los archivos adjuntos.
- La información necesaria para entregar el correo correctamente.

Mientras que el **tráfico de red** representa el movimiento de esos datos.

Podemos resumir la diferencia de esta forma:

| Tráfico de red | Datos de red |
|---------------|--------------|
| Movimiento de información | Información transmitida |
| Describe el flujo | Describe el contenido |
| Se monitorea continuamente | Se analiza cuando es necesario |

---

# ¿Por qué es importante monitorear una red?

No es posible proteger aquello que no se conoce.

Antes de detectar un ataque, un analista necesita comprender cómo funciona normalmente la red de la organización.

El monitoreo permite detectar:

- Conexiones inusuales.
- Equipos comprometidos.
- Malware.
- Robo de información.
- Comunicación con servidores maliciosos.
- Intentos de acceso no autorizados.

Mientras más rápido se detecte una anomalía, menor será el impacto del incidente.

---

# Línea base (Baseline)

Una **línea base** representa el comportamiento normal esperado de una red.

Es el punto de referencia contra el cual se comparan todas las actividades futuras.

Ejemplo:

Una empresa trabaja de:

- 09:00
- a
- 18:00

Durante ese horario existen aproximadamente:

- 800 usuarios conectados.
- 40 GB de tráfico por hora.

Ese comportamiento se convierte en la línea base.

Ahora imagina que a las **03:00 AM** aparecen:

- 500 conexiones nuevas.
- 90 GB de información saliendo hacia Internet.

Eso representa una desviación importante de la línea base y debe investigarse inmediatamente.

---

# ¿Qué puede monitorearse?

Un analista puede monitorear diferentes aspectos de la red.

## Flujo de comunicaciones

Permite conocer:

- origen
- destino
- protocolo
- puerto
- duración
- volumen de datos

Ejemplo:

```
Origen: 192.168.1.25

↓

HTTPS

↓

443

↓

Servidor Web
```

---

## Carga útil (Payload)

La carga útil contiene la información que realmente se está transmitiendo.

Dependiendo del protocolo, puede encontrarse:

- archivos
- imágenes
- documentos
- credenciales
- comandos
- malware

Mucho del tráfico actual se encuentra cifrado, por lo que no siempre es posible inspeccionar directamente el contenido.

---

## Patrones temporales

También se analiza:

- Hora del día
- Frecuencia
- Duración
- Días de mayor actividad

Ejemplo:

Si normalmente existen:

- 2 GB por hora

y de repente aparecen

- 40 GB enviados durante la madrugada

podría tratarse de un ataque de **exfiltración de datos**.

---

# Exfiltración de datos

La exfiltración consiste en la transferencia no autorizada de información fuera de una organización.

Generalmente el atacante intenta enviar:

- Bases de datos.
- Contraseñas.
- Información financiera.
- Información personal.
- Propiedad intelectual.

Este tipo de ataque suele detectarse observando grandes volúmenes de tráfico saliente.

---

# Command and Control (C2)

Después de comprometer un equipo, un atacante necesita mantener comunicación con él.

A esto se le conoce como **Command and Control (C2)**.

```
Atacante
      │
      ▼
Servidor C2
      │
      ▼
Equipo comprometido
```

El atacante utiliza este canal para:

- ejecutar comandos
- instalar malware
- robar información
- mantener persistencia

Una señal común es observar conexiones hacia puertos o protocolos poco habituales.

Ejemplo:

HTTPS normalmente utiliza:

```
443
```

Si un malware utiliza:

```
HTTPS → Puerto 8088
```

puede representar actividad sospechosa.

---

# Indicadores de Compromiso (IoC)

Un **IoC** es cualquier evidencia que indica que un sistema pudo haber sido comprometido.

Ejemplos:

- Dirección IP maliciosa.
- Hash de malware.
- Dominio sospechoso.
- Archivo infectado.
- Conexión C2.
- Usuario desconocido.
- Transferencias inusuales.

Los IoC ayudan a detectar incidentes rápidamente.

---

# Herramientas utilizadas

## IDS (Intrusion Detection System)

Un IDS monitorea continuamente la actividad de la red y genera alertas cuando detecta comportamientos sospechosos.

No bloquea ataques.

Su función es:

Detectar y alertar.

---

## Analizadores de protocolos

También llamados:

- Packet Sniffers

Permiten:

- Capturar tráfico.
- Analizar paquetes.
- Filtrar información.
- Investigar incidentes.

Los más utilizados son:

- tcpdump
- Wireshark
- TShark

Estos se estudiarán con mayor detalle en los siguientes capítulos.

---

# SOC vs NOC

Es común confundir ambos conceptos.

## SOC

Security Operations Center

Responsable de:

- Detectar amenazas.
- Analizar incidentes.
- Responder ataques.

## NOC

Network Operations Center

Responsable de:

- Disponibilidad de la red.
- Rendimiento.
- Caídas del servicio.
- Infraestructura.

El SOC protege la organización.

El NOC mantiene funcionando la infraestructura.

---

# Buenas prácticas

- Conocer el comportamiento normal de la red.
- Mantener una línea base actualizada.
- Investigar toda desviación importante.
- Automatizar alertas.
- Registrar los eventos relevantes.
- Revisar periódicamente los IoC conocidos.

---

# Errores comunes

❌ Pensar que mucho tráfico siempre significa un ataque.

❌ Analizar únicamente el volumen de datos.

❌ Ignorar los patrones horarios.

❌ No actualizar la línea base.

❌ Confiar únicamente en herramientas automáticas.

---

# Preguntas de entrevista

**¿Qué es el tráfico de red?**

Es el flujo de datos que circula entre dispositivos conectados a una red.

---

**¿Qué es una línea base?**

Es el comportamiento normal esperado de una red utilizado como referencia para detectar anomalías.

---

**¿Qué es un IoC?**

Es una evidencia observable que indica un posible compromiso de seguridad.

---

**¿Cuál es la diferencia entre un SOC y un NOC?**

El SOC protege la organización contra amenazas; el NOC mantiene la disponibilidad y el rendimiento de la infraestructura de red.

---

**¿Qué herramientas se utilizan para monitorear el tráfico de red?**

Entre las más comunes se encuentran:

- IDS
- tcpdump
- Wireshark
- TShark

---

# Resumen

El tráfico de red constituye una de las principales fuentes de información para un analista de ciberseguridad. Comprender el comportamiento normal de una red mediante una línea base permite detectar desviaciones que podrían indicar ataques, exfiltración de datos o comunicaciones maliciosas. Herramientas como los IDS y los analizadores de protocolos proporcionan la visibilidad necesaria para investigar incidentes y proteger la infraestructura de una organización.
