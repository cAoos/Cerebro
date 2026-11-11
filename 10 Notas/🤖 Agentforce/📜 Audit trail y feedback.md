---
tipo: nota
tema: trust-layer
estado: nueva
debil: true
fuente: "[[2026-10 Agentforce Specialist]]"
creada: 2026-11-09
---
# 📜 Audit trail y feedback

La Trust Layer guarda cada interacción generativa: el **prompt original**, el **prompt enmascarado**, la **respuesta**, los **puntajes de toxicidad** y el **feedback** del usuario (👍/👎 y comentarios). Todo eso vive en **Data 360** (antes Data Cloud), en un modelo de datos propio (DMOs de *GenAI Gateway Request/Response*, *Generation*, *Feedback*…).

## 🔛 Cómo se activa
1. **Data 360 aprovisionado** en la org. Sin Data 360 no hay dónde guardar el audit trail.
2. **Einstein Setup → Turn on Einstein** (IA generativa).
3. Activar la **recolección de audit y feedback**: *Einstein Audit, Analytics, and Monitoring Setup* (en versiones viejas, la página *Einstein Feedback*). Eliges el **data space** donde se guarda.
4. Los datos aparecen en Data 360 en **hasta 24 horas**.
5. Para verlos: instalar el paquete de **reportes y dashboard de Audit and Feedback**, o consultar los DMOs con el **Query Editor** de Data 360.

## 🔀 No confundir
| Necesito… | Uso |
|---|---|
| Ver qué prompt salió, cómo se enmascaró y qué respondió el LLM | **Audit trail** (Data 360) |
| Ver adopción y uso de un agente, qué topics y acciones elige | **Agentforce Analytics / Observability** ([[📈 Agentforce Observability]]) |
| Seguir paso a paso una sesión de un agente | **Session Tracing** (también en Data 360) |
| Saber si los usuarios están contentos con las respuestas | **Feedback** (parte del mismo audit) |

## 🧪 Ejemplo
Cumplimiento pide demostrar qué datos de clientes viajaron al LLM el mes pasado. El admin abre el dashboard de Audit and Feedback en Data 360, filtra por la plantilla de resumen de casos y muestra el prompt enmascarado de cada ejecución.

> ⚠️ Ojo de examen:
> - "Quieren reportar sobre audit y feedback" → **requiere Data 360 aprovisionado**. No van en objetos custom ni big objects.
> - "Ver qué prompt se envió, cómo se enmascaró y la respuesta" → **audit trail de la Trust Layer**. Los debug logs y Event Monitoring **no**.
> - "Monitorear el uso del agente y qué acciones asigna" → **Agentforce Analytics** (en el banco viejo: *Einstein Copilot Analytics*).

Parte de [[🛡️ Einstein Trust Layer]] · Guía: [[🛡️ Trust Layer para el examen]]

## 🔁 Repaso #flashcards
¿Dónde se almacenan el audit trail y el feedback de la IA generativa?::En Data 360 (antes Data Cloud); debe estar aprovisionado.
¿Qué guarda el audit trail de la Trust Layer?::Prompt original, prompt enmascarado, respuesta del LLM, puntajes de toxicidad y feedback del usuario.
¿Cuánto tarda en aparecer el audit data después de activarlo?::Hasta 24 horas.
¿Cómo se revisa el audit trail?::Con el paquete de reportes/dashboard de Audit and Feedback en Data 360, o consultando los DMOs con el Query Editor.
Monitorear el uso de un agente y las acciones que elige: ¿audit trail o Agentforce Analytics?::Agentforce Analytics (Observability); el audit trail es para prompts, enmascarado y respuestas.
