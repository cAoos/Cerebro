---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# 💎 Comportamiento confiable de un agente

Un agente rápido que **alucina es un riesgo**; uno listo pero **difícil de hablar frustra**. El diseñador es **arquitecto de confianza**: define qué es un comportamiento correcto. El buen diseño **anticipa la fricción antes de que sea falla**. Meta: no solo completar la tarea, sino **la confianza**.

## 1️⃣ 🔍 Que sea claro (transparencia y predictibilidad)
El usuario **nunca debe adivinar** qué hace el agente ni por qué.
- 📚 **Explica su razonamiento** citando la fuente: "Según nuestra política de garantía…"
- 🎚️ **Fija expectativas**: "Puedo ver tu pedido, pero un reembolso completo lo procesa un colega humano."
- ⏱️ **Cuenta los pasos**: "Estoy buscando en el inventario… listo, lo encontré."

✅ Con transparencia, un error menor se ve como **un fallo técnico**; sin ella, como **un fallo de la marca**.

## 2️⃣ 🧠 Que sea consciente del contexto (relevancia y continuidad)
- 🔁 **Usa lo dicho antes**: no pregunta "¿en qué te ayudo?" a mitad de la solución.
- 📱 **Se adapta al rol y al canal**: no le habla igual a un técnico en el móvil que a un CEO en el escritorio.
- 📏 **Profundidad apropiada**: no un ensayo de 500 palabras para un sí/no.

✅ Evita la sensación **robótica** y ahorra tiempo.

## 3️⃣ 🛡️ Que genere confianza con respeto (seguridad, ética y control)
- 🙋 **Sabe cuándo escalar**: casos sensibles o complejos, **sentimiento muy negativo**, o tareas que requieren **permisos humanos** → **warm hand-off** a un humano.
- 🔐 **Respeta privacidad y permisos**: solo usa datos autorizados, **nunca comparte PII** indebidamente.
- 🚫 **No alucina ni se extralimita**: si no sabe, **lo dice**.

✅ **La confianza impulsa la adopción** y protege de riesgos legales y de reputación.

Es un proceso **iterativo**. Ver [[🎭 Diseño del comportamiento de un agente]], [[💥 Fallas de sistema frente a fallas de intención]] y [[🛡️ Einstein Trust Layer]].

> ⚠️ Ojo de examen: los tres principios son **claro, consciente del contexto y respetuoso**. Citar la fuente y fijar expectativas = **claro**. Recordar lo dicho y adaptarse al canal = **contexto**. Escalar con sentimiento negativo y no inventar = **respeto**.

## 🔁 Repaso #flashcards
¿Cuáles son los tres principios del comportamiento confiable de un agente?::Que sea claro, consciente del contexto y que genere confianza con respeto.
¿Qué hace un agente "claro"?::Explica su razonamiento citando la fuente, fija expectativas sobre lo que puede y no puede hacer, y cuenta los pasos que da.
¿Qué hace un agente consciente del contexto?::Usa lo dicho antes en la conversación, se adapta al rol y al canal y responde con la profundidad adecuada.
¿Cuándo debe un agente hacer un warm hand-off a un humano?::En casos sensibles o complejos, cuando el sentimiento del usuario es muy negativo o la tarea requiere permisos humanos.
¿Qué debe hacer un agente si no sabe la respuesta?::Decirlo, sin inventar una solución.
¿Por qué importa la transparencia ante un error?::Con transparencia el error se ve como un fallo técnico; sin ella, como un fallo de la marca.
