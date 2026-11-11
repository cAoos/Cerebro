---
tipo: nota
tema: trust-layer
estado: nueva
debil: true
fuente: "[[2026-10 Agentforce Specialist]]"
creada: 2026-11-09
---
# ☣️ Detección de toxicidad

Después de que el LLM responde, la Trust Layer **puntúa la respuesta** (y también el prompt) con un modelo detector. Da un **puntaje general de seguridad** y un puntaje por **categoría**: toxicidad, odio, identidad, violencia, daño físico, contenido sexual y groserías.

- 📊 Los puntajes se guardan en el **audit trail en Data 360**, junto al prompt y la respuesta.
- 🔎 Para revisarlos: un **reporte o consulta del audit trail en Data 360**, filtrando por el **tipo de detector** (toxicity) y viendo los puntajes.
- 🧱 Es el control **posterior** al LLM. El **anterior** es la [[🧱 Defensa del prompt]].

## 🧪 Ejemplo
Un cliente insulta al agente de servicio y el LLM, al copiar el tono, genera una frase grosera. La respuesta queda con un puntaje alto en *profanity*. El equipo la encuentra en el reporte de Data 360 filtrando por el detector de toxicidad, y ajusta las instrucciones del agente.

> ⚠️ Ojo de examen:
> - "¿Cómo confirmo que la toxicidad se está manejando?" → **reporte del audit trail en Data 360 con filtro por tipo de detector**. No existe un "Toxicity Detection log" en Setup ni hace falta un flow que mande emails.
> - Prompt injection o jailbreak → **Prompt Defense**, no toxicidad ni enmascarado.

Parte de [[🛡️ Einstein Trust Layer]] · Guía: [[🛡️ Trust Layer para el examen]]

## 🔁 Repaso #flashcards
¿Cuándo actúa la detección de toxicidad?::Después del LLM: puntúa la respuesta (y el prompt) por categorías dañinas.
¿Dónde se ven los puntajes de toxicidad?::En el audit trail almacenado en Data 360, filtrando por tipo de detector.
¿Qué controla la toxicidad vs qué controla la defensa del prompt?::Toxicidad: puntúa la salida después del LLM. Defensa del prompt: barandillas antes del LLM contra injection/jailbreak.
