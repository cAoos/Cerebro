---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-08
---
# 🪄 Agentforce Service Assistant

Agente **asistivo** (no autónomo) **para los agentes de servicio**, en la **página del Case** como **Lightning web component**. Da un **resumen del caso** y una **guía paso a paso** para resolverlo: el **service plan**. Es un agente **para empleados**.

> 🔄 **Ojo con la versión**: el módulo describe la **experiencia legacy** (plan sugerido, no conversacional, solo en el **legacy Agentforce Builder**). Salesforce avisa que Service Assistant **ya es un agente conversacional en tiempo real** y que el módulo se actualizará.

![[service-assistant-componente.png]]

## 🧠 Tres fuentes de grounding
| Fuente | Cómo entra |
|---|---|
| 📜 **Políticas de la empresa** | Convertidas en **subagentes e instrucciones** ([[🧷 Instrucciones para Service Assistant]]) |
| 📂 **Datos del caso** | **Service AI Grounding**: campos del Case (Subject, Description) + **Case Emails** y **Case Comments** |
| 📚 **Knowledge** | [[📚 Agentforce Data Library]] con **RAG**: agrega pasos al plan desde los artículos; solo soporta **Knowledge** como fuente |

**No soporta** como grounding los **casos relacionados** ni el **case feed**.

![[service-assistant-adl-subagentes.png]]

## 🗺️ Ciclo del service plan
1. Al guardar cambios en Subject o Description, crea el **resumen** (*service plan summary state*). Botón **Sync** si no arranca.
2. **Draft Plan** (hasta ~2 min): pasos en secciones lógicas (en la captura: *Gather Information, Work the Case, Resolve the Case, Wrap Up*) con **checkboxes** que se guardan solos.
3. **Redraft Plan** aparece con información nueva del caso o instrucciones nuevas, **solo si ningún paso está marcado**.

![[service-assistant-resumen.png]]
![[service-assistant-plan.png]]

## ⚙️ Reglas clave
- 🚫 **No ejecuta acciones**: el agente de servicio hace cada paso. Si agregas acciones, se usan **como grounding**, igual que instrucciones.
- 🎟️ **Eligibility criteria obligatorios**: un flow decide qué casos reciben plan ([[🎟️ Eligibility criteria de Service Assistant]]).
- 🧪 **No se prueba** en el Agentforce Builder ni en **Testing Center**: se prueba **en la página del Case** redactando un plan.
- ✏️ Para editar subagentes o instrucciones hay que **desactivar y reactivar** el agente.
- 🧩 Opcionales: **Quick Actions** (automatizan tareas de un paso), **Similar Cases**, grounding de **Messaging and Voice**.

> ⚠️ Ojo de examen: casos que **piden cuidado extra** (datos sensibles, varios sistemas, alta duración) son el uso ideal. Si una política **no está en las instrucciones, no estará en el plan** (salvo que la cubra Knowledge).

Práctica: [[🛠️ Configurar Service Assistant paso a paso]].

## 🔁 Repaso #flashcards
¿Qué es Agentforce Service Assistant?::Un agente asistivo para agentes de servicio, en la página del Case, que da un resumen y un service plan paso a paso.
¿Service Assistant es autónomo?::No: es asistivo; sugiere pasos que el agente de servicio ejecuta.
¿Cuáles son las 3 fuentes de grounding de Service Assistant?::Subagentes e instrucciones (políticas), Service AI Grounding (datos del caso) y Agentforce Data Library (Knowledge).
¿Qué no soporta Service Assistant como grounding?::Casos relacionados y el case feed.
¿Qué fuente de datos soporta la Data Library en Service Assistant?::Solo Knowledge.
¿Qué pasa si agregas acciones a Service Assistant?::Se usan como grounding adicional, igual que instrucciones; no se ejecutan.
¿Dónde se prueba Service Assistant?::En la página del Case redactando un plan; no en el Builder ni en Testing Center.
¿Cuándo aparece el botón Redraft Plan?::Cuando hay información nueva del caso o instrucciones nuevas, y ningún paso está marcado como completo.
¿Qué hay que hacer para editar subagentes de Service Assistant?::Desactivar el agente y luego reactivarlo.
¿Qué genera Service Assistant al guardar cambios del caso?::Un resumen del caso (service plan summary state).
¿Qué incluye Service AI Grounding para el Case?::Campos requeridos Subject y Description, y opcionalmente Case Emails y Case Comments.
