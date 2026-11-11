---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# ⚡ Acciones de agente

**Tareas individuales** que el agente realiza al hacer su trabajo, como pedirle al usuario su número de cuenta. Viven dentro de los [[🗂️ Subagentes]]; un agente puede tener **una o varias**.

## 📝 Instrucciones de las acciones
Le dicen al agente **qué hace la acción**. El **nombre, la descripción, las entradas y las salidas** determinan **cuándo y cómo** se usa. **Mejores instrucciones = acciones más predecibles.**

## 📦 Acciones estándar
Biblioteca de Salesforce; algunas para todos, otras con licencias extra. Algunas son **acciones de sistema**: fundamentales y **no se pueden eliminar**.

| Acción | 🧪 Ejemplo |
|--------|-----------|
| 🔎 **Consultar registros** | "Encuentra las oportunidades abiertas que cierran este trimestre" |
| 📝 **Resumir registros** | "Resume la negociación de Acme" (un solo registro) |
| ✉️ **Elaborar o revisar correos** | "Escribe un correo de introducción para Steve de Acme" |
| 📚 **Responder preguntas con Knowledge** | "¿Cuál es la política de devolución pasados 30 días?" (**requiere licencia de Knowledge**) |

De serie, un agente también puede **encontrar y actualizar registros** y **agregar datos** de Salesforce.

## 🛠️ Acciones personalizadas
Se construyen con **tecnología de la plataforma que ya conoces**:

| Base | 🧪 Ejemplo |
|------|-----------|
| 🌊 **Flujo iniciado automáticamente** (autolaunched) | Iniciar una devolución · llamar APIs de MuleSoft |
| 💻 **Apex invocable o REST** | Llamar una app del clima o una API de terceros |
| ✍️ **Plantilla de solicitud** (prompt template) | Generar correos de ventas (ver [[🧾 Tipos de plantillas de Prompt Builder]]) |
| 🌐 **Servicios externos** (External Services) | Conectar una API descrita con OpenAPI |

> 💡 Si ya tienes un **flow** que recomienda productos, lo conviertes en acción **en unos clics**. Con Apex o flows también accedes a datos de terceros vía **Data 360**.

> ⚠️ Ojo de examen: las 4 bases de una acción personalizada: **Flow autolanzado · Apex invocable/REST · prompt template · External Services**. Proceso de negocio → **Flow**; generar texto → **prompt template**; lógica compleja → **Apex**. "Responder con Knowledge" **requiere licencia de Knowledge**.

Componente de [[🤖 Agentforce]].

## 🔁 Repaso #flashcards
¿Qué es una acción de agente?::Una tarea individual que realiza el agente, como pedir el número de cuenta o iniciar una devolución.
¿Qué determina cuándo y cómo se usa una acción?::Sus instrucciones: nombre, descripción, entradas y salidas.
¿Con qué se crean acciones personalizadas?::Flows iniciados automáticamente, Apex invocable o REST, plantillas de solicitud y External Services.
¿Qué son las acciones de sistema?::Acciones estándar fundamentales que no se pueden eliminar.
¿Qué requiere la acción "Responder preguntas con Knowledge"?::Una licencia de Knowledge.
