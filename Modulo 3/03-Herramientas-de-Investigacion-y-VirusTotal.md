# Herramientas de Investigación y VirusTotal

## Introducción

Una vez detectado un posible incidente de seguridad, el siguiente paso consiste en investigar los indicadores encontrados para determinar si realmente representan una amenaza. Para ello, los analistas utilizan diversas herramientas de investigación que permiten consultar información sobre archivos, direcciones IP, dominios, URL y otros indicadores de compromiso (IoC).

Estas herramientas recopilan información de múltiples fuentes, ayudando a validar amenazas, identificar campañas maliciosas y obtener inteligencia útil para responder a un incidente.

---

# ¿Qué son las herramientas de investigación?

Las herramientas de investigación permiten analizar indicadores de compromiso mediante bases de datos públicas y privadas, proporcionando información sobre amenazas conocidas y actividades maliciosas.

Su objetivo principal es ayudar a los analistas a responder preguntas como:

- ¿Este archivo es malicioso?
- ¿Esta dirección IP ha sido reportada anteriormente?
- ¿Este dominio participa en campañas de phishing?
- ¿Esta URL distribuye malware?
- ¿Qué organizaciones han observado esta amenaza?

---

# VirusTotal

**VirusTotal** es una plataforma en línea que analiza archivos, direcciones IP, dominios, URL y hashes utilizando múltiples motores antivirus y fuentes de inteligencia de amenazas.

Es una de las herramientas más utilizadas por analistas SOC e investigadores de seguridad.

## Permite analizar

- Archivos.
- Hashes (MD5, SHA-1 y SHA-256).
- Direcciones IP.
- Dominios.
- URL.

## Información proporcionada

- Resultado de múltiples motores antivirus.
- Relaciones entre indicadores.
- Comportamiento observado.
- Reputación.
- Detecciones históricas.
- Inteligencia compartida por la comunidad.

### Ventajas

- Fácil de utilizar.
- Información proveniente de múltiples proveedores.
- Amplia base de datos.
- Excelente para validar IoC.

### Limitaciones

- No detecta todas las amenazas.
- Los resultados pueden variar entre motores antivirus.
- No debe utilizarse como única fuente para tomar decisiones.

---

# MalwareBazaar

**MalwareBazaar** es una plataforma gratuita que recopila muestras reales de malware compartidas por investigadores y organizaciones de seguridad.

Su objetivo es facilitar el intercambio de información sobre software malicioso.

## Permite consultar

- Hashes.
- Familias de malware.
- Archivos maliciosos.
- Información técnica de muestras.

Es especialmente útil durante investigaciones forenses y análisis de malware.

---

# Urlscan.io

**Urlscan.io** permite analizar páginas web y URL sospechosas.

Cuando una dirección es analizada, la plataforma registra información como:

- Capturas de pantalla.
- Solicitudes HTTP.
- Recursos descargados.
- Dominios relacionados.
- Certificados SSL.
- Direcciones IP.

Es una herramienta ampliamente utilizada para investigar campañas de phishing y sitios maliciosos.

---

# Jotti Malware Scan

**Jotti Malware Scan** es un servicio gratuito que permite analizar archivos utilizando múltiples motores antivirus.

Su funcionamiento es similar al de VirusTotal y resulta útil para obtener una segunda opinión sobre un archivo sospechoso.

---

# Open Source Intelligence (OSINT)

**OSINT (Open Source Intelligence)** consiste en obtener información a partir de fuentes públicas disponibles en Internet.

Estas fuentes incluyen:

- Sitios web.
- Redes sociales.
- Bases de datos públicas.
- Registros DNS.
- WHOIS.
- Repositorios públicos.
- Blogs especializados.
- Informes de seguridad.

OSINT permite enriquecer una investigación sin necesidad de acceder a información confidencial.

---

# Crowdsourcing

El **Crowdsourcing** consiste en recopilar información proporcionada por investigadores, empresas y miembros de la comunidad de ciberseguridad.

Gracias a esta colaboración es posible:

- Compartir indicadores de compromiso.
- Detectar campañas de malware.
- Identificar nuevas amenazas.
- Mejorar la inteligencia de amenazas.

Muchas plataformas utilizan información generada por la comunidad para mantener sus bases de datos actualizadas.

---

# ¿Cómo ayudan estas herramientas durante una investigación?

Las herramientas de investigación permiten:

- Validar indicadores de compromiso.
- Obtener contexto sobre una amenaza.
- Correlacionar eventos.
- Confirmar si una amenaza es conocida.
- Priorizar incidentes.
- Compartir inteligencia con otros equipos.

---

# Comparación de herramientas

| Herramienta | Función principal |
|-------------|-------------------|
| VirusTotal | Analizar archivos, hashes, IP, dominios y URL. |
| MalwareBazaar | Compartir y consultar muestras de malware. |
| Urlscan.io | Analizar páginas web y URL sospechosas. |
| Jotti Malware Scan | Analizar archivos con múltiples motores antivirus. |
| OSINT | Obtener información de fuentes públicas. |
| Crowdsourcing | Compartir inteligencia entre la comunidad de seguridad. |

---

# Buenas prácticas

- Validar un indicador utilizando varias fuentes.
- No depender de una única herramienta.
- Correlacionar la información obtenida.
- Verificar la reputación de los indicadores.
- Documentar todos los hallazgos durante la investigación.
- Compartir indicadores relevantes con el equipo de seguridad.

---

# Resumen

Las herramientas de investigación permiten validar indicadores de compromiso y obtener información valiosa sobre amenazas conocidas. Plataformas como **VirusTotal**, **MalwareBazaar**, **Urlscan.io** y **Jotti Malware Scan**, junto con técnicas de **OSINT** y **Crowdsourcing**, ayudan a los analistas a comprender mejor un incidente, identificar amenazas y fortalecer la capacidad de respuesta de una organización.

---

# Conceptos clave

- VirusTotal
- MalwareBazaar
- Urlscan.io
- Jotti Malware Scan
- OSINT
- Crowdsourcing
- Indicador de Compromiso (IoC)
- Hash
- Dirección IP
- Dominio
- URL
- Inteligencia de amenazas

---

> **Siguiente tema:** [04 - Buenas Prácticas de Documentación](04-Buenas-Practicas-de-Documentacion.md)
