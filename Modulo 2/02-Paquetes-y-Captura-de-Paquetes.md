# Paquetes y Captura de Paquetes

## Introducción

Toda comunicación que ocurre en una red depende del intercambio de pequeñas unidades de información conocidas como **paquetes de datos**. Cada vez que visitas un sitio web, envías un correo electrónico o reproduces un video, la información se divide en múltiples paquetes que viajan por la red hasta su destino, donde son reconstruidos.

Para un analista de ciberseguridad, los paquetes representan una de las fuentes de evidencia más importantes durante una investigación. Analizar su contenido permite comprender cómo se comunican los dispositivos, detectar anomalías e identificar actividades maliciosas.

En este capítulo aprenderás cómo está compuesto un paquete, qué son los analizadores de protocolos de red, cómo funcionan las capturas de paquetes (PCAP) y por qué son una herramienta indispensable durante una investigación forense.

---

# Objetivos de aprendizaje

Al finalizar este capítulo serás capaz de:

- Comprender qué es un paquete de datos.
- Identificar las partes que componen un paquete.
- Explicar el funcionamiento de un analizador de protocolos.
- Comprender qué es una captura de paquetes (PCAP).
- Diferenciar los principales formatos de captura.
- Reconocer los riesgos y beneficios del Packet Sniffing.

---

# ¿Qué es un paquete de datos?

Un **paquete de datos** es la unidad básica de información que viaja a través de una red.

Cuando un archivo es demasiado grande para enviarse completo, el sistema operativo lo divide en cientos o miles de paquetes. Cada paquete viaja de forma independiente hasta llegar al destino, donde todos son ensamblados nuevamente.

Por ejemplo:

```
Imagen (10 MB)

↓

Se divide en

↓

250 paquetes

↓

Viajan por Internet

↓

Se reconstruyen en el destino
```

Este mecanismo hace que las comunicaciones sean más rápidas, eficientes y tolerantes a fallos.

---

# ¿Por qué son importantes los paquetes?

Desde el punto de vista de la ciberseguridad, cada paquete contiene información valiosa sobre una comunicación.

Un analista puede conocer:

- Quién envió la información.
- Quién la recibió.
- Qué protocolo se utilizó.
- Qué puerto fue empleado.
- Cuándo ocurrió la comunicación.
- Cuánto duró.
- Cuántos datos fueron enviados.

Toda esta información permite reconstruir eventos durante una investigación.

---

# Componentes de un paquete

Un paquete está formado por tres partes principales.

## 1. Encabezado (Header)

Es la parte más importante para el enrutamiento.

Contiene información como:

- Dirección IP de origen.
- Dirección IP de destino.
- Protocolo utilizado.
- Longitud del paquete.
- Identificador del paquete.
- TTL (Time To Live).
- Información de fragmentación.

Sin este encabezado los dispositivos no sabrían hacia dónde enviar el paquete.

---

## 2. Carga útil (Payload)

La carga útil contiene los datos reales que se desean transmitir.

Ejemplos:

- Un documento PDF.
- Una imagen.
- Un correo electrónico.
- Una página web.
- Un mensaje de chat.

En muchos protocolos modernos esta información viaja cifrada mediante HTTPS o TLS.

---

## 3. Pie de página (Trailer)

El trailer se encuentra al final del paquete.

Su función principal es verificar la integridad de la información mediante mecanismos de detección de errores.

No todos los protocolos utilizan un trailer.

Por ejemplo:

- Ethernet → Sí utiliza trailer.
- IPv4 → No utiliza trailer.

---

# Analizadores de protocolos de red

Un **analizador de protocolos** (Network Protocol Analyzer o Packet Sniffer) es una herramienta diseñada para capturar, visualizar y analizar el tráfico de una red.

Estas herramientas convierten millones de bits en información comprensible para un analista.

Los analizadores más utilizados son:

- tcpdump
- Wireshark
- TShark

---

# ¿Para qué sirven?

Entre sus principales usos se encuentran:

- Investigar incidentes.
- Analizar tráfico sospechoso.
- Diagnosticar problemas de red.
- Detectar malware.
- Analizar protocolos.
- Encontrar conexiones no autorizadas.
- Investigar ataques.

---

# ¿Cómo funcionan?

El proceso puede resumirse en cinco pasos:

