# Investigar los Detalles del Paquete

## Introducción

Capturar paquetes de red es solo el primer paso durante una investigación de ciberseguridad. El verdadero valor se obtiene al interpretar la información contenida en cada paquete para reconstruir las comunicaciones entre dispositivos, identificar comportamientos anómalos y descubrir posibles actividades maliciosas.

Cada paquete almacena información sobre el origen, el destino, el protocolo utilizado y los datos transmitidos. Analizar correctamente estos campos permite responder preguntas como:

- ¿Quién inició la comunicación?
- ¿Qué servicio se utilizó?
- ¿Se transfirió información sensible?
- ¿Existe evidencia de un ataque?

En este capítulo aprenderás a interpretar los principales campos de un paquete IPv4 y comprenderás cómo esta información ayuda a los analistas durante una investigación.

---

# Objetivos de aprendizaje

Al finalizar este capítulo serás capaz de:

- Comprender la estructura de un paquete IPv4.
- Interpretar los principales campos del encabezado.
- Identificar información útil durante una investigación.
- Reconocer protocolos comunes.
- Comprender cómo los encabezados ayudan al enrutamiento.
- Analizar un paquete desde la perspectiva de un analista de seguridad.

---

# Anatomía de un paquete

Un paquete está compuesto por tres partes principales:

```text
┌─────────────────────────────┐
│         Header              │
├─────────────────────────────┤
│         Payload             │
├─────────────────────────────┤
│         Trailer             │
└─────────────────────────────┘
```

Cada sección cumple una función específica durante la transmisión de datos.

---

# El encabezado (Header)

El encabezado contiene toda la información necesaria para transportar el paquete hasta su destino.

Durante una investigación, esta es normalmente la sección más importante.

Entre sus campos destacan:

- Versión del protocolo
- Longitud del encabezado
- Longitud total
- Identificación
- Banderas (Flags)
- Fragmentación
- Tiempo de vida (TTL)
- Protocolo
- Dirección IP de origen
- Dirección IP de destino
- Checksum

---

# Versión (Version)

Indica qué versión del Protocolo de Internet está utilizando el paquete.

Los valores más comunes son:

- IPv4
- IPv6

Ejemplo:

```
Version: IPv4
```

---

# Longitud del encabezado (Header Length)

Indica el tamaño del encabezado.

Generalmente un encabezado IPv4 ocupa:

```
20 bytes
```

Aunque puede aumentar cuando contiene opciones adicionales.

---

# Longitud total (Total Length)

Representa el tamaño completo del paquete.

Incluye:

- Encabezado
- Datos (Payload)

Ejemplo:

```
Total Length: 1500 bytes
```

---

# Identificación (Identification)

Cada paquete recibe un número identificador.

Este valor permite reconstruir correctamente un paquete cuando fue dividido en múltiples fragmentos.

---

# Fragmentación

Si un paquete es demasiado grande para una red determinada, puede dividirse en varios fragmentos.

Cada fragmento conserva información que permitirá volver a ensamblarlo en el equipo destino.

---

# Flags

Las banderas indican cómo debe tratarse el paquete durante la transmisión.

Las más importantes son:

