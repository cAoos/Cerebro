---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 📝 Instrucciones de razonamiento

El agente puede tener todas las [[⚡ Acciones de agente|acciones]], pero **no sabe cuándo ni cómo usarlas**. Las **reasoning instructions** del [[🗂️ Subagentes|subagente]] le dicen **qué hacer y cómo responder**.

## 🔗 Referenciar acciones
- En Script, una acción se nombra como **`{!@actions.Nombre_Accion}`**.
- En Canvas, se escribe **`@`** para abrir el **Resource Picker** → Actions → elegir la acción. **Hay que teclear la @**: copiar y pegar no lo dispara.

![[instrucciones-appropriate-action.jpg]]

**Ejemplo de Coral Cloud** (subagente Experience Management):
1. Para info de experiencias → correr **Get Experience Details** y resumir. Siempre **conocer al cliente** antes.
2. Cliente desconocido → pedir **email y número de membresía** y correr `{!@actions.Get_Customer_Details}` **antes de cualquier otra acción**.
3. Sesiones → `{!@actions.Get_Sessions}`, pedir la fecha y usar el **Id** del Experience__c, **no el nombre**.
4. Reservar → `{!@actions.Create_Experience_Session_Booking}` con los IDs de las acciones anteriores. Si hay varias sesiones, pedir que elija.

![[instrucciones-agent-script.jpg]]

## ✨ Ayuda de IA
- **Refinar** una instrucción: icono de **destellos** (sparkles) al pasar el mouse, o el comando **`/`**. Lo que se quita sale en **rojo**, lo que se agrega en **verde**, y tú **aceptas o rechazas**.
- ¿Error al hacer **Commit**? Escribir **"scan and fix"** en el Agentforce Assistant → **Accept All** → volver a hacer commit.

Canvas y Script están **sincronizados**: lo editado en Script aparece en Canvas. Luego **Commit → Activate** (ver [[🏷️ Versiones de un agente]]) y **Preview** (ver [[🧪 Probar un agente en el Builder]]).

> ⚠️ Ojo de examen: las acciones se citan con **`{!@actions.X}`**. Para forzar un orden (validar identidad primero) se usan **instrucciones**. "**scan and fix**" en el Assistant arregla errores comunes de commit. En **Live Test Mode** los cambios a datos **son reales**; en **Simulate** no.

> 🏋️ En Sales Coach: formatos **If… Then / Never… Instead**, nombres exactos de acciones, e instrucciones **a nivel de topic** (repetirlas si la acción está en varios): [[🎨 Personalizar Agentforce Sales Coach]].

## 🔁 Repaso #flashcards
¿Para qué sirven las reasoning instructions de un subagente?::Le dicen al agente cuándo y cómo usar las acciones y cómo responder.
¿Cómo se referencia una acción dentro de una instrucción en Agent Script?::{!@actions.Nombre_Accion}
¿Cómo se abre el Resource Picker en Canvas?::Tecleando @ (copiar y pegar no funciona).
¿Cómo pides a la IA que refine una instrucción?::Con el icono de sparkles o el comando /; muestra en rojo lo que quita y en verde lo que agrega, y tú aceptas o rechazas.
¿Qué hacer si el agente no deja hacer commit?::Escribir "scan and fix" en el Agentforce Assistant, aceptar los cambios y volver a hacer commit.
