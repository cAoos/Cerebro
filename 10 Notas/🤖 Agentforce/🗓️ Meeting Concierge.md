---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-09
---
# 🗓️ Meeting Concierge

Herramienta de [[🧑‍💼 Agentic Advisor]] que lleva **todo el ciclo de una reunión**: preparación, sesión y seguimiento. Convierte horas de trabajo manual en minutos. Se abre desde su propia homepage o desde una reunión en [[☀️ Run My Day]].

## 📒 Meeting playbooks
- Cada reunión tiene un registro de **meeting playbook**. Se **crea solo** (con un **flow**) cuando aparece una reunión con cliente en el calendario del asesor.
- Se genera a partir de **meeting playbook definitions** por rol y tipo de tarea, que el admin configura con **prompts, Action Plans y acciones de Agentforce**.
- Hay plantillas incluidas y un **playbook builder low-code**. Las definiciones se asignan a **permission sets**.

## 🔄 Tres etapas (pestañas)
| Etapa | Qué genera o hace |
|---|---|
| 📋 **Pre Meeting** | **Client Summary** (salud financiera, metas, portafolio, interacciones, eventos de vida) y **Meeting Preparation Brief** con agenda sugerida. Tareas de preparación vía **Action Plan**. Subir documentos y que Agentforce los resuma. Al final: **Generate Meeting Discussion Guide** |
| 🎙️ **In Session** | Seguir la **Discussion Guide**. Grabar audio **con consentimiento del cliente**, escribir notas, subir documentos y notas a mano. Al final: **Generate Meeting Follow-Up** |
| ✅ **Post Meeting** | **Meeting Follow-Up Summary** (temas, decisiones, próximos pasos) y acciones rankeadas: email de seguimiento, actualizar metas, crear tareas, actualizar miembros del hogar, **crear referidos** |

![[advisor-concierge-pre.jpg]]
![[advisor-concierge-in-session.jpg]]
![[advisor-concierge-post.jpg]]

## 🛡️ Control y cumplimiento
- ✏️ Todo lo generado se puede **editar a mano** o **pedirle a Agentforce que lo revise** describiendo el cambio.
- 🎧 **No guarda el audio completo ni la transcripción**: solo los **resúmenes generados por IA**, para cumplir las reglas de la firma.
- 💾 El Follow-Up Summary **solo entra a Salesforce cuando el asesor lo acepta y lo guarda**. El humano controla la fuente de verdad.

## 🧪 Ejemplo
Antes, Ryan tardaba más de una hora en preparar una reunión entre el portal del custodio, correos viejos y una agenda escrita a mano. Ahora abre el playbook, revisa el Client Summary, pide un brief más corto sobre jubilación y genera la guía. En la sesión graba con permiso. Al cerrar revisa el resumen, lo guarda y crea un referido de hipoteca.

> ⚠️ Ojo de examen: es un buen ejemplo de **human-in-the-loop**: la IA genera y el humano **acepta antes de guardar**. Y de cumplimiento: **no se guarda el audio ni la transcripción**, solo resúmenes.

## 🔁 Repaso #flashcards
¿Cuáles son las tres etapas de Meeting Concierge?::Pre Meeting, In Session y Post Meeting.
¿Cómo se crea el meeting playbook de una reunión?::Automáticamente con un flow cuando aparece una reunión con cliente en el calendario del asesor.
¿Con qué configura el admin una meeting playbook definition?::Prompts, Action Plans y acciones de Agentforce; se asigna a permission sets.
¿Guarda Meeting Concierge el audio o la transcripción de la reunión?::No; solo guarda los resúmenes generados por IA, por cumplimiento.
¿Cuándo entra el Meeting Follow-Up Summary a los registros de Salesforce?::Solo cuando el asesor lo acepta y lo guarda.
¿Qué genera la etapa Pre Meeting?::Client Summary, Meeting Preparation Brief con agenda y, al final, la Meeting Discussion Guide.
