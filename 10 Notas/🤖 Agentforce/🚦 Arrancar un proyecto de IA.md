---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-10-31
---
# 🚦 Arrancar un proyecto de IA

Después de elegir el caso de uso en la [[🔭 Estrategia de IA]], el proyecto arranca con tres cosas: **stakeholders, metas y solución técnica**.

## 👥 Stakeholders del proyecto
Personas con **interés, influencia o impacto** en el proyecto. Son **distintos de los stakeholders estratégicos** ([[👥 Centro de excelencia de IA]]): estos supervisan la estrategia de toda la empresa, pero **el líder del proyecto es quien rinde cuentas**.

| Rol | Qué aporta | Coral Cloud |
|---|---|---|
| 🧑‍💼 **Manager de los usuarios finales** | Representa a quienes usarán la solución | Customer success manager |
| 👔 **Sponsor ejecutivo** | **Asigna recursos y prioriza** | VP de Customer Experience |
| ⚖️ **Seguridad y Legal** | Que sea ético, seguro y use los datos legalmente | |
| 🛠️ **Equipo técnico** | Construye la solución | Becca, la admin |

Comunicarse **seguido**: entender necesidades, recoger feedback y ajustar.

## 🎯 Metas SMART
**S**pecific · **M**easurable · **A**chievable · **R**elevant · **T**ime-bound. Ej: **reducir 50% el tiempo de check-in** y **mantener o subir la satisfacción**. Sin **métricas y KPIs** no puedes medir el éxito; atar la IA a **ingresos** muestra ROI y abre la puerta al siguiente proyecto.

## 🛠️ Requisitos técnicos
- 🤖 ¿IA **predictiva, generativa o ambas**?
- 🔗 ¿Debe **integrarse** con otros sistemas?
- 📦 ¿Hay solución **out-of-the-box** que personalizar, o hay que construir? ¿Hay habilidades internas?
- ⚖️ Trade-offs: precisión vs velocidad, complejidad vs simplicidad, innovación vs costo.
- ☁️ En Salesforce: **Data 360 y Einstein Generative AI habilitados**.

## 🏝️ La solución de Coral Cloud: check-in con IA
1. 🌊 Un **flow** crea el registro **Guest Event** con los datos de reserva en **Data 360**.
2. 🤖 **Agentforce** lanza ese flow en lenguaje natural: "Check in Sofia Rodriguez". Ver [[⚡ Acciones de agente]].
3. ✉️ **Prompt Builder** genera un **email de bienvenida personalizado** con excursiones según compras previas. Ver [[🧾 Tipos de plantillas de Prompt Builder]].

Siguiente: [[🔄 Etapas de un proyecto de IA]].

> ⚠️ Ojo de examen: el **sponsor ejecutivo asigna recursos y prioriza**. Las metas deben ser **SMART** con **KPIs**. Prerrequisitos en Salesforce: **Data 360 + Einstein Generative AI**.

## 🔁 Repaso #flashcards
¿Qué diferencia a los stakeholders del proyecto de los estratégicos?::Los del proyecto se dedican a implementar ese proyecto específico; los estratégicos supervisan la estrategia de IA de toda la empresa.
¿Qué hace el sponsor ejecutivo de un proyecto de IA?::Asigna recursos y prioriza el proyecto.
¿Qué significa SMART?::Specific, measurable, achievable, relevant y time-bound.
¿Qué debe estar habilitado para construir un proyecto de IA en Salesforce?::Data 360 y Einstein Generative AI.
¿Qué tres piezas usó Coral Cloud para el check-in con IA?::Un flow que crea el Guest Event con datos de Data 360, Agentforce que lanza el flow en lenguaje natural y Prompt Builder para el email de bienvenida.
