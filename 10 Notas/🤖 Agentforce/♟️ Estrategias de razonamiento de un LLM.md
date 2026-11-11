---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-27
---
# ♟️ Estrategias de razonamiento de un LLM

Cuatro formas en que un [[⚙️ Reasoning engine]] hace razonar a un [[🧠 Modelos de lenguaje grandes (LLM)|LLM]]:

| | Estrategia | Idea clave |
|---|-----------|------------|
| 🔗 | **Chain-of-Thought (CoT)** | Romper un problema grande en **pasos pequeños enlazados** entre sí |
| 🔄 | **Reasoning and Acting (ReAct)** | Combina el razonamiento con **acciones**: no se queda en lo que el LLM sabe, sino que interactúa, **comprueba la información** y refina sus respuestas paso a paso con los comentarios de los usuarios → **menos alucinaciones** |
| 🌳 | **Tree of Thoughts (ToT)** | En vez de seguir un solo plan, **explora varios caminos en cada paso**, como una lluvia de ideas antes de elegir la mejor |
| 🗺️ | **Reasoning via Planning (RAP)** | **Simula resultados futuros**: predice cómo saldrán las acciones, explora alternativas y ajusta el plan sobre la marcha, como un estratega |

```text
🔗 CoT    A ─► B ─► C ─► ✅              (una cadena)
🔄 ReAct  pensar ─► actuar ─► observar ─┐ (un ciclo)
             ▲─────────────────────────┘
🌳 ToT        ┌─ B1
          A ──┼─ B2 ─► C ✅             (un árbol de opciones)
              └─ B3
🗺️ RAP    simular futuro ─► elegir ─► replanear
```

> ⚠️ Ojo de examen: la que **reduce alucinaciones** porque **verifica con acciones** es **ReAct**. Es la idea detrás de un agente que llama a actions, mira el resultado y decide el siguiente paso.

> 💡 CoT también sirve al escribir un prompt: pedirle al modelo "piensa paso a paso" (ver [[✨ Buenas prácticas de prompts]]).

## 🔁 Repaso #flashcards
¿Qué hace Chain-of-Thought (CoT)?::Rompe un problema grande en pasos pequeños enlazados.
¿Qué hace ReAct y por qué reduce alucinaciones?::Combina razonamiento con acciones: interactúa, comprueba la información y refina la respuesta paso a paso.
¿Qué hace Tree of Thoughts (ToT)?::Explora varios caminos posibles en cada paso antes de elegir el mejor.
¿Qué hace Reasoning via Planning (RAP)?::Simula resultados futuros, explora alternativas y ajusta el plan sobre la marcha.
