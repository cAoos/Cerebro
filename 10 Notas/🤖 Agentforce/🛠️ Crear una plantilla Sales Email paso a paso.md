---
tipo: nota
tema: prompts
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-05
---
# 🛠️ Crear una plantilla Sales Email paso a paso

Proyecto práctico: un **correo de bienvenida** a un huésped de Coral Cloud Resorts recién llegado, con los datos de su reserva. Es uno de los [[🧾 Tipos de plantillas de Prompt Builder]]: una plantilla **reutilizable** que sirve a **muchos vendedores**, para distintos productos y clientes.

## 0️⃣ Encender Einstein y los Sales Emails
1. **Setup → Einstein Setup →** el toggle **Turn on Einstein** en **On**, y refresca.
2. **Setup → Einstein for Sales →** activa el toggle de **Sales Emails**.

![[sales-email-einstein-setup.jpg|300]]
![[sales-email-einstein-for-sales.jpg|400]]

## 1️⃣ Preparar los datos
Para que el correo traiga los datos de la reserva, hace falta una relación:
- **Object Manager → Guest Event → Fields & Relationships → New → Lookup Relationship →** *Related To*: **External Reservation**.
- Crear una External Reservation (check-in, check-out, *Room Type* = Suite) y asociarla al Guest Event **GE-00000001**.

## 2️⃣ Crear la plantilla
**Setup → Prompt Builder → New Prompt Template**

| Campo | Valor |
|---|---|
| Type | **Sales Email** |
| Name / API Name | Welcome Guest / `Welcome_Guest` |
| Recipient | **Contact** |
| Related Object | **Guest Event** |

![[sales-email-nueva-plantilla.jpg|400]]

> 💡 Sales Email trae **entradas fijas**: **Sender** (el usuario que envía), **Recipient** (Contact o Lead) y un **Related Object** opcional.

## 3️⃣ El prompt
Define el **rol** (recepcionista), el **remitente**, el **tono** (claro, voz activa, sin relleno), el **asunto** (que suba la tasa de apertura) y el **formato del cuerpo**:

```text
You're a receptionist for the Coral Cloud Resorts hotel.
Your name is {!$Input:Sender.Name}, with phone {!$Input:Sender.Phone} and email {!$Input:Sender.Email}.
…
- First add a title that includes the name of the guest and welcomes them: {!$Input:Recipient.Name}.
- Add a paragraph explaining the characteristics of the reservation, including its Check_in_Date__c, Check_out_Date__c, and Room_Type__c.
…
```

Los marcadores de la reserva se reemplazan con **+ Insert Resource → Guest Event → External Reservation →** el campo:

```text
Input:Guest_Event__c.External_Reservation__r.Check_in_Date__c
Input:Guest_Event__c.External_Reservation__r.Check_out_Date__c
Input:Guest_Event__c.External_Reservation__r.Room_Type__c
```

Modelo: **GPT 4 Omni Mini**.

![[sales-email-workspace.jpg|500]]

> 💡 Contact y User viven en el **CRM**. La reserva es una lista relacionada que se expuso en el CRM con **enriquecimiento de Data 360**.

## 4️⃣ Previsualizar y activar
**Preview Settings:** Recipient = Sofia Rodriguez, Related Record = GE-00000001 **→ Preview → View Rendered Response**. Ahí se comparan la **Resolution** (el prompt con los datos ya puestos, ver [[👁️ Vista previa de una plantilla]]) y la **Response** (asunto y cuerpo).

![[sales-email-rendered-response.jpg|500]]

**Activate**: sin este paso **los usuarios no pueden usar** la plantilla.

![[sales-email-activar.jpg|500]]

## 5️⃣ Usarla (distribuir)
En el **Contacto → Activity →** sobre ![[sales-email-activity-email.jpg|25]] **Email →** elegir el correo **→ Draft with AI →** en *Use pre-made instructions…* elegir **Welcome Guest →** elegir el Guest Event **→ Continue**. Einstein redacta el borrador; el usuario lo revisa, puede ajustarlo y lo envía con **Done → Send**.

> ⚠️ Ojo de examen:
> - Para usar plantillas de correo hay que activar **Sales Emails** en **Einstein for Sales**.
> - Una Sales Email tiene **Recipient** (Contact/Lead) y un **Related Object** opcional; el **Sender** es el usuario.
> - Para traer datos de otro objeto en un merge field hace falta una **relación (lookup)**.
> - El usuario la usa con **Draft with AI** desde el compositor de email del registro.
> - **Activate** es obligatorio para que los usuarios la vean.

> 💲 Mismo **Draft with AI** para enviar cotizaciones con la plantilla *Create Quote Email*: [[🛠️ Crear un Quoting Agent paso a paso]].

## 🔁 Repaso #flashcards
¿Qué hay que activar en Setup para usar plantillas Sales Email?::Einstein (Einstein Setup) y Sales Emails en Einstein for Sales.
¿Qué entradas tiene una plantilla Sales Email?::Sender (usuario), Recipient (Contact o Lead) y un Related Object opcional.
¿Cómo usa un vendedor una plantilla Sales Email?::Desde Activity → Email del registro, con Draft with AI y eligiendo la plantilla en Use pre-made instructions.
¿Qué botón muestra el prompt resuelto junto a la respuesta en la vista previa?::View Rendered Response (Resolution y Response).
¿Por qué se creó un lookup de Guest Event a External Reservation en el proyecto?::Para poder traer los campos de la reserva como merge fields a través del objeto relacionado.
¿Qué pasa si no se activa la plantilla Sales Email?::Los usuarios no la pueden usar en la org.
