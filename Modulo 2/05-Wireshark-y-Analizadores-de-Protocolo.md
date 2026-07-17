# Wireshark y Analizadores de Protocolos

## Introducción

Capturar paquetes es solo una parte del trabajo de un analista de ciberseguridad. El siguiente paso consiste en interpretar esa información para descubrir comportamientos sospechosos, reconstruir comunicaciones e identificar posibles incidentes.

Aunque herramientas como **tcpdump** son excelentes para capturar tráfico desde la línea de comandos, analizar miles o millones de paquetes puede resultar complicado. Para facilitar esta tarea existen los **analizadores de protocolos de red**, siendo **Wireshark** el más utilizado en la industria.

Wireshark permite visualizar, filtrar y analizar paquetes de manera gráfica, ofreciendo una visión detallada de las comunicaciones de una red. Gracias a su capacidad para interpretar cientos de protocolos, se ha convertido en una herramienta indispensable para analistas SOC, equipos Blue Team, administradores de red y especialistas en respuesta a incidentes.

---

# Objetivos de aprendizaje

Al finalizar este capítulo serás capaz de:

- Comprender qué es Wireshark.
- Identificar las principales funciones de un analizador de protocolos.
- Abrir y analizar archivos PCAP.
- Aplicar filtros de visualización.
- Interpretar la información de un paquete.
- Reconocer cuándo utilizar Wireshark o tcpdump.

---

# ¿Qué es Wireshark?

**Wireshark** es un analizador de protocolos de red de código abierto que permite capturar, visualizar y analizar el tráfico de una red mediante una interfaz gráfica.

Es capaz de interpretar cientos de protocolos diferentes y mostrar la información de forma organizada para facilitar el análisis.

Actualmente es una de las herramientas más utilizadas en:

- Centros de Operaciones de Seguridad (SOC).
- Equipos Blue Team.
- Equipos de Respuesta a Incidentes.
- Auditorías de red.
- Laboratorios de ciberseguridad.
- Universidades.

---

# ¿Cómo funciona?

Wireshark captura el tráfico que pasa por una interfaz de red o abre un archivo PCAP previamente generado.

```text
Red

↓

Interfaz de Red

↓

Wireshark

↓

Captura de paquetes

↓

Análisis gráfico
```

El programa interpreta automáticamente cada protocolo y organiza la información para facilitar su comprensión.

---

# Principales características

Wireshark permite:

- Capturar tráfico en tiempo real.
- Abrir archivos PCAP.
- Aplicar filtros avanzados.
- Seguir conversaciones TCP.
- Analizar protocolos.
- Exportar información.
- Buscar paquetes específicos.
- Detectar anomalías en la comunicación.

---

# La interfaz de Wireshark

La ventana principal se divide normalmente en tres paneles.

## 1. Lista de paquetes

Muestra todos los paquetes capturados.

Incluye información como:

- Número del paquete.
- Hora.
- Dirección IP origen.
- Dirección IP destino.
- Protocolo.
- Longitud.
- Descripción.

---

## 2. Detalles del paquete

Al seleccionar un paquete se muestran todos sus encabezados.

Por ejemplo:

- Ethernet
- IPv4
- TCP
- HTTP

Cada protocolo puede expandirse para observar sus campos.

---

## 3. Datos en formato hexadecimal

Muestra el contenido real del paquete.

Incluye:

- Valores hexadecimales.
- Representación ASCII.

Es especialmente útil durante análisis forenses.

---

# Abrir una captura PCAP

Una vez capturado el tráfico con tcpdump, puede abrirse en Wireshark.

Archivo

↓

Open

↓

Seleccionar archivo PCAP

↓

Visualizar captura

No es necesario volver a capturar el tráfico.

---

# Filtros de visualización

Una de las funciones más potentes de Wireshark son sus filtros.

Permiten localizar rápidamente información relevante.

---

## Mostrar únicamente tráfico HTTP

```text
http
```

---

## Mostrar tráfico HTTPS

```text
tls
```

o

```text
tcp.port == 443
```

---

## Mostrar tráfico DNS

```text
dns
```

---

