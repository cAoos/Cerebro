---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 📚 Agentforce Data Library

Le da al agente la capacidad de **responder en tiempo real con información de tu base de conocimiento**. Mejora la precisión y la confianza del cliente.

**Fuentes que soporta:** 📰 artículos de **Knowledge** (registros y campos) · 📎 **archivos subidos** (PDF) · 🌐 **web search** · 🧩 **custom retrievers**.

![[service-agent-data-library.jpg]]

## 🔍 Cómo funciona
- Usa **grounding con RAG** (retrieval augmented generation): indexa artículos y adjuntos para traer la información **más relevante y actualizada**. Ver [[📥 Grounding dinámico]].
- Al agregar una Data Library, **Salesforce construye automáticamente** la solución RAG que recupera datos **no estructurados (y estructurados)** de artículos y PDFs.
- Con lo indexado, el agente **verifica sus respuestas** contra políticas concretas: **no adivina**.
- Los LLMs procesan [[🗂️ Datos estructurados, semiestructurados y no estructurados|datos no estructurados]] (transcripciones, PDFs, audio, video, documentos legales) sin formato consistente.

## 🆚 Data Library frente a Article Answers (Einstein Bots)
| | 📚 Data Library (Agentforce) | 📰 Article Answers (Einstein Bots) |
|---|---|---|
| Datos | No estructurados: artículos, PDFs | **Muy estructurados** |
| Cómo entiende | LLM, entiende lenguaje natural sin entrenar | **NLP entrenado** para reconocer intents |
| Mapeo | **No hay que mapear campos** | **Mapeo manual** de preguntas (y sus variantes) a campos de cada artículo |
| Alcance | Cualquier pregunta que cubra el contenido | Solo preguntas **predefinidas**, solo artículos **publicados con campos llenos** |
| Actualización | Subir y listo: sin refrescar ni esperar build | Un **build** podía tardar **30 minutos o más** |

## 🛠️ Cómo se configura
En **Agentforce Builder** se usa una Data Library existente o se crea una nueva.
1. ☁️ **Data 360 debe estar activado antes** de crear la Data Library. Ver [[☁️ Data 360 para agentes]].
2. 📎 Subir archivos o enlazar artículos de Knowledge existentes. Eso es todo.

> 💡 La guided setup del [[🆘 Help Agent]] **crea sola una ADL** por defecto para los archivos subidos (PDF, DOCX, HTML, ~300 páginas) y activa Data 360 por ti.

> ⚠️ Ojo de examen: **prerrequisito = Data 360 activado**. La Data Library usa **RAG** y se configura desde el **Builder**. Si la opción menciona **mapear campos, entrenar NLP o builds**, es Einstein Bots (article answers), no Agentforce.

> 📮 El SDR también usa una data library (subir archivos con la FAQ). Un archivo puede tardar **hasta 24 h** en aparecer en las respuestas: [[📮 Agentforce SDR (Engagement agent)]].

> 🪄 En Service Assistant la Data Library solo soporta **Knowledge** y agrega pasos al service plan por RAG: [[🪄 Agentforce Service Assistant]].

## 🔁 Repaso #flashcards
¿Qué fuentes soporta una Agentforce Data Library?::Artículos de Knowledge (registros y campos), archivos subidos, web search y custom retrievers.
¿Qué técnica usa la Data Library para recuperar información?::Grounding con RAG: indexa artículos y adjuntos y Salesforce construye la solución automáticamente.
¿Qué debe estar activado antes de crear una Data Library?::Data 360.
¿Dónde se asigna o crea una Data Library para un agente?::En Agentforce Builder.
¿Qué limitaba a las article answers de Einstein Bots?::Datos muy estructurados, NLP entrenado, mapeo manual de preguntas a campos, solo artículos publicados con campos llenos y builds de 30+ minutos.
