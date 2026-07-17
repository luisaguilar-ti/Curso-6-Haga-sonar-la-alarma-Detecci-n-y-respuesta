# Resumen del Módulo

## Introducción

En este módulo se estudiaron los fundamentos del tráfico de red y las herramientas utilizadas para capturarlo y analizarlo. Estos conocimientos constituyen la base para comprender cómo se comunican los dispositivos y cómo los analistas de ciberseguridad investigan incidentes utilizando evidencia obtenida de la red.

---

## Conceptos clave

### Tráfico de red

El tráfico de red es el flujo de datos que circula entre dispositivos conectados a una red. Analizar este tráfico permite detectar actividades sospechosas, identificar ataques y comprender el comportamiento normal de una infraestructura.

---

### Paquetes de datos

Toda comunicación se divide en pequeños paquetes que contienen información necesaria para llegar a su destino.

Cada paquete está compuesto por:

- Header
- Payload
- Trailer (cuando aplica)

---

### Direcciones IP y protocolos

Las direcciones IP identifican los dispositivos dentro de una red.

Los protocolos establecen las reglas de comunicación entre ellos.

Entre los protocolos estudiados destacan:

- TCP
- UDP
- ICMP
- HTTP
- HTTPS
- DNS
- TLS

---

### Captura de paquetes

Las capturas de paquetes (PCAP) permiten almacenar el tráfico de red para su análisis posterior.

Estas capturas constituyen una fuente importante de evidencia durante investigaciones de seguridad.

---

### tcpdump

tcpdump es una herramienta de línea de comandos utilizada para capturar tráfico de red en sistemas Linux y Unix.

Permite:

- Capturar paquetes.
- Aplicar filtros.
- Guardar archivos PCAP.
- Analizar tráfico en tiempo real.

---

### Wireshark

Wireshark es un analizador gráfico de protocolos de red.

Permite:

- Abrir archivos PCAP.
- Analizar protocolos.
- Aplicar filtros avanzados.
- Seguir conversaciones TCP.
- Investigar incidentes.

---

## Lo más importante aprendido

- Comprender cómo circula la información por una red.
- Interpretar la estructura de un paquete.
- Analizar encabezados IPv4.
- Utilizar tcpdump para capturar tráfico.
- Utilizar Wireshark para analizar capturas.
- Aplicar filtros para localizar información relevante.

---

## Aplicación en ciberseguridad

Estos conocimientos son fundamentales para:

- Análisis forense.
- Respuesta a incidentes.
- Threat Hunting.
- Detección de malware.
- Investigación de ataques.
- Monitoreo de redes.

---

## Conclusión

Comprender el tráfico de red y saber interpretar paquetes constituye una de las habilidades más importantes para cualquier profesional de ciberseguridad. Herramientas como tcpdump y Wireshark permiten transformar grandes cantidades de datos en información útil para detectar amenazas y responder a incidentes de manera eficiente.
