---
tipo: nota
tema: prompts
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-05
---
# 🌊 Template-Triggered Prompt Flow

Un tipo de flow que **solo se ejecuta desde una plantilla de Prompt Builder** y le pasa datos y texto. Sirve cuando el prompt necesita **lógica** o **varios registros**, por ejemplo **todas** las actividades de un resort y no solo una (ver [[🔗 Grounding de plantillas]]).

**Su capacidad única:** el elemento **Add Prompt Instructions**, que arma texto en Flow Builder y lo **manda a Prompt Builder**.

## 🧱 Cómo se arma
**App Launcher → Automation → New → buscar "prompt" → Template-Triggered Prompt Flow.** Input type: **Manual Inputs** (la otra opción es automática, ligada a la plantilla).

![[ttpf-tipo-de-input.jpg|400]]

| # | Elemento | Configuración |
|---|---|---|
| 1 | 📥 **Get Records** | Objeto Experience · **All records** → guarda una **colección** |
| 2 | 🔁 **Loop** | Recorre *Experiences from Guest Experience* |
| 3 | ✍️ **Add Prompt Instructions** | Dentro del *For Each*: el texto por cada registro |

```text
(Experience Name: {!Loop_Experiences.Name},
 Experience Location:{!Loop_Experiences.Location__c} ,
 Experience Details: {!Loop_Experiences.Description__c})
```

![[ttpf-flow-final.jpg|500]]

**Save → Activate.** El flow tiene que estar **activo** para que aparezca en Prompt Builder.

## 🔌 Usarlo en la plantilla
En Prompt Builder: **Insert Resource → Flows →** el flow, que queda como `Flow:Get_Experience_Newsletter_Data`. Refresca Prompt Builder si ya estaba abierto. El paso a paso completo está en [[🛠️ Crear una plantilla Flex paso a paso]].

> ⚠️ Ojo de examen:
> - El elemento exclusivo de este flow es **Add Prompt Instructions**.
> - Patrón típico: **Get Records → Loop → Add Prompt Instructions**.
> - Debe estar **activo** para elegirlo en *Resources → Flows*.
> - Solo corre **disparado por una plantilla**.

## 🔁 Repaso #flashcards
¿Qué es un Template-Triggered Prompt Flow?::Un flow que solo se ejecuta desde una plantilla de Prompt Builder y le pasa datos y texto.
¿Qué elemento exclusivo tiene un Template-Triggered Prompt Flow?::Add Prompt Instructions, que manda texto del flow a Prompt Builder.
¿Qué secuencia de elementos se usa para pasar varios registros a un prompt?::Get Records (colección) → Loop → Add Prompt Instructions dentro del For Each.
¿Qué hay que hacer con el flow para usarlo en Prompt Builder?::Activarlo, y luego insertarlo con Insert Resource → Flows.
¿Cuándo usar un Template-Triggered Prompt Flow en vez de un merge field?::Cuando el prompt necesita lógica o varios registros, no solo los campos de un registro.
