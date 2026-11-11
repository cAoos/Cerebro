---
tipo: nota
tema: prompts
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-05
---
# 🛠️ Crear una plantilla Flex paso a paso

Proyecto práctico: un **newsletter de bienvenida** para los huéspedes de Coral Cloud Resorts, con los datos de su reserva y las actividades del resort. La teoría está en [[🧩 Plantilla Flex]].

## 0️⃣ Encender Einstein
**Setup → Einstein Setup →** el toggle **Turn on Einstein** en **On**, y refresca para ver los ajustes de admin.

![[flex-newsletter-einstein-setup.jpg|400]]

## 1️⃣ Crear la plantilla
**Setup → Prompt Builder → New Prompt Template**

| Campo | Valor |
|---|---|
| Type | **Flex** |
| Name / API Name | New Guest Newsletter / `New_Guest_Newsletter` |
| Description | Newsletter for incoming resort guests |

**Inputs (hasta 5)**, cada uno con *Source Type* = **Object**:

| Name / API Name | Objeto |
|---|---|
| Reservation | External Reservation |
| Experience | Experience |

> 💡 Elige los **API Names con cuidado**: los usan Apex y Flow cuando llaman a la plantilla.

## 2️⃣ Prompt con merge fields
Primero se escribe el prompt con marcadores `{…}`: rol (*Director of Fun*), objetivo, instrucciones numeradas, tono y cierre con llamada a la acción. Luego se reemplazan con **Insert Resource**:

![[flex-newsletter-recursos.jpg|300]]

```text
… writing a newsletter to welcome Input:Reservation.External_Guest__r.First_Name__c …
Check In: Input:Reservation.Check_in_Date__c
Check Out: Input:Reservation.Check_out_Date__c
Room Selection: Input:Reservation.Room_Type__c
Experience Name: Input:Experience.Name
Experience Location: Input:Experience.Location__c
Experience Details: Input:Experience.Description__c
```
- Se puede **navegar relaciones**: `Reservation > External Guest > First Name` da `External_Guest__r.First_Name__c`.
- Los recursos pueden venir del **CRM**, de **Data 360** o de **fuentes externas a través de Data 360**.
- Modelo: **OpenAI GPT 4 Omni Mini**.

## 3️⃣ Probar
**Preview**: elegir **un registro por cada input** (una Reservation y una Experience) y revisar la *Generated Response*.

**Límite:** con un input de tipo Experience solo entra **una** actividad, y el resort tiene varias. La solución es un flow: [[🌊 Template-Triggered Prompt Flow]].

## 4️⃣ Con el flow
Se borran los tres merge fields de Experience y se inserta **Insert Resource → Flows → Get Experience Newsletter Data**, que aparece como `Flow:Get_Experience_Newsletter_Data`. Luego **Save As → Save as a New Version**, Preview y **Activate**. Ahora el newsletter lista **todas** las actividades.

> ⚠️ Ojo de examen:
> - Flex **no tiene puntos de entrada predefinidos**: tú eliges los objetos (hasta 5 inputs) y la llamas desde **Apex, Flow, REST API o Agentforce**.
> - Sirve para PDFs, posts de redes, newsletters, emails, campos…
> - Si necesitas **varios registros** (una lista) en el prompt → **Template-Triggered Prompt Flow**.
> - Cambiar una plantilla activa → **Save as a New Version**.

## 🔁 Repaso #flashcards
¿Desde dónde se puede invocar una plantilla Flex?::Desde Apex, Flow, REST API o Agentforce.
¿Por qué importan los API Names de los inputs de una plantilla Flex?::Porque los usan Apex y Flow al llamar la plantilla.
¿Qué Source Type tienen los inputs de objeto en una plantilla Flex?::Object, con el objeto elegido (p. ej. External Reservation).
¿Cómo se llega a un campo de un registro relacionado en un merge field?::Navegando la relación en Insert Resource; queda como Input:Reservation.External_Guest__r.First_Name__c.
¿De dónde pueden venir los recursos de una plantilla?::Del CRM, de Data 360 o de fuentes externas a través de Data 360.
¿Cómo se guarda un cambio en una plantilla que ya existe?::Save As → Save as a New Version.
¿Qué hacer si el prompt necesita varios registros de un objeto, no solo uno?::Usar un Template-Triggered Prompt Flow que los recupere y los pase como prompt instructions.