```text
Dispositivo

↓

Tarjeta de Red (NIC)

↓

Modo Promiscuo / Monitor

↓

Analizador de Protocolos

↓

Captura de Paquetes (PCAP)
```

El analizador recibe los paquetes, los interpreta y los presenta de forma legible.

---

# Tarjeta de Interfaz de Red (NIC)

La **Network Interface Card (NIC)** es el componente físico encargado de conectar un dispositivo a la red.

Normalmente una NIC solo procesa los paquetes dirigidos a su propio equipo.

Para capturar todo el tráfico visible es necesario habilitar un modo especial.

---

# Modo Promiscuo

El **Modo Promiscuo** permite que una tarjeta de red capture todos los paquetes que pasan por el segmento de red, independientemente de su destinatario.

Esto es indispensable para realizar análisis de tráfico.

⚠ **Importante:** utilizar este modo sin autorización puede violar políticas de seguridad o incluso la legislación vigente.

---

# Modo Monitor

En redes inalámbricas existe un modo equivalente denominado **Monitor Mode**.

Permite capturar las tramas inalámbricas que circulan por el canal Wi-Fi.

Es ampliamente utilizado durante auditorías de redes inalámbricas.

---

# Captura de paquetes (PCAP)

Una **Packet Capture (PCAP)** es un archivo que almacena todos los paquetes capturados durante una sesión.

Posteriormente puede abrirse con herramientas como Wireshark para realizar un análisis detallado.

Una captura puede contener:

- Miles de paquetes.
- Millones de paquetes.
- Varias horas de tráfico.

---

# Packet Sniffing

El **Packet Sniffing** consiste en capturar e inspeccionar el tráfico de una red.

Su uso puede ser:

## Legítimo

- Investigación forense.
- Respuesta a incidentes.
- Diagnóstico de redes.
- Auditorías.
- Monitoreo.

## Malicioso

- Robo de credenciales.
- Espionaje.
- Robo de información.
- Captura de sesiones.
- Reconocimiento de redes.

Por ello debe utilizarse únicamente con autorización.

---

# Formatos de captura

## Libpcap

Biblioteca utilizada principalmente por sistemas Linux y macOS.

Herramientas compatibles:

- tcpdump
- Wireshark

---

## WinPcap

Antigua biblioteca utilizada en Windows.

Actualmente se considera obsoleta.

---

## Npcap

Biblioteca moderna desarrollada para Windows.

Es utilizada por:

- Nmap
- Wireshark

---

## PCAPng

Formato moderno de capturas.

Ventajas:

- Guarda paquetes.
- Almacena metadatos.
- Soporta múltiples interfaces.
- Más información de la captura.

Actualmente es el formato más utilizado.

---

# Buenas prácticas

- Capturar únicamente el tráfico necesario.
- Proteger los archivos PCAP.
- Analizar las capturas en un entorno seguro.
- Filtrar antes de analizar.
- Documentar el origen de la captura.

---

# Errores comunes

❌ Pensar que todos los paquetes contienen información legible.

❌ Capturar tráfico sin autorización.

❌ No proteger los archivos PCAP.

❌ Analizar únicamente la carga útil.

❌ Ignorar la información del encabezado.

---

# Preguntas de entrevista

### ¿Qué es un paquete de datos?

Es la unidad básica de información que viaja a través de una red.

---

### ¿Cuáles son las tres partes de un paquete?

- Header
- Payload
- Trailer

---

### ¿Qué es una captura PCAP?

Es un archivo que almacena paquetes capturados durante una comunicación de red.

---

### ¿Qué diferencia existe entre tcpdump y Wireshark?

tcpdump funciona desde la línea de comandos, mientras que Wireshark ofrece una interfaz gráfica para analizar capturas de paquetes.

---

### ¿Qué es Packet Sniffing?

Es la práctica de capturar e inspeccionar paquetes de datos que circulan por una red.

---

# Resumen

Los paquetes de datos constituyen la base de toda comunicación en una red. Analizar su contenido permite comprender cómo interactúan los dispositivos, detectar anomalías e investigar incidentes de seguridad. Herramientas como tcpdump y Wireshark capturan estos paquetes y los almacenan en archivos PCAP para su análisis posterior, convirtiéndose en recursos fundamentales para cualquier analista de ciberseguridad.
