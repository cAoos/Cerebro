---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-08
---
# 🛠️ Configurar Service Assistant paso a paso

Ejercicio de **Coral Cloud Resorts**: casos de **documentación de viaje** (1–4 días) y **seguros de viaje** (1–3 semanas) en temporada alta. Todo parte de **Setup > Service Assistant**. Usa el **legacy Agentforce Builder** y requiere **Data 360**. Concepto en [[🪄 Agentforce Service Assistant]].

## 1️⃣ Encender funcionalidades
- **Go to Einstein Setup** → Einstein **On**.
- [[🏁 Salesforce Go]] → **Agentforce (Default)** → Get Started → **Turn On**.

## 2️⃣ Crear el agente
**Agentforce Agents** → **+ New Agent** → Create Agent → plantilla **Agentforce Service Assistant** → campo **Company** → ✅ **Enhanced Event Logs** → Agent User **New Agent User** → Create.

![[service-assistant-plantilla.png]]
![[service-assistant-agente-setup.jpg]]

## 3️⃣ Subagente e instrucciones
**New → New Subagent** → describir qué hace → **Travel Documentation**: Classification Description, Scope y 8 instrucciones (verificar documentos, visa y vacunas, links al portal y embajada, checklist, seguimiento, agradecer + encuesta). **Sin acciones** → Finish → **Activate** (*Ignore & Activate* si avisa). Detalle en [[🧷 Instrucciones para Service Assistant]].

![[service-assistant-nuevo-subagente.jpg]]

## 4️⃣ Service AI Grounding
**Customize Experience by Object** → pestaña Case → **Go to Service AI Grounding** → encender → Case Fields: **Subject** y **Description** → ✅ **Include Case Emails** y **Include Case Comments** → Save → **Activate**.

## 5️⃣ Eligibility criteria
**Go to Flows** → **Check Service Plan Eligibility** → decisión: Case no nulo **AND** Priority = **High** **AND** Case Origin = **Email** → **Save as New Flow** (*Travel Documentation*) → Activate → mapear variables en Setup. Ver [[🎟️ Eligibility criteria de Service Assistant]].

![[service-assistant-flow-criterios.png]]

## 6️⃣ Activar y poner el componente
- Toggle **Turn on Service Assistant for Cases**.
- Caso → **Edit Page** → componente **Service Assistant** → Save → Activate → **Org Default** (Desktop) y **App Default** en **Service Console**.

![[service-assistant-activar.jpg]]
![[service-assistant-componente-pagina.jpg]]

## 7️⃣ Probar
Service Console → caso *Help with Travel Documentation* → editar Subject o Description → **Save** → aparece el resumen → **Draft Plan** → marcar pasos. Para rehacer: desmarcar todo → **Redraft Plan**.

![[service-assistant-redraft.png]]

> ⚠️ Ojo de examen: orden **Einstein → Agentforce → agente → subagente → Service AI Grounding → eligibility → toggle → componente**. El plan se **dispara** al guardar cambios del caso, no desde el Builder.

## 🔁 Repaso #flashcards
¿Dónde se configura Service Assistant?::En Setup > Service Assistant.
¿Qué plantilla de agente se usa para Service Assistant?::Agentforce Service Assistant.
¿En qué builder se configura hoy Service Assistant (según el módulo)?::En el legacy Agentforce Builder.
¿Qué campos del Case son requeridos en Service AI Grounding?::Subject y Description.
¿Qué criterios de elegibilidad usa el ejercicio?::Case no nulo, Priority = High y Case Origin = Email.
¿Dónde se pone el componente de Service Assistant?::En la Case Record Page, como Org Default y App Default de Service Console.
¿Cómo se dispara el resumen del caso en la prueba?::Editando y guardando Subject o Description del caso.
¿Qué toggle final enciende Service Assistant?::Turn on Service Assistant for Cases.
