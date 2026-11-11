---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# 🌟 IA agéntica confiable

La **confianza es el valor #1** de Salesforce, y su IA agéntica se construye sobre las **Salesforce guidelines for responsible AI**. Los valores se respaldan con acciones concretas: [[🛡️ Einstein Trust Layer]], [[🏛️ Guardrails de plataforma y de Agentforce|guardrails de Agentforce]], [[🧩 Trust patterns de agentes|trust patterns]], [[🎯 Red-teaming de IA|red-teaming ético]] y la **AI Acceptable Use Policy (AI AUP)**.

## 📖 Términos
- **Agentforce**: la marca de la **capa agéntica** de la Salesforce Platform; incluye agentes para clientes y para empleados.
- **Agentes**: autónomos, orientados a objetivos, hacen tareas con **mínima intervención humana**. Conversan en lenguaje natural, responden con datos del negocio, colaboran con el usuario o **actúan en su nombre**, en la interfaz de Salesforce o en canales de clientes.
- **IA agéntica**: el sistema que permite a los agentes **operar autónomamente, decidir y adaptarse**, y colaborar con humanos.

## 🧭 Los 5 principios de la IA agéntica responsable

![[ia-agentica-confiable-principios.png|500]]

| Principio | Cómo se cumple en Agentforce |
|---|---|
| 🎯 **Accuracy** | El reasoning engine usa **clasificación por topic** (hoy [[🗂️ Subagentes\|subagentes]]) para mantener al agente en su tarea; el **grounding** trae contexto de la org al prompt |
| 🛡️ **Safety** | **Políticas de sistema** que limitan el alcance (ver [[🧱 Defensa del prompt]]); la Trust Layer **detecta contenido dañino** y lo registra en el **audit trail**; **zero data retention** con los proveedores de LLM (tus datos no salen ni entrenan modelos ajenos) |
| 🪟 **Honesty** | Respeta el origen de los datos y pide **consentimiento**; **declara cuando la IA generó el contenido** (disclosures estándar) |
| 💪 **Empowerment** | Alianza humano-IA: se **automatiza lo rutinario** y **las decisiones de alto riesgo las toma la persona** (ver [[🤝 Modelo de colaboración humano-IA]]) |
| 🌱 **Sustainability** | Modelos **más pequeños y eficientes** (a veces superan a los grandes), hardware eficiente y data centers bajos en carbono; modelos optimizados como **xLAM** y **xGen-Sales** |

Los riesgos que estos principios atacan están en [[☢️ Riesgos de la IA agéntica]]. No confundir con los 5 principios de *Trusted AI* de [[⚖️ Gobernanza de IA]].

> ⚠️ Ojo de examen: los 5 principios de IA agéntica responsable son **Accuracy, Safety, Honesty, Empowerment, Sustainability**. **xLAM / xGen-Sales → Sustainability**. **Zero data retention → Safety**. **Avisar que algo lo generó la IA → Honesty**. **Humano decide lo de alto riesgo → Empowerment**.

## 🔁 Repaso #flashcards
¿Cuáles son los 5 principios de Salesforce para IA agéntica responsable?::Accuracy, Safety, Honesty, Empowerment y Sustainability.
¿Qué mecanismos mantienen la exactitud (Accuracy) de un agente?::La clasificación por topic/subagente del reasoning engine y el grounding con datos de la org.
¿A qué principio corresponde la política de zero data retention con los proveedores de LLM?::Safety.
¿A qué principio corresponde declarar que un contenido fue generado por IA?::Honesty.
¿A qué principio corresponde usar modelos como xLAM y xGen-Sales?::Sustainability (modelos pequeños, optimizados y eficientes).
¿Qué dice el principio de Empowerment?::Automatizar lo rutinario y dejar las decisiones de alto riesgo a las personas.
¿Qué es Agentforce según Salesforce?::La marca de la capa agéntica de la Salesforce Platform, con agentes para clientes y empleados.
