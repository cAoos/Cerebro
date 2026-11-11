---
tipo: nota
tema: trust-layer
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-27
---
# 📥 Grounding dinámico

Es cuando la [[🛡️ Einstein Trust Layer]] **agrega al prompt información de los registros** en el momento de ejecutarlo, para que el LLM responda con contexto real de la empresa.

Dos formas de traer esa información:
- 🔤 **Merge fields**: datos de registros de Salesforce, como `{!conv_context}` o los `{!$Input:Objeto.Campo}` de [[🔗 Grounding de plantillas]].
- 🔎 [[🔎 Búsqueda semántica]]: busca información relevante en **otras fuentes de datos** (artículos, documentos) y la incluye sola.

> [!note]
> Dynamic grounding pulls data from your org, so it's important to make sure your data is kept current, accurate, and complete.

> 💡 Si los datos están desactualizados o incompletos, el LLM responde mal **aunque el prompt esté perfecto**. Por eso importa la [[🧹 Preparación de datos para IA]].

> ⚠️ Ojo de examen: el grounding pasa **después de la recuperación segura**, así que solo entran datos que **el usuario puede ver**.

## 🔁 Repaso #flashcards
¿Qué es el grounding dinámico?::Agregar al prompt, al ejecutarlo, información de los registros y de otras fuentes para dar contexto real al LLM.
¿Por qué importa la calidad de los datos en el grounding dinámico?::Porque los datos se traen de la org; si están desactualizados o incompletos, la respuesta del LLM sale mal.
