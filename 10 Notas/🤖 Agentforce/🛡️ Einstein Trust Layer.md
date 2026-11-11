---
tipo: nota
tema: trust-layer
estado: nueva
debil: true
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-23
---
# 🛡️ Einstein Trust Layer

La **confianza es el valor número 1 de Salesforce**, y la Trust Layer (o Capa de confianza) es la forma de usar [[🧠 Modelos de lenguaje grandes (LLM)|LLM]] sin poner en riesgo los datos.

- 🧱 Es una **secuencia de pasarelas y mecanismos de recuperación** con controles de datos y de privacidad integrados en la experiencia de Salesforce.
- 🎯 Su objetivo: entregar IA que se **basa de forma segura en los datos de clientes y empresa**, sin introducir riesgos de seguridad.
- 🔎 Permite usar **RAG de forma segura**: personaliza las respuestas con los datos de la empresa y de los clientes (Salesforce + Data 360).
- 🤖 **Todo agente de Agentforce** llama al LLM pasando por la Trust Layer.
- 🔌 Esto incluye los modelos externos: ver [[🔌 Opciones de LLM en Salesforce]].

## 🔄 El viaje del prompt y de la respuesta

```text
📤 PROMPT ─► 🔐 Recuperación segura ─► 📥 Grounding dinámico ─► 🎭 Enmascarado ─► 🧱 Defensa del prompt
                                                                                        │
                                          🚪 LLM Gateway ── 🚫 Zero data retention ◄────┘
                                                │
📩 RESPUESTA ◄─ 📜 Audit trail + feedback ◄─ 🎭 Desenmascarado ◄─ ☣️ Detección de toxicidad
```

| Paso | Qué hace |
|------|----------|
| 🔐 **Recuperación segura de datos** | Solo trae datos a los que **el usuario tiene acceso** (respeta permisos y FLS) |
| 📥 [[📥 Grounding dinámico]] | Agrega al prompt información de los registros y de otras fuentes, vía [[🔎 Búsqueda semántica]] |
| 🎭 **Enmascarado de datos** | Cambia datos sensibles (PII, PCI) por marcadores antes de enviarlos al LLM |
| 🧱 [[🧱 Defensa del prompt]] | Barandillas que le dicen al LLM cómo comportarse |
| 🚫 **Zero data retention** | El proveedor externo **no guarda** prompts ni respuestas ni **entrena** con ellos |
| ☣️ **Detección de toxicidad** | Puntúa la respuesta en categorías dañinas (toxicidad, violencia, groserías…) |
| 🎭 **Desenmascarado** | Devuelve los datos reales a la respuesta |
| 📜 **Audit trail y feedback** | Guarda prompts, respuestas, puntajes de toxicidad y feedback en **Data 360** |

> ⚠️ Ojo de examen: preguntas tipo "¿qué componente evita que el proveedor del LLM se quede con los datos?" → **zero data retention**. "¿Dónde se revisa qué se envió al LLM?" → **audit trail en Data 360**. "¿Qué baja la probabilidad de una respuesta dañina?" → **prompt defense** (antes) y **toxicity detection** (después).

> [!note]- 🌐 Complementado con la web
> El enmascarado, zero data retention, toxicidad y audit trail vienen de la [guía de Trust Layer de Salesforce](https://developer.salesforce.com/docs/ai/agentforce/guide/trust.html). Trailhead (*LLM Data Masking in the Einstein Trust Layer*) confirma que el **enmascarado está desactivado para los agentes**; sigue aplicando a las funciones generativas embebidas.

📚 Cada paso en detalle: [[🔐 Recuperación segura de datos]] · [[🎭 Enmascarado de datos]] · [[🚫 Zero data retention]] · [[☣️ Detección de toxicidad]] · [[📜 Audit trail y feedback]]. Repaso de examen: [[🛡️ Trust Layer para el examen]].

## 🔁 Repaso #flashcards
¿Qué es la Einstein Trust Layer?::Una secuencia de pasarelas y mecanismos de recuperación, con controles de datos y privacidad, para usar IA generativa (y RAG) de forma segura en Salesforce.
¿Qué garantiza zero data retention?::Que el proveedor externo del LLM no guarda los prompts ni las respuestas, ni los usa para entrenar.
¿Dónde se guarda el audit trail de la Trust Layer?::En Data 360: prompts, respuestas, puntajes de toxicidad y feedback.
¿Qué hace el enmascarado de datos?::Reemplaza datos sensibles por marcadores antes de enviar el prompt al LLM y los restaura en la respuesta.
