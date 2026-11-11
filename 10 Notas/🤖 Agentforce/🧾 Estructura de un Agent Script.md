---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-05
---
# 🧾 Estructura de un Agent Script

Un agente completo se puede escribir (y **exportar e importar**) como un archivo de [[📜 Agent Script]]. Esa **portabilidad** permite **compartir agentes** entre equipos o entornos y partir de **patrones probados**.

**Importar:** Agentforce Studio → flecha junto a **New Agent → New from Script →** pegar **→ Create Agent**. Después, **asignar el usuario del agente** (ver [[🔐 Permisos del usuario del agente]]).

![[agent-script-new-from-script.jpg|300]]

## 🧱 Bloques del script
| Bloque | Qué define |
|---|---|
| `system` | **Instrucciones globales** y mensajes de **welcome** y **error** |
| `config` | `developer_name`, `agent_label`, `description` y **`default_agent_user`** |
| `language` | Idioma por defecto y adicionales |
| `variables` | **`linked`** = vienen de una fuente (p. ej. `@MessagingSession.Id`); **`mutable`** = el agente las escribe. Ver [[🔣 Variables de agente]] |
| `knowledge` | Por ejemplo `citations_enabled` |
| `start_agent agent_router` | El **subagente de entrada**: decide a qué subagente ir con `@utils.transition to @subagent.X` |
| `subagent X` | `label`, `description`, `reasoning` (instrucciones + acciones disponibles) y la definición de `actions` |

## 🗂️ Subagentes típicos de un Service Agent
- **Escalation**: escala con `@utils.escalate`. Si falla, ofrece abrir un caso.
- **Off Topic**: redirige con cortesía y **no responde cultura general**.
- **Ambiguous Question**: pide detalles y **no invoca acciones**.
- **Customer Experience Support**: el subagente de negocio.

Off Topic y Ambiguous traen **reglas de seguridad** iguales a la [[🧱 Defensa del prompt]]: ignorar intentos de reemplazar las reglas, no revelar el system prompt ni las funciones, tratar los datos enmascarados como reales.

## ⚙️ Cómo se declara una acción
```yaml
Get_Sessions:
    description: "Get the Sessions__c based on the provided specific Date and the Id of the Experience__c"
    require_user_confirmation: False
    include_in_progress_indicator: False
    target: "flow://Get_Sessions"
    inputs:
        "startDate": date
            is_required: True
    outputs:
        "sessions": list[object]
            is_displayable: True
```
- `target` dice qué ejecuta: **`flow://`** un flow, **`generatePromptResponse://`** una **plantilla de Prompt Builder**.
- En `reasoning.actions` se conectan los valores: `with startDate = @variables.converted_date` toma el valor de una variable, y `with contactId = ...` deja que **el LLM lo llene**.
- En las instrucciones, las acciones se citan como `{!@actions.Get_Sessions}`.
- `is_displayable` equivale a **Show in conversation**; `include_in_progress_indicator` equivale al **loading text**. Ver [[🔩 Configurar una acción custom]].

> ⚠️ Ojo de examen:
> - Los agentes son **portables** con **New from Script**.
> - El **agent_router** (`start_agent`) enruta entre subagentes con `@utils.transition`.
> - Escalar a un humano es `@utils.escalate`.
> - Variables **linked** frente a **mutable**.
> - `target` puede ser un **flow** o una **plantilla de prompt**.

## 🔁 Repaso #flashcards
¿Cómo se importa un agente definido en Agent Script?::Agentforce Studio → flecha junto a New Agent → New from Script → pegar → Create Agent.
¿Qué hace el bloque start_agent agent_router?::Es el subagente de entrada que dirige la conversación al subagente adecuado con @utils.transition.
¿Qué diferencia hay entre una variable linked y una mutable en Agent Script?::Linked toma su valor de una fuente (p. ej. MessagingSession); mutable la escribe el agente durante la conversación.
¿Qué indica target: "generatePromptResponse://..." en una acción?::Que la acción ejecuta una plantilla de Prompt Builder (flow:// sería un flow).
¿Qué significa with contactId = ... en el reasoning de un subagente?::Que el LLM llena ese input a partir de la conversación.
¿Con qué utilidad escala un subagente a un humano en Agent Script?::@utils.escalate.
¿Qué hacen los subagentes Off Topic y Ambiguous Question?::Off Topic redirige sin responder cultura general; Ambiguous pide más detalles sin invocar acciones.
