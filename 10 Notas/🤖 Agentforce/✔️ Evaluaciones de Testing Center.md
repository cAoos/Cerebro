---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[2026-10 Agentforce Specialist]]"
creada: 2026-11-08
---
# ✔️ Evaluaciones de Testing Center

**Agentforce Testing Center** prueba un agente **en lote**: corre muchas frases y compara lo que el agente hizo con lo que se esperaba. Complementa al panel Preview ([[🧪 Probar un agente en el Builder]]).

## 🧾 Un caso de prueba
| Campo | Qué es |
|---|---|
| 🗣️ **Utterance** | La frase del usuario |
| 🗂️ **Subagente (topic) esperado** | A qué subagente debería ir |
| ⚡ **Acciones esperadas** | Qué acciones debería ejecutar |
| 💬 **Resultado esperado** | Qué debería lograr o responder |

Los casos se **suben en CSV** o se **generan con IA** a partir de la configuración del agente (cientos de interacciones sintéticas).

## ⚖️ Cómo evalúa
| Evaluación | Cómo se decide |
|---|---|
| 🗂️ **Subagent (topic) assertion** | ¿Clasificó en el subagente esperado? |
| ⚡ **Action assertion** | ¿Ejecutó las acciones esperadas? (pasa si las reales **incluyen** las esperadas) |
| 💬 **Outcome / response evaluation** | Un **LLM como juez** compara la respuesta real con el resultado esperado. No es una comparación de texto exacto |

Las guías de terceros mencionan además **scorers de calidad** opcionales (completitud, coherencia, concisión, latencia, adherencia a instrucciones) puntuados por un LLM juez.

> ⚠️ Ojo de examen:
> - Testing Center **ejecuta las acciones de verdad** → correrlo en **sandbox**.
> - La respuesta se evalúa con **LLM-as-judge**, por **significado**, no por texto idéntico.
> - Si falla el **subagent assertion**, ajusta las **descripciones de clasificación**; si falla el **action assertion**, ajusta las **instrucciones de la acción**; si falla el **outcome**, revisa instrucciones, grounding o datos.

> [!note]- 🌐 Fuentes
> El detalle de *assertions* y *scorers* viene de guías de terceros ([open-exam-prep](https://open-exam-prep.com/study-guides/sf-agentforce/testing-center/testing-center-evaluations), [dev.to](https://dev.to/dipojjal/how-to-test-agentforce-agents-before-they-hit-production-44fj)). Confirmar en la Help oficial.

## 🔁 Repaso #flashcards
¿Qué compara un caso de Testing Center?::El subagente, las acciones y el resultado esperados con lo que hizo el agente.
¿Cómo se crean casos en Testing Center?::Subiendo un CSV o generándolos con IA.
¿Cómo se evalúa la respuesta en Testing Center?::Con un LLM como juez que compara por significado contra el resultado esperado.
¿Cuándo pasa un action assertion?::Cuando las acciones ejecutadas incluyen las esperadas.
Falla el subagent assertion: ¿qué ajustas?::Las descripciones de clasificación de los subagentes.
Falla el action assertion: ¿qué ajustas?::Las instrucciones (descripción) de las acciones.
¿Por qué correr Testing Center en sandbox?::Porque ejecuta las acciones reales.
