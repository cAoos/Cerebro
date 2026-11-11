---
tipo: nota
tema: prompts
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-27
---
# 🏷️ Plantilla Field Generation

Plantilla que **devuelve la respuesta del LLM a un campo específico** de un registro. Está **atada a un campo**.

## 🧰 Se necesitan dos cosas
1. 🧾 **La plantilla** en Prompt Builder, tipo **Field Generation**, con su **objeto y campo**
2. ⚡ **El campo en la página**, configurado en **Lightning App Builder**

El usuario la activa con el **botón de Einstein** ![[prompt-builder-boton-einstein.png|30]] que aparece junto al campo.

## 🧪 Ejemplo: resumen de un caso
| Dato | Valor |
|------|-------|
| Type | Field Generation |
| Name / API | `Case Comments Summary` / `Case_Comments_Summary` |
| Object | Case |
| Object Field | `Case_AI_Summary__c` |

```text
You are a support representative who is tasked with creating a short summary of a case that happened between a customer and a company support rep.
```
![[field-generation-case-ai-summary.png]]

## ⚡ Configuración en Lightning App Builder
- Se hace sobre una **Field Section** (Dynamic Forms) o **Record Detail**.
- El campo tiene que ser **editable, nunca de solo lectura**: Text, Text Area, Text Area (Long) o Text Area (Rich).
- En las propiedades del campo, sección **Einstein Generative AI**, se elige la plantilla.

> ⚠️ Ojo de examen: si el botón de Einstein no aparece, revisa que el campo sea **editable** y de **tipo texto**.

Uno de los [[🧾 Tipos de plantillas de Prompt Builder]]. Paso a paso con capturas: [[🛠️ Crear una plantilla Field Generation paso a paso]].

## 🔁 Repaso #flashcards
¿Qué dos cosas necesita una plantilla Field Generation?::La plantilla en Prompt Builder (con objeto y campo) y el campo configurado en Lightning App Builder.
¿Qué tipos de campo admite Field Generation?::Campos de texto editables: Text, Text Area, Text Area (Long), Text Area (Rich).
