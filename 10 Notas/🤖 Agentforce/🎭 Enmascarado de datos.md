---
tipo: nota
tema: trust-layer
estado: nueva
debil: true
fuente: "[[2026-10 Agentforce Specialist]]"
creada: 2026-11-09
---
# 🎭 Enmascarado de datos

Antes de que el prompt salga hacia el LLM, la Trust Layer **cambia los datos sensibles por marcadores** (por ejemplo `PERSON_0`, `EMAIL_0`). Cuando vuelve la respuesta, el **desenmascarado** pone otra vez los valores reales, así que el usuario ve todo normal.

## 🧩 Dos formas de detectar qué enmascarar
| Tipo | Cómo decide | Ejemplos |
|---|---|---|
| **Pattern-based** | Reconoce patrones con modelos y expresiones regulares | Nombres, emails, teléfonos, tarjetas de crédito, IBAN, números de identificación |
| **Field-based** | Usa la **clasificación de datos** de los campos (Data Sensitivity Level / Compliance Categorization) | Un campo custom marcado como *Confidential* o *PII* |

- ⚙️ Se configura en **Setup → Einstein Trust Layer → Configure Data Masking**, y se puede activar o no **por proveedor/modelo**.
- 🤖 **En los agentes de Agentforce el enmascarado está desactivado**: sigue funcionando en las funciones generativas embebidas (Service Replies, Work Summaries, plantillas de prompt…), pero los agentes necesitan los datos reales para razonar y ejecutar acciones. Para un agente, la protección se hace **antes**: permisos del usuario del agente, qué campos expone cada acción, instrucciones.

## ✅ Validar que enmascara bien
1. Revisa los datos de **audit trail** en Data 360: ahí se ve el prompt enmascarado que salió al LLM (ver [[📜 Audit trail y feedback]]).
2. Después de **agregar o quitar campos enmascarados**, prueba que las respuestas sigan siendo útiles: enmascarar de más le quita contexto al LLM y baja la calidad.

## 🧪 Ejemplo
Prompt original: *"Escribe a Laura Gómez (laura@acme.com) sobre su caso"*. Al LLM llega: *"Escribe a PERSON_0 (EMAIL_0) sobre su caso"*. La respuesta vuelve con los marcadores y la Trust Layer los reemplaza por *Laura Gómez* y *laura@acme.com*.

> ⚠️ Ojo de examen:
> - "Cambié los campos enmascarados, ¿y ahora?" → **probar que la calidad de las respuestas no empeoró**. No hay que apagar y prender la Trust Layer.
> - "¿Cómo valido qué se enmascaró?" → **audit data** (Data 360). El Flow Debugger o los debug logs **no**.
> - "¿Por qué el agente no enmascara?" → porque **en agentes no aplica**.

Parte de [[🛡️ Einstein Trust Layer]] · Guía: [[🛡️ Trust Layer para el examen]]

## 🔁 Repaso #flashcards
¿Qué hace el enmascarado de datos de la Trust Layer?::Reemplaza datos sensibles por marcadores antes de enviar el prompt al LLM; el desenmascarado restaura los valores reales en la respuesta.
¿Cuáles son los dos tipos de enmascarado?::Pattern-based (patrones como emails, teléfonos, tarjetas) y field-based (según la clasificación de sensibilidad del campo).
¿Aplica el enmascarado de la Trust Layer a los agentes de Agentforce?::No; está desactivado para agentes. Sigue aplicando a las funciones generativas embebidas y a las plantillas.
¿Qué hacer después de modificar los campos enmascarados?::Probar que las respuestas generadas con datos enmascarados siguen teniendo buena calidad.
¿Cómo se valida qué datos se enmascararon?::Revisando el audit trail (audit data) almacenado en Data 360.
