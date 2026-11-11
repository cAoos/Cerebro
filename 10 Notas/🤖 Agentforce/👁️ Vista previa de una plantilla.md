---
tipo: nota
tema: prompts
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-27
---
# 👁️ Vista previa de una plantilla

Antes de activar una plantilla se prueba con registros reales. La vista previa muestra **tres partes**:

| Parte | Qué muestra |
|-------|-------------|
| ✍️ **Prompt** | Lo que escribiste: instrucciones y recursos |
| 🔍 **Resolved Prompt** | El prompt **con los datos ya reemplazados** para el registro elegido: lo que **realmente se envía al LLM** |
| 💬 **Response** | Lo que contestó el LLM a partir del Resolved Prompt |

Cada prueba actualiza el Resolved Prompt, y así se va afinando la plantilla (el ciclo de [[✨ Buenas prácticas de prompts]]).

> ⚠️ Ojo de examen: si la respuesta sale mal, **revisa primero el Resolved Prompt**: ahí se ve si un merge field vino vacío o con un dato equivocado.

## 🔁 Repaso #flashcards
¿Qué es el Resolved Prompt?::El prompt con los merge fields ya reemplazados por los datos del registro: lo que realmente recibe el LLM.
¿Cuáles son las tres partes de la vista previa?::Prompt, Resolved Prompt y Response.
