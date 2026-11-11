---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-07
---
# 🛰️ Enfoque API-first

La arquitectura headless se apoya en que **Salesforce diseña, construye y expone APIs robustas para cada funcionalidad**. Es la base del [[🧳 Headless Toolkit]].

## 🧱 Principios
| Principio | Qué significa |
|---|---|
| 🪟 **Decoupled architecture** | Lógica y datos **separados del diseño de pantalla** |
| ⚙️ **System of execution** | El CRM funciona como **motor de backend** para humanos **y** agentes |
| 🤖 **Agentic readiness** | Endpoints **limpios y deterministas**: el agente ejecuta tareas **sin navegador** |
| 🧩 **Developer flexibility** | Cada equipo arma **front ends propios y componibles** sobre las mismas capacidades |

## 🗂️ Tipos de API
| Necesidad            | API                                                                      |
| -------------------- | ------------------------------------------------------------------------ |
| Operaciones de datos | **REST**, **SOAP**, **Bulk**                                             |
| Metadata             | **Metadata API**                                                         |
| Tiempo real          | APIs de **eventos**                                                      |
| Patrones modernos    | **GraphQL**, **Named Queries**                                           |
| Por producto         | Por ejemplo **Connect REST API**: Search, B2B Commerce, Experience Cloud |

Se elige según el **patrón de integración** y el **volumen de datos**.

## 🧭 Apoyos
- 📖 El **developer portal** trae referencia, ejemplos de código, **rate limits** y versionado.
- 📮 **Postman collections oficiales** con autenticación preconfigurada y requests de ejemplo: explorar sin escribir código.
- 🎯 Compromiso de Salesforce: **superficie de API completa en cada funcionalidad** y **mensajes de error independientes de la UI**, para que los agentes **puedan actuar sobre ellos**.

> ⚠️ Ojo de examen: los cuatro principios son **decoupled architecture, system of execution, agentic readiness y developer flexibility**. "Que un agente ejecute sin navegador" → **agentic readiness**. Para volumen grande de datos → **Bulk API**.

> 🧯 Los errores explícitos también son paso obligatorio del [[🛫 Checklist antes de conectar herramientas headless]].

## 🔁 Repaso #flashcards
¿Qué significa que Salesforce sea API-first?::Que diseña, construye y expone APIs robustas para sus funcionalidades.
¿Cuáles son los cuatro principios del enfoque API-first?::Decoupled architecture, system of execution, agentic readiness y developer flexibility.
¿Qué es agentic readiness en el enfoque API-first?::Endpoints limpios y deterministas que dejan a los agentes ejecutar tareas sin navegador.
¿Qué es system of execution en el enfoque API-first?::El CRM funciona como motor de backend para interacciones de humanos y de agentes.
¿Qué APIs ofrece Salesforce para operaciones de datos?::REST, SOAP y Bulk.
¿Qué patrones modernos de API ofrece Salesforce?::GraphQL y Named Queries.
¿Qué da acceso programático a Search, B2B Commerce y Experience Cloud?::Connect REST API.
¿Por qué importan los mensajes de error independientes de la UI?::Porque los agentes pueden entenderlos y actuar sobre ellos.
