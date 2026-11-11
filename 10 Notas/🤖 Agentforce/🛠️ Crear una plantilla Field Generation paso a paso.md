---
tipo: nota
tema: prompts
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-05
---
# 🛠️ Crear una plantilla Field Generation paso a paso

Proyecto práctico: un campo **Quick Summary** en el **Caso** que el LLM llena con un resumen corto de los comentarios, el asunto, la prioridad y el tipo. La teoría está en [[🏷️ Plantilla Field Generation]].

## 0️⃣ Encender Agentforce Studio
**Setup → Quick Find: Salesforce Go →** buscar **Agentforce Studio → Get Started → Turn On → Confirm**. Espera a que el botón diga **On** y refresca.

![[quick-summary-salesforce-go-agentforce-studio.jpg|500]]

## 1️⃣ Crear la plantilla
**App Launcher → Agentforce Studio → Prompt Templates → New Prompt Template**

| Campo | Valor |
|---|---|
| Prompt Template Type | **Field Generation** |
| Name / API Name | Quick Summary / `Quick_Summary` |
| Description | A short summary of case details |
| Object | **Case** |
| Object Field | **Quick Summary** |

## 2️⃣ Escribir el prompt y elegir el modelo
Primero va el texto con **marcadores en mayúsculas**: objetivo, límite de tamaño y guardrails.

```text
Summarize the concatenation of the contents of the comment bodies of COMMENTS along with the text from SUBJECT, the case priority which is PRIORITY, and the case type which is TYPE. Keep the response to a single short paragraph.
```

![[quick-summary-prompt-con-placeholders.jpg|500]]

Modelo: **OpenAI GPT 4 Omni Mini**, en la lista **Models** del panel de propiedades.

![[quick-summary-modelo-gpt4o-mini.jpg|300]]

## 3️⃣ Cambiar los marcadores por merge fields
Pon el cursor delante del marcador, abre **+ Insert Resource → Case →** el campo, y borra el marcador. El merge field queda en **azul**.

![[quick-summary-recursos-case.jpg|400]]

```text
Summarize the concatenation of the contents of the comment bodies of RelatedList: Case.CaseComments along with the text from Input:Case.Subject, the case priority which is Input:Case.Priority, and the case type which is Input:Case.Type.
Keep the response to a single short paragraph.
```

- `Input:Case.Campo` es un **campo del registro**.
- `RelatedList: Case.CaseComments` es una **lista relacionada** y sale en **otro color**.

## 4️⃣ Probar y activar
**Preview → Inputs → Related Record** (caso 00001002) **→ Preview**. Revisa la *Generated Response* y luego **Activate**. Ver [[👁️ Vista previa de una plantilla]].

![[quick-summary-related-record-preview.jpg|400]]
![[quick-summary-respuesta-generada.jpg|500]]

> 💡 Que el LLM conteste distinto al mismo prompt es **normal**.

## 5️⃣ Ponerla en la página con Dynamic Forms
1. En el caso: **⚙️ → Edit Page**, clic en el componente **Record Detail**.
2. En el panel de propiedades: **Upgrade Now** para pasar a **Dynamic Forms**, elegir **Case Layout** y **Finish**.
3. Clic en el campo **Quick Summary**; en **Prompt Template** elige **Quick Summary**.
4. **Save → Activate → Assign as Org Default →** **Desktop and phone** **→ Save**.

![[quick-summary-record-detail-upgrade.jpg|400]]
![[quick-summary-campo-plantilla-asignada.jpg|300]]

## 6️⃣ Usarla
El lápiz de editar del campo ahora tiene una **estrellita ✨**. Edita el campo y pulsa el icono de Einstein. Se abre el **overlay de Einstein** con la sugerencia: puedes **seguir conversando para refinarla** o darle **Use**. Después, **Save**.

![[quick-summary-campo-icono-einstein.jpg|300]]
![[quick-summary-overlay-einstein-resumen.jpg|400]]

> ⚠️ Ojo de examen:
> - Agentforce Studio se enciende desde **Salesforce Go**.
> - La plantilla tiene que estar **activa** antes de asignarla.
> - Para asignarla a un campo, la página tiene que usar **Dynamic Forms**: se convierte el Record Detail con **Upgrade Now**.
> - El usuario **revisa y puede refinar** la sugerencia en el overlay antes de aceptarla.

## 🔁 Repaso #flashcards
¿Desde dónde se enciende Agentforce Studio en una org?::Setup → Salesforce Go → buscar Agentforce Studio → Get Started → Turn On.
¿Cómo se convierte un Record Detail para asignar una plantilla a un campo?::Con Upgrade Now en Lightning App Builder, que lo pasa a Dynamic Forms.
¿Cómo se ve un merge field de lista relacionada en Prompt Builder?::RelatedList: Case.CaseComments, en un color distinto al de los campos Input.
¿Qué indica la estrellita junto al lápiz de un campo?::Que el campo tiene una plantilla Field Generation asignada y se puede llenar con Einstein.
¿Qué puede hacer el usuario con la sugerencia en el overlay de Einstein?::Revisarla, seguir conversando para refinarla o aceptarla con Use.
¿Qué hay que hacer con la plantilla antes de asignarla a un campo?::Activarla.
