---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 🔩 Configurar una acción custom

Las [[⚡ Acciones de agente|acciones]] son las herramientas del [[🗂️ Subagentes|subagente]] para hacer el trabajo. En el Builder, dentro del subagente → **Add action** (o el **+** junto al subagente en el Explorer).

## 🆕 Crear una acción nueva
1. **+Create a custom action** → nombre y **descripción** (el agente la usa para decidir cuándo llamarla). → **Create and Open**.
2. **Reference Action Type**: el tipo, por ejemplo **Flow**. **Reference Action**: el flow concreto.
3. Configurar **inputs y outputs**:
   - 📥 Input → ✅ **Require Input to execute action**: no corre sin ese dato.
   - 📤 Output → ✅ **Show in conversation**: el resultado se muestra al usuario.
4. Opcional: **Show Loading text for this action**, el mensaje que ve el usuario mientras corre.
5. **Save**, y luego **Commit Version → Activate**.

> 🔑 Las descripciones de la acción y de sus inputs/outputs **forman parte del prompt** que se manda al LLM. Ejemplo completo: [[🛠️ Conectar un flow a un agente paso a paso]].

![[accion-reference-action-type.jpg]]
![[accion-inputs-outputs.jpg]]

## 📦 Reusar desde la Asset Library
Si la acción **ya existe**: **+** junto al subagente → **Add from Asset Library** → buscar → **Select** → **Add to Agent**.

## 🔐 Patrón: validar al cliente primero
En Coral Cloud, **Get Customer Details** valida **email + número de membresía** contra un Contact **antes** de cualquier otra acción, por seguridad. Se fuerza con las [[📝 Instrucciones de razonamiento]].

> ⚠️ Ojo de examen: **Require Input** = la acción no se ejecuta sin ese input. **Show in conversation** = el output se ve en el chat. Acción ya creada → **Asset Library**. La **descripción** de la acción guía al agente para elegirla.

## 🔁 Repaso #flashcards
¿Qué campo define que una acción custom es un Flow?::Reference Action Type = Flow, y Reference Action = el flow concreto.
¿Qué hace "Require Input to execute action"?::Impide que la acción se ejecute sin ese input.
¿Qué hace "Show in conversation" en un output?::Muestra el resultado de la acción al usuario en la conversación.
¿Cómo se agrega a un agente una acción que ya existe?::Desde la Asset Library: + junto al subagente → Add from Asset Library → Select → Add to Agent.
