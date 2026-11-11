---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# 🩺 Evaluar el valor de un agente

Que un agente **funcione** no significa que **valga la pena**. El éxito no se mide con un benchmark del modelo, sino con el **valor que percibe el usuario** y la **confianza** que le tiene.

![[evaluacion-agente-funciona-vs-vale.jpg|500]]

**Ejemplo:** el usuario pregunta *"¿Cuál es el inventario actual de nuestro producto más vendido?"* y el agente responde *"No tengo acceso a la base de inventario; búscalo en el Supply Chain Dashboard"*.
- ⚙️ **Técnicamente es un éxito**: no alucinó, reconoció su límite y redirigió.
- 🙁 **Para el usuario es un fracaso**: no obtuvo lo que necesitaba para su tarea → "el agente no funciona".

Cuando el usuario dice que "no funciona", casi nunca habla de un error 404. Le faltan palabras para explicar por qué la conversación se sintió "rara", así que se queja en genérico.

**De éxito de sistema a éxito percibido:** las [[📏 Heurísticas de calidad de agentes]] miden si la respuesta es **valiosa, oportuna y confiable** como para que el usuario dependa de ella. Cada falla se mapea a un [[🚨 Niveles de falla de un agente|nivel de severidad]] y se corrige con [[🚑 Triage de respuestas de un agente|triage]].

Continúa lo de [[💥 Fallas de sistema frente a fallas de intención]].

> ⚠️ Ojo de examen: un agente que **no alucina y deflecta correctamente** puede seguir siendo un **fracaso para el usuario**. Lo que se evalúa es el **éxito percibido**, no solo que el código corra.

## 🔁 Repaso #flashcards
¿Qué mide realmente el éxito de un agente según Salesforce?::El valor que percibe el usuario y la confianza que deposita en él, no el benchmark del modelo.
Un agente dice "no tengo acceso, ve al dashboard". ¿Éxito o fracaso?::Técnicamente éxito (no alucinó), pero fracaso para el usuario porque no completó su tarea.
¿Qué diferencia hay entre éxito de sistema y éxito percibido?::El de sistema pregunta si el código corrió bien; el percibido, si la respuesta es valiosa, oportuna y confiable para el usuario.
