---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-08
---
# 🎟️ Eligibility criteria de Service Assistant

El **portero** de los service plans: reglas en el **Decision element de un autolaunched flow** que deciden **para qué casos** se crea un plan (p. ej. origen Email, una cola concreta o prioridad High). Son **obligatorios**. Concepto en [[🪄 Agentforce Service Assistant]].

## 🛤️ Dos caminos
| Opción | Detalle |
|---|---|
| 📄 **Flow template** **Check Service Plan Eligibility** | Trae todo listo; decisión *Is Case Eligible for Service Plan?* con outcome `EligibleForServicePlan` |
| 🧱 **Autolaunched flow propio** | Para más control; debe tener **una entrada String** y **una salida Boolean** |

![[service-assistant-elegibilidad.png]]

## 🔗 Conectar el flow en Setup
En **Service Assistant > Customize Experience by Object > Add Eligibility Criteria**:
- **Flow Label**: el flow guardado.
- **Case ID Variable**: `caseId`.
- **Eligibility Result Variable**: `meetsEligibility`.
- **Ineligibility Reason**: `ineligibilityReason`.

![[service-assistant-elegibilidad-setup.png]]

> ⚠️ Ojo de examen: **sin eligibility criteria no hay plan**. Si construyes el flow desde cero: **autolaunched**, con **1 String de entrada** (el Case Id) y **1 Boolean de salida**. Patrón parecido a [[🛠️ Conectar un flow a un agente paso a paso]].

## 🔁 Repaso #flashcards
¿Qué son los eligibility criteria de Service Assistant?::Reglas en el decision element de un autolaunched flow que deciden qué casos reciben service plan.
¿Son opcionales los eligibility criteria?::No, son obligatorios para Service Assistant.
¿Cómo se llama el flow template de elegibilidad?::Check Service Plan Eligibility.
¿Qué requisitos tiene un flow de elegibilidad propio?::Ser autolaunched, con una entrada String y una salida Boolean.
¿Qué variables se mapean al conectar el flow de elegibilidad?::caseId, meetsEligibility e ineligibilityReason.
Da ejemplos de criterios de elegibilidad.::Casos que vienen por email, asignados a una cola concreta o con prioridad High.
