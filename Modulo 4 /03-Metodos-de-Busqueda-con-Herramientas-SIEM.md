# 03. Métodos de Búsqueda con Herramientas SIEM

## Descripción

Las herramientas **SIEM (Security Information and Event Management)** recopilan enormes cantidades de registros provenientes de múltiples fuentes. Para localizar rápidamente eventos relevantes, estas plataformas incorporan diferentes métodos de búsqueda que permiten filtrar, organizar y analizar la información.

En este tema se estudian los métodos de búsqueda utilizados por **Splunk** y **Google Security Operations (Chronicle)**, así como los conceptos fundamentales relacionados con el lenguaje de consultas SPL, las búsquedas UDM y las búsquedas sobre registros sin procesar.

---

# Importancia de las búsquedas en un SIEM

La principal función de un SIEM es ayudar a los analistas de seguridad a localizar rápidamente información útil durante una investigación.

Una búsqueda adecuada permite:

- Encontrar eventos específicos.
- Investigar incidentes de seguridad.
- Detectar actividades sospechosas.
- Correlacionar información de múltiples fuentes.
- Reducir el tiempo de respuesta ante incidentes.

Cada plataforma SIEM implementa sus propios mecanismos de búsqueda.

---

# Métodos de búsqueda en Splunk

Splunk utiliza un lenguaje propio llamado **Search Processing Language (SPL)** para consultar los registros almacenados.

Mediante SPL es posible:

- Buscar eventos.
- Filtrar resultados.
- Transformar información.
- Generar estadísticas.
- Crear gráficos.
- Correlacionar registros.

---

# Búsqueda básica en SPL

Una búsqueda sencilla puede consultar un índice específico y localizar un término determinado.

Ejemplo:

```spl
index=main fail
```

En esta consulta:

- **index=main** indica el índice donde se realizará la búsqueda.
- **fail** representa el término que se desea localizar.

El resultado incluirá todos los eventos del índice **main** que contengan la palabra **fail**.

---

# Índices (Indexes)

Un **índice** es el repositorio donde Splunk almacena los registros ya recopilados y procesados.

Cada índice contiene eventos que posteriormente pueden consultarse mediante SPL.

Trabajar sobre índices permite realizar búsquedas de forma rápida y organizada.

---

# Tuberías (Pipes)

Splunk utiliza el carácter:

```text
|
```

para conectar varios comandos en una misma consulta.

Cada comando utiliza el resultado del comando anterior.

Ejemplo:

```spl
index=main fail | chart count by host
```

Esta búsqueda realiza dos acciones:

1. Busca eventos que contienen la palabra **fail**.
2. Genera un gráfico con el número de eventos agrupados por host.

El uso de tuberías permite construir consultas más complejas sin realizar varias búsquedas independientes.

---

# Comodines (Wildcards)

Un **Wildcard** es un carácter especial que representa cualquier conjunto de caracteres.

En Splunk normalmente se utiliza el asterisco:

```text
*
```

Ejemplo:

```spl
index=main fail*
```

Esta consulta devuelve eventos que contienen palabras como:

- fail
- failed
- failure

El uso de comodines amplía el alcance de la búsqueda.

---

# Búsquedas exactas

Cuando se desea localizar una frase específica se utilizan comillas dobles.

Ejemplo:

```spl
"login failure"
```

En este caso únicamente se devolverán eventos que contengan exactamente esa frase.

---

# Métodos de búsqueda en Google Security Operations (Chronicle)

Google Security Operations (antes Chronicle) permite realizar diferentes tipos de búsqueda sobre los datos recopilados.

Los dos métodos principales son:

- Búsqueda UDM.
- Búsqueda sobre registros sin procesar (Raw Log Search).

---

# Búsqueda UDM (Unified Data Model)

La búsqueda **UDM** es el método predeterminado de Chronicle.

Antes de almacenar los registros, Chronicle los:

- recopila,
- analiza,
- normaliza,
- estructura.

Esto permite realizar búsquedas más rápidas y consistentes.

---

# Campos UDM

Los registros normalizados contienen diferentes campos utilizados para realizar búsquedas.

Entre los más importantes se encuentran:

## Entidades (Entities)

Describen los elementos involucrados en un evento.

Por ejemplo:

- Usuario
- Equipo
- Dirección IP
- Host

---

## Metadatos del evento (Event Metadata)

Incluyen información general como:

- Tipo de evento.
- Fecha.
- Hora.
- Origen.

---

## Metadatos de red (Network Metadata)

Contienen información relacionada con la comunicación de red.

Ejemplos:

- Dirección IP.
- Puerto.
- Protocolo.
- Conexión.

---

## Resultados de seguridad (Security Results)

Describen el resultado de un evento relacionado con la seguridad.

Por ejemplo:

- Malware detectado.
- Archivo puesto en cuarentena.
- Amenaza bloqueada.

---

# Ejemplo de búsqueda UDM

Una búsqueda sencilla para localizar inicios de sesión sería:

```text
metadata.event_type = "USER_LOGIN"
```

Esta consulta devuelve únicamente eventos relacionados con autenticaciones de usuarios.

---

# Búsqueda sobre registros sin procesar

Cuando la información deseada no se encuentra en los datos normalizados, Chronicle permite realizar búsquedas directamente sobre los registros originales.

Este método recibe el nombre de:

**Raw Log Search**

Al trabajar sobre datos sin normalizar:

- La búsqueda suele tardar más tiempo.
- Permite acceder a información que no fue estructurada durante la normalización.

---

# Expresiones regulares

Las búsquedas sobre registros sin procesar permiten utilizar **expresiones regulares (Regex)**.

Las expresiones regulares ayudan a localizar:

- Patrones.
- Direcciones IP.
- Correos electrónicos.
- Hashes.
- Nombres de archivos.
- Valores específicos.

Esto facilita investigaciones más precisas.

---

# Comparación entre Splunk y Chronicle

| Característica | Splunk | Google Security Operations |
|----------------|---------|----------------------------|
| Lenguaje propio | SPL | UDM Search |
| Datos normalizados | Sí | Sí |
| Búsqueda sobre registros originales | Sí | Sí (Raw Log Search) |
| Uso de tuberías | Sí | No aplica |
| Uso de comodines | Sí | Sí |
| Soporte para expresiones regulares | Sí | Sí |

---

# Buenas prácticas

- Definir correctamente los criterios de búsqueda.
- Utilizar índices adecuados.
- Aprovechar la normalización de los datos.
- Emplear comodines únicamente cuando sean necesarios.
- Utilizar expresiones regulares para búsquedas específicas.
- Refinar progresivamente las consultas para reducir resultados innecesarios.
- Conocer la sintaxis propia de cada plataforma SIEM.

---

# Resumen

Las plataformas SIEM proporcionan herramientas de búsqueda que permiten localizar rápidamente eventos relevantes entre grandes volúmenes de registros. Splunk utiliza el lenguaje **SPL**, mientras que Google Security Operations emplea búsquedas **UDM** y búsquedas sobre registros sin procesar. Dominar estos métodos permite a los analistas investigar incidentes con mayor rapidez y precisión.

---

# Conceptos clave

- SIEM
- SPL (Search Processing Language)
- Índice (Index)
- Pipe
- Wildcard
- Búsqueda exacta
- UDM
- Unified Data Model
- Raw Log Search
- Entidades
- Event Metadata
- Network Metadata
- Security Results
- Expresiones regulares (Regex)
- Chronicle
- Splunk
```