**DF (Don't Fragment)**

Indica que el paquete no debe fragmentarse.

**MF (More Fragments)**

Indica que todavía existen fragmentos pendientes por recibir.

---

# TTL (Time To Live)

El TTL indica cuántos dispositivos de red puede atravesar un paquete antes de ser descartado.

Cada router disminuye este valor en uno.

Ejemplo:

```
TTL inicial = 64

↓

Router 1

TTL = 63

↓

Router 2

TTL = 62
```

Cuando llega a:

```
TTL = 0
```

el paquete es eliminado.

Esto evita que los paquetes circulen indefinidamente por Internet.

---

# Protocolo

Este campo indica qué protocolo de la capa superior transporta el paquete.

Ejemplos comunes:

| Valor | Protocolo |
|--------|-----------|
| 1 | ICMP |
| 6 | TCP |
| 17 | UDP |

Este dato ayuda al analista a comprender qué tipo de comunicación está ocurriendo.

---

# Dirección IP de origen

Identifica el dispositivo que envió el paquete.

Ejemplo:

```
192.168.1.15
```

Esta información ayuda a identificar el posible origen de una actividad sospechosa.

---

# Dirección IP de destino

Indica el equipo que recibirá el paquete.

Ejemplo:

```
172.217.14.206
```

Durante una investigación es uno de los primeros campos revisados.

---

# Checksum

El checksum permite verificar que el encabezado no fue alterado durante la transmisión.

Si el valor calculado no coincide con el recibido, el paquete puede descartarse.

---

# La carga útil (Payload)

Después del encabezado se encuentra la carga útil.

Aquí viajan los datos reales.

Puede contener:

- Una página web.
- Un archivo.
- Una imagen.
- Un correo electrónico.
- Un mensaje.
- Datos cifrados.

En conexiones HTTPS normalmente la carga útil se encuentra cifrada.

---

# El trailer

Algunos protocolos, como Ethernet, agregan un trailer al final del paquete.

Su función principal consiste en detectar errores durante la transmisión.

IPv4 no utiliza trailer.

---

# Información útil para una investigación

Cuando un analista examina un paquete normalmente responde preguntas como:

## ¿Quién envió el paquete?

Utilizando la IP de origen.

---

## ¿Quién lo recibió?

Utilizando la IP de destino.

---

## ¿Qué protocolo utiliza?

Observando el campo Protocol.

---

## ¿Cuándo ocurrió?

Mediante la marca de tiempo registrada por la captura.

---

## ¿Existe fragmentación?

Revisando Identification y Flags.

---

## ¿Es tráfico normal?

Comparando con la línea base de la organización.

---

# Ejemplo práctico

Supongamos el siguiente paquete:

| Campo | Valor |
|--------|-------|
| Origen | 192.168.1.15 |
| Destino | 142.250.190.78 |
| Protocolo | TCP |
| Puerto | 443 |
| TTL | 64 |

Un analista puede concluir:

- Es una comunicación TCP.
- Utiliza HTTPS.
- Se dirige a un servidor web.
- No presenta anomalías evidentes.

Ahora imagina este caso:

| Campo | Valor |
|--------|-------|
| Protocolo | HTTPS |
| Puerto | 8088 |

Aunque HTTPS suele utilizar el puerto 443, aquí aparece utilizando el puerto 8088.

Esto podría representar:

- Software malicioso.
- Canal Command & Control (C2).
- Configuración no autorizada.

Sería necesario continuar la investigación.

---

# Buenas prácticas

- Revisar primero el encabezado.
- Verificar direcciones IP.
- Analizar el protocolo utilizado.
- Identificar puertos inusuales.
- Correlacionar la información con otros registros.
- Comparar siempre con la línea base de la red.

---

# Errores comunes

❌ Analizar únicamente la carga útil.

❌ Ignorar el TTL.

❌ No revisar los Flags.

❌ Confiar únicamente en la dirección IP.

❌ No correlacionar la información con otros eventos.

---

# Preguntas de entrevista

### ¿Cuál es la función del encabezado de un paquete?

Contener la información necesaria para transportar correctamente el paquete hasta su destino.

---

### ¿Qué información contiene el encabezado IPv4?

Entre otros campos:

- Dirección IP origen
- Dirección IP destino
- TTL
- Protocolo
- Longitud
- Fragmentación
- Checksum

---

### ¿Qué es el TTL?

Es un contador que limita la cantidad de dispositivos que un paquete puede atravesar antes de ser descartado.

---

### ¿Qué función tiene el campo Protocol?

Indicar qué protocolo de capa superior transporta el paquete, por ejemplo TCP, UDP o ICMP.

---

### ¿Por qué es importante analizar el encabezado durante una investigación?

Porque proporciona información sobre el origen, destino, protocolo y comportamiento de la comunicación, permitiendo identificar actividades sospechosas.

---

# Resumen

El análisis de paquetes constituye una habilidad esencial para cualquier analista de ciberseguridad. Comprender los campos del encabezado IPv4 permite reconstruir comunicaciones, identificar anomalías y obtener evidencia durante una investigación. Elementos como las direcciones IP, el protocolo utilizado, el TTL y la fragmentación proporcionan información crítica para detectar incidentes y comprender el comportamiento del tráfico de red.
