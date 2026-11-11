---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-08
---
# 🎨 Personalizar Agentforce Sales Coach

Viene optimizado para primeros pitches, discovery, negociación, objeciones y propuestas. Se personaliza por **dos lados**:

| | Qué cambia | Dónde | Cómo |
|---|---|---|---|
| 🎭 **Role-Play** | Cómo se comporta el **comprador** simulado | Setup > **Agentforce Agents** > Sales Coach > Open in Builder | **Deactivate** → topic → **Add Instructions** → Save → **Activate** |
| 📝 **Feedback** | Qué evalúa y cómo responde el coach | **Prompt Builder** > prompt de la etapa (p. ej. *Get Negotiation/Review Stage Feedback*) | **Deactivate** → **Save as New Version** → editar → probar |

> ⚠️ Ojo de examen: hay que **desactivar** el agente o el prompt **antes de editarlo**. En role-play basta con tocar **topics e instrucciones**.

## 🎭 Ejemplo de role-play
Instrucción nueva para que el comprador mencione a un competidor (*ClearTech*) con mejor precio, pida comparación de funcionalidades e intente sacar mejor trato. (El módulo la agrega en el topic *Opportunity Coaching*.)

**Buenas prácticas de instrucciones** (ver [[📝 Instrucciones de razonamiento]]):
- Formatos condicionales o imperativos: **If… Then** / **Never… Instead** (*"Never ask the user for an ID. Instead, use the name…"*).
- Usar los **nombres exactos** de labels y acciones para que el LLM sepa qué función llamar.
- Las instrucciones viven **a nivel de topic, no de acción**: si una acción está en varios topics, **repetir** la instrucción.
- El subagente **Off Topic no se puede desactivar**.

## 📝 Ejemplo de feedback
Se agrega al prompt un **COMPETITOR_HANDLING_CHECKLIST** (reconocer al competidor sin despreciar la preocupación, resaltar diferenciadores, reencuadrar hacia las prioridades del cliente, manejar objeciones) y campos de la oportunidad con merge fields (`{!$Input:Opportunity.StageName}`, Probability, NextStep, `{!$Input:Transcript}`…). Salida: **Deal Summary · Key Strengths · Areas for Improvement · Next Steps**, en segunda persona y máximo 400 palabras.

**Buenas prácticas de prompts** (ver [[✨ Buenas prácticas de prompts]]):
- 🏷️ **Etiquetas de sección** y **delimitadores** para que el modelo sepa dónde mirar.
- 🕳️ Cuidado con **campos que pueden venir null**: dar valores por defecto o guardrails.
- 📏 **"within"** para acotar la longitud (*"within 50 words"*).
- 💪 **"must"** para obligar, **"must strictly"** para más fuerza, **you + must + verbo imperativo**, **"always"** para que no omita algo.

**Plantilla de prompt sugerida**: Objective/Goal → Grounding Data → Instructions → Expected Output → Guidelines for output style → Task closing.

## 🧪 Probar
| Qué | Dónde | Cómo |
|---|---|---|
| Prompt | Prompt Builder | Preview Settings → **Test Inputs** → pegar una transcripción → elegir oportunidad → **Preview** |
| Topics e instrucciones | Agentforce Builder | **Conversation Preview**: *"Let's do role play…"* y ver en el panel central qué acciones e instrucciones se invocan |

> 🛠️ Ejercicio completo de role-play + prompt (Asset Library, Agentforce Assets, <NEGOTIATION QUESTIONS>): [[🛠️ Personalizar el role-play de Sales Coach paso a paso]].

## 🔁 Repaso #flashcards
¿Cuáles son los 2 tipos de personalización de Sales Coach?::Role-Play (instrucciones de los topics) y Feedback (prompts en Prompt Builder).
¿Qué hay que hacer antes de editar el agente o un prompt de Sales Coach?::Desactivarlo.
¿Cómo se edita un prompt de fábrica de Sales Coach?::Deactivate y Save as New Version, luego editar y probar.
¿A qué nivel viven las instrucciones: topic o acción?::A nivel de topic; si una acción está en varios topics, hay que repetir la instrucción.
¿Qué formatos se recomiendan para instrucciones?::Condicionales o imperativos: If… Then y Never… Instead.
¿Qué palabra acota la longitud de la salida en un prompt?::"within" (por ejemplo, within 50 words).
¿Cómo se refuerza una orden en un prompt?::Con "must", más fuerte con "must strictly", y con you + must + verbo imperativo.
¿Para qué sirve "always" en un prompt?::Para que el LLM incluya la información aunque falte algún elemento.
¿Cómo se manejan campos que pueden venir null en un prompt?::Con valores por defecto o guardrails sobre cómo usarlos.
¿Cuáles son las partes de la plantilla de prompt sugerida para Sales Coach?::Objective/Goal, Grounding Data, Instructions, Expected Output, Guidelines for output style y Task closing.
¿Cómo se prueba un prompt de Sales Coach?::En Prompt Builder con Test Inputs (una transcripción) y Preview.
¿Dónde se ven las acciones e instrucciones invocadas al probar el role-play?::En el panel central del Agentforce Builder, usando Conversation Preview.
