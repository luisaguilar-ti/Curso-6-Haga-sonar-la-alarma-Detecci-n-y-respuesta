# tcpdump

## Introducción

Durante una investigación de ciberseguridad, una de las primeras tareas consiste en observar el tráfico que circula por la red. Para ello, los analistas utilizan herramientas capaces de capturar y mostrar los paquetes que viajan entre dispositivos. Una de las herramientas más utilizadas en sistemas Linux y Unix es **tcpdump**.

tcpdump es un analizador de protocolos de red basado en la línea de comandos que permite capturar, filtrar e inspeccionar paquetes en tiempo real. Gracias a su velocidad y flexibilidad, es ampliamente utilizado por administradores de sistemas, analistas SOC, equipos Blue Team y profesionales de respuesta a incidentes.

En este capítulo aprenderás qué es tcpdump, cómo funciona y los comandos más utilizados para capturar tráfico de red.

---

# Objetivos de aprendizaje

Al finalizar este capítulo serás capaz de:

- Comprender qué es tcpdump.
- Identificar las interfaces de red disponibles.
- Capturar tráfico de una red.
- Filtrar paquetes utilizando diferentes criterios.
- Guardar capturas para analizarlas posteriormente.
- Interpretar la salida básica de tcpdump.

---

# ¿Qué es tcpdump?

**tcpdump** es un analizador de protocolos de red que funciona desde la línea de comandos.

Permite capturar paquetes directamente desde una interfaz de red para analizarlos en tiempo real o almacenarlos en un archivo.

Es una de las herramientas más utilizadas en sistemas Linux debido a que:

- Es ligera.
- Es rápida.
- Consume pocos recursos.
- Puede ejecutarse en servidores sin entorno gráfico.

---

# ¿Cómo funciona?

tcpdump escucha el tráfico que pasa por una interfaz de red.

```text
Red

↓

Interfaz de Red (NIC)

↓

tcpdump

↓

Captura de paquetes
```

Cada paquete capturado puede visualizarse inmediatamente o guardarse para su análisis posterior.

---

# Sintaxis básica

```bash
tcpdump [opciones]
```

Ejemplo:

```bash
sudo tcpdump
```

Este comando comienza a capturar todos los paquetes visibles.

---

# ¿Por qué utilizar sudo?

Capturar tráfico requiere permisos elevados.

Por ello normalmente se ejecuta:

```bash
sudo tcpdump
```

---

# Identificar las interfaces disponibles

Antes de capturar tráfico es necesario conocer el nombre de la interfaz de red.

Comando:

```bash
sudo tcpdump -D
```

Ejemplo de salida:

```text
1.eth0
2.lo
3.wlan0
```

Donde:

- **eth0** → Red cableada.
- **wlan0** → Red inalámbrica.
- **lo** → Interfaz de loopback.

---

# Capturar en una interfaz específica

```bash
sudo tcpdump -i eth0
```

Solo capturará paquetes provenientes de esa interfaz.

---

# Capturar un número determinado de paquetes

```bash
sudo tcpdump -c 20
```

Finaliza automáticamente después de capturar 20 paquetes.

Esto resulta muy útil durante pruebas.

---

# No resolver nombres DNS

Por defecto tcpdump intenta convertir direcciones IP en nombres de dominio.

Para evitarlo:

```bash
sudo tcpdump -n
```

Esto acelera la captura y facilita el análisis.

---

# Mostrar información detallada

```bash
sudo tcpdump -v
```

Opciones adicionales:

```bash
-v
-vv
-vvv
```

Cada nivel muestra información más detallada.

---

# Guardar una captura

Para almacenar los paquetes en un archivo:

```bash
sudo tcpdump -w captura.pcap
```

El archivo podrá abrirse posteriormente con Wireshark.

---

# Leer una captura

```bash
sudo tcpdump -r captura.pcap
```

No es necesario volver a capturar tráfico.

---

# Filtrar por dirección IP

Capturar tráfico de un host específico:

```bash
sudo tcpdump host 192.168.1.10
```

Solo mostrará paquetes relacionados con esa dirección IP.

---

# Filtrar por puerto

Ejemplo:

```bash
sudo tcpdump port 80
```

Captura únicamente tráfico HTTP.

Otro ejemplo:

```bash
sudo tcpdump port 443
```

Captura tráfico HTTPS.

---

# Filtrar por protocolo

TCP:

```bash
sudo tcpdump tcp
```

UDP:

```bash
sudo tcpdump udp
```

ICMP:

```bash
sudo tcpdump icmp
```

---

# Combinar filtros

Ejemplo:

```bash
sudo tcpdump host 192.168.1.10 and port 443
```

Solo mostrará tráfico HTTPS asociado a esa dirección IP.

---

# Ejemplo de salida

```text
15:42:08 IP 192.168.1.15.54872 > 142.250.190.78.443: Flags [S]
```

Información visible:

- Hora.
- Dirección IP origen.
- Dirección IP destino.
- Puerto utilizado.
- Protocolo.
- Flags TCP.

---

# Casos de uso

Un analista SOC puede utilizar tcpdump para:

- Detectar conexiones sospechosas.
- Confirmar comunicaciones C2.
- Analizar tráfico DNS.
- Investigar malware.
- Verificar actividad de una dirección IP.
- Analizar incidentes de red.

---

# Ventajas

- Muy rápido.
- Ligero.
- Disponible en la mayoría de distribuciones Linux.
- Ideal para servidores.
- Compatible con Wireshark.
- Excelente para automatización.

---

# Limitaciones

- No posee interfaz gráfica.
- Requiere conocimientos de línea de comandos.
- Capturas muy grandes pueden dificultar el análisis.
- No interpreta visualmente los protocolos como Wireshark.

---

# Buenas prácticas

- Capturar únicamente el tráfico necesario.
- Utilizar filtros para reducir información.
- Guardar las capturas originales.
- Documentar cuándo y dónde fue realizada la captura.
- Analizar posteriormente con Wireshark cuando sea necesario.

---

# Errores comunes

❌ Capturar todo el tráfico durante horas.

❌ No utilizar filtros.

❌ Olvidar ejecutar el comando con permisos elevados.

❌ No guardar las capturas importantes.

❌ Analizar directamente sobre el servidor de producción.

---

# Preguntas de entrevista

### ¿Qué es tcpdump?

Es un analizador de protocolos de red basado en la línea de comandos que permite capturar y analizar paquetes.

---

### ¿Por qué normalmente se ejecuta con sudo?

Porque capturar tráfico de red requiere permisos elevados sobre la interfaz de red.

---

### ¿Qué hace la opción -w?

Guarda la captura en un archivo PCAP.

---

### ¿Qué hace la opción -r?

Lee una captura previamente almacenada.

---

### ¿Cuál es la diferencia entre tcpdump y Wireshark?

tcpdump funciona desde la línea de comandos y es ideal para capturas rápidas o servidores, mientras que Wireshark ofrece una interfaz gráfica con herramientas avanzadas de análisis.

---

# Resumen

tcpdump es una de las herramientas más importantes para el análisis de tráfico de red en sistemas Linux. Permite capturar, filtrar y almacenar paquetes de manera eficiente, convirtiéndose en una herramienta esencial para analistas de seguridad, administradores de sistemas y equipos de respuesta a incidentes. Dominar sus comandos básicos facilita la investigación de comunicaciones sospechosas y el diagnóstico de problemas de red.
