---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 🆚 Agentforce Service Agent frente a Einstein Bots

| | 🎧 Agentforce Service Agent | 🤖 Einstein Bots |
|---|---|---|
| ⚙️ **Setup** | Rápido, con **subagentes y acciones prediseñados**. IA generativa + LLMs: conversa casi como un humano | Hay que **entrenar modelos de lenguaje (NLMs)** y **diseñar diálogos** a mano |
| 🔧 **Mantenimiento** | Ajustar unos pocos subagentes, acciones e instrucciones, o crear nuevos. Se mejora **iterando instrucciones en lenguaje natural** | **Alto**: mantener diálogos e intents y entrenar nuevos a medida que crecen las solicitudes |
| 🧠 **Contexto y excepciones** | Entiende lenguaje humano, responde **preguntas de seguimiento y excepciones no planeadas**. Tiene el **contexto de toda la conversación** | No entiende lenguaje humano. **Solo responde a la última pregunta**, sin contexto de la conversación |
| 📚 **Knowledge** | [[📚 Agentforce Data Library]] con RAG: sin mapear campos | **Article answers**: mapeo manual de preguntas a campos de artículos |

## 🤔 ¿Cuándo sigue teniendo sentido Einstein Bots?
- 🏛️ Industrias **reguladas** que exigen procesos **explicables** y gobierno extra.
- 🎯 Cuando se necesitan flujos de conversación **deterministas** muy específicos, con diálogos e intents.

> ⚠️ Ojo de examen: si la pregunta habla de **regulación, explicabilidad o flujos deterministas**, la respuesta es **Einstein Bots**. Si habla de **contexto de toda la conversación, seguimiento o excepciones no planeadas**, es **Agentforce**.

## 🔁 Repaso #flashcards
¿Cuál es la diferencia de setup entre Service Agent y Einstein Bots?::Service Agent arranca con subagentes y acciones prediseñados sobre LLMs; Einstein Bots exige entrenar modelos de lenguaje y diseñar diálogos.
¿Cuál de los dos tiene contexto de toda la conversación?::Agentforce Service Agent. Einstein Bots solo responde a la pregunta más reciente.
¿Cuándo conviene todavía Einstein Bots?::En industrias reguladas que piden procesos explicables con más gobierno, o cuando se necesitan flujos deterministas con diálogos e intents.
¿Cómo se mejora el rendimiento de Service Agent?::Iterando y agregando instrucciones en lenguaje natural.
