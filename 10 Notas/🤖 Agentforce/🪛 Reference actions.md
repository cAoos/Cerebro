---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-01
---
# 🪛 Reference actions

Las acciones custom no salen de la nada: se construyen **sobre funcionalidad de plataforma existente**, llamada **reference action**:
- **Apex** invocable o REST
- **Flows autolanzados**
- **Prompt templates**
- **External services**
- **APIs de MuleSoft**

Al crear la acción custom, **label, API name, instrucciones e inputs/outputs se llenan** con los de la reference action. Ver [[🔩 Configurar una acción custom]].

## ⚖️ Decisiones de diseño
| Eje | Opción A | Opción B |
|---|---|---|
| 🔒 vs ✨ | **Determinista**: Apex o flow, lógica de negocio y **resultado consistente** | **Basada en prompt**: prompt template para controlar cómo se redacta o usar el razonamiento del LLM (**resúmenes, análisis de sentimiento, grounding** en datos) |
| 🧱 vs 🏗️ | **Atómica**: tarea pequeña y única; el agente las **combina** libremente y se **reusan** entre subagentes | **Compuesta**: tarea compleja con subtareas; **controlas la secuencia exacta** |

Se pueden **combinar**: un flow que cancela la reserva y llama a un prompt template para el email con ofertas personalizadas.

📥📤 **Cada acción necesita al menos un input y al menos un output** (y por tanto el flow/Apex/prompt de base también). El agente decide si ya tiene los datos para dispararla.

📝 Las **instrucciones de la acción** dicen qué hace y **cuándo dispararla**: bien escritas = uso consistente.

## 🏝️ Acciones de Reservation Management
Get Reservation by Email (flow) · Get Reservation by Number (flow) · Send Reservation Confirmation (**Apex**) · Create or Update Reservation (flow) · Cancel Reservation (flow + **prompt template**) · Initiate Refund (flow con condiciones).

## 🧪 Probar
| Opción | Dónde |
|---|---|
| ✋ **Manual** | **Agentforce Builder** (ver [[🧪 Probar un agente en el Builder]]) |
| 📦 **En lote (batch)** | **Testing Center** |

¿Interpreta bien? ¿Lanza las acciones correctas? ¿Respuestas útiles? ¿Sigue las políticas? Si hay errores, **revisar permisos**.

> ⚠️ Ojo de examen: **resúmenes o sentimiento → prompt template**; **resultado consistente → flow o Apex**. **Atómica** = reutilizable y flexible; **compuesta** = controlas el orden. Mínimo **1 input y 1 output**. Pruebas en lote = **Testing Center**.

## 🔁 Repaso #flashcards
¿Qué es una reference action?::La funcionalidad de plataforma sobre la que se construye una acción custom: Apex invocable o REST, flows autolanzados, prompt templates, external services o APIs de MuleSoft.
¿Cuándo usar una acción determinista y cuándo una basada en prompt?::Determinista (flow/Apex) para resultados consistentes con reglas de negocio; basada en prompt para redactar, resumir, analizar sentimiento o hacer grounding.
¿Qué ventaja tiene una acción atómica?::El agente la combina libremente y se reutiliza entre subagentes.
¿Qué ventaja tiene una acción compuesta?::Controlas la secuencia exacta de pasos.
¿Cuántos inputs y outputs necesita una acción de agente?::Al menos uno de cada uno.
¿Dónde se prueban agentes en lote?::En Testing Center; la prueba manual es en Agentforce Builder.