## Mostrar tráfico ICMP

```text
icmp
```

---

## Mostrar una dirección IP

```text
ip.addr == 192.168.1.15
```

---

## Mostrar únicamente tráfico TCP

```text
tcp
```

---

## Mostrar únicamente tráfico UDP

```text
udp
```

---

# Seguir una conversación TCP

Wireshark permite reconstruir toda una conversación entre dos dispositivos.

Esta función resulta muy útil para:

- Analizar ataques.
- Investigar malware.
- Revisar sesiones HTTP.
- Comprender una comunicación completa.

---

# ¿Qué información puede obtener un analista?

Mediante Wireshark es posible identificar:

- Direcciones IP.
- Direcciones MAC.
- Protocolos utilizados.
- Puertos.
- Tiempos de respuesta.
- Errores de comunicación.
- Retransmisiones.
- Tráfico sospechoso.

---

# Casos de uso

Un analista puede utilizar Wireshark para:

- Investigar incidentes.
- Analizar malware.
- Detectar conexiones C2.
- Diagnosticar problemas de red.
- Analizar tráfico DNS.
- Investigar exfiltración de datos.
- Verificar comunicaciones entre servidores.

---

# Wireshark vs tcpdump

| Característica | Wireshark | tcpdump |
|----------------|-----------|----------|
| Interfaz gráfica | ✅ | ❌ |
| Línea de comandos | ❌ | ✅ |
| Fácil de interpretar | ✅ | ❌ |
| Consumo de recursos | Alto | Bajo |
| Ideal para servidores | No | Sí |
| Análisis avanzado | Excelente | Básico |
| Captura en tiempo real | Sí | Sí |

---

# ¿Cuándo utilizar cada uno?

### Utiliza tcpdump cuando:

- Trabajas en un servidor Linux.
- No existe entorno gráfico.
- Necesitas capturas rápidas.
- Automatizas procesos.

### Utiliza Wireshark cuando:

- Debes analizar muchos paquetes.
- Necesitas visualizar protocolos.
- Investigas incidentes.
- Analizas archivos PCAP.
- Realizas análisis forense.

En muchos casos ambas herramientas se utilizan de forma complementaria.

---

# Buenas prácticas

- Capturar únicamente el tráfico necesario.
- Utilizar filtros para reducir el ruido.
- Guardar siempre la captura original.
- Documentar la investigación.
- Proteger los archivos PCAP.
- Analizar el tráfico en un entorno controlado.

---

# Errores comunes

❌ Capturar tráfico sin autorización.

❌ Analizar únicamente un paquete aislado.

❌ No utilizar filtros.

❌ Ignorar los protocolos de transporte.

❌ No correlacionar la información con otros registros.

---

# Preguntas de entrevista

### ¿Qué es Wireshark?

Es un analizador de protocolos de red de código abierto que permite capturar y analizar tráfico mediante una interfaz gráfica.

---

### ¿Qué diferencia existe entre Wireshark y tcpdump?

tcpdump se utiliza desde la línea de comandos y es ideal para capturar tráfico, mientras que Wireshark proporciona herramientas gráficas para analizar los paquetes con mayor detalle.

---

### ¿Qué es un archivo PCAP?

Es un archivo que almacena paquetes capturados durante una comunicación de red y puede abrirse posteriormente con herramientas como Wireshark.

---

### ¿Para qué sirven los filtros de Wireshark?

Permiten localizar rápidamente paquetes específicos según protocolos, direcciones IP, puertos u otras características.

---

### ¿Por qué Wireshark es tan utilizado durante la respuesta a incidentes?

Porque facilita la inspección detallada del tráfico de red y ayuda a reconstruir comunicaciones sospechosas de forma visual.

---

# Resumen

Wireshark es el analizador de protocolos de red más utilizado en el ámbito de la ciberseguridad. Su interfaz gráfica, su capacidad para interpretar cientos de protocolos y sus potentes filtros lo convierten en una herramienta esencial para investigar incidentes, analizar archivos PCAP y comprender el comportamiento del tráfico de red. Combinado con tcpdump, proporciona una solución completa para la captura y el análisis de paquetes.
