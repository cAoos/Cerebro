---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# 📏 Heurísticas de calidad de agentes

Las heurísticas clásicas (las **10 de Nielsen Norman**) miden cómo un humano navega una **interfaz estática**. Las **Agent Quality Heuristics** miden cómo un agente navega un **contexto dinámico**: no son un chequeo de usabilidad sino un **estándar de desempeño**. Le dan a la empresa una definición **compartida** de buena experiencia para evaluar a escala.

| Heurística | Pregunta de diagnóstico | Nivel |
|---|---|---|
| ✅ **Factual and Reliable** | ¿Es correcta y relevante, sin alucinaciones ni contradicciones con el contexto previo? | 🔴 **P0** |
| 🎯 **Effective** | ¿Cumple la **intención real** del usuario, aunque el sistema actúe como se diseñó? | 🟠 P1 |
| ❓ **Responsive** | ¿Hace **preguntas aclaratorias** si el prompt es vago? | 🟠 P1 |
| 🧠 **Memory and UI Context** | ¿Usa el **contexto de la página** y los turnos previos sin que el usuario repita? | 🟠 P1 |
| 🛡️ **Trusted** | ¿Opera dentro de sus **límites y autoridad**? ¿Evita solo deflectar sin dar **alternativas accionables**? | 🟠 P1 |
| 📖 **Teachable** | ¿Se ajusta ante **sentimiento negativo** ("eso no es lo que quise decir")? | 🟠 P1 |
| 🧭 **Decisive** | ¿Mueve al usuario con **dirección clara**, sin exponer complejidad interna, sin exceso de cautela ni parálisis? | 🟠 P1 |
| 💬 **Conversational** | ¿Lenguaje simple, sin ruido ni verbosidad? | 🟡 P2 |
| 🎨 **Consistent** | ¿Voz de marca, terminología y formato consistentes entre turnos? | 🟡 P2 |
| ♿ **Approachable** | ¿Inclusivo, **accesible (WCAG 2.2)** y fácil de usar? | 🟡 P2 |
| 🙌 **Helpful** | ¿Da **acciones y siguientes pasos** en vez de mandar al autoservicio? | 🟡 P2 |

Truco para recordar: **solo Factual es P0**; las de **entender y mover al usuario** son P1; las de **forma** (tono, consistencia, accesibilidad, utilidad) son P2.

Los niveles se explican en [[🚨 Niveles de falla de un agente]] y se aplican en [[🚑 Triage de respuestas de un agente]].

> ⚠️ Ojo de examen: **Trusted (P1)** falla si el agente solo dice "no puedo" sin alternativa; **Helpful (P2)** falla si manda al autoservicio en vez de dar siguientes pasos. **Teachable** = reacciona al sentimiento negativo. **Responsive** = pregunta cuando el prompt es vago.

## 🔁 Repaso #flashcards
¿Qué miden las Agent Quality Heuristics frente a las de Nielsen Norman?::Cómo el agente navega un contexto dinámico (estándar de desempeño), no cómo un humano navega una interfaz estática.
¿Qué heurística de calidad mapea a P0?::Factual and Reliable.
¿Qué heurística evalúa si el agente hace preguntas aclaratorias ante un prompt vago?::Responsive (P1).
¿Qué heurística evalúa si el agente se ajusta cuando el usuario dice "eso no es lo que quise decir"?::Teachable (P1).
¿Qué heurística evalúa la accesibilidad (WCAG 2.2)?::Approachable (P2).
¿Qué heurística falla si el agente solo declara sus límites sin ofrecer alternativas?::Trusted (P1).
¿Qué heurísticas mapean a P2?::Conversational, Consistent, Approachable y Helpful.
