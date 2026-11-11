---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 🤖 Agentforce

Es una **solución de IA conversacional proactiva**, formada por [[🦾 Agentes autónomos|agentes autónomos]] construidos sobre **Salesforce Platform**. Los agentes conocen tu negocio y trabajan dentro de los flujos diarios de empleados y clientes, **con o sin intervención humana**: piensa en ellos como **compañeros digitales de confianza**.

Usan **ML y [[🗣️ Procesamiento de lenguaje natural (NLP)|NLP]]** para entender la petición, siguen instrucciones y responden con **datos seguros**.

## 🧬 Los 5 componentes
| | Componente | Qué es |
|---|-----------|--------|
| 📊 | **Datos** | Lo que el agente sabe de la empresa y los clientes: **estructurados y no estructurados** (artículos de Knowledge, CRM, fuentes externas). Tú eliges a qué accede |
| 🧠 | **Razonamiento** | **La base de todo agente**: entiende la intención y activa subagentes y acciones durante la conversación. Lo hace el [[🌍 Atlas Reasoning Engine]] |
| ⚡ | [[⚡ Acciones de agente\|Acciones]] | **Tareas individuales** que hace el agente (pedir el número de cuenta, iniciar una devolución) |
| 🗂️ | [[🗂️ Subagentes\|Subagentes]] | **Categorías de acciones** que definen los trabajos del agente, con **instrucciones** que sirven de protección |
| 📡 | **Canales** | Dónde vive: org de Salesforce, app móvil, Slack, SMS, correo, sitio web, Experience Cloud |

## 🔄 Cómo trabaja (recapitulación)
```text
🗣️ Pregunta ─► 🗂️ compara con sus subagentes y elige el más relevante ─► ⚡ ejecuta sus acciones ─► 💬 responde
                                                                          │
                                                   ❓ pide más datos o muestra error si no puede
```

> [!example]- 🖼️ Un agente en acción
> ![[agentforce-ejemplo-conversacion.jpg]]

## 📍 Dónde se interactúa
![[agentforce-barra-lateral.jpg]]

- 👩‍💼 **Empleados**: en la org, la **app móvil** o **Slack** (resumir cuentas, aprobar, revisar casos, tickets de TI, onboarding de RR. HH.).
- 🧑‍🤝‍🧑 **Clientes**: en el **sitio web** o **sitios de Experience Cloud** (soporte, documentación, agendar citas).

## 🛡️ Agentes y confianza
- 🛡️ Integrados con la [[🛡️ Einstein Trust Layer]]: respuestas basadas en datos confiables, **zero data retention**, detección de respuestas dañinas y **registro de eventos**.
- 🗂️ Las **instrucciones de los subagentes** son guardrails contra **alucinaciones y ataques**.
- 🔐 El acceso a registros y campos se basa en **permisos**.
- 🧪 Se prueba en el panel **Agent Preview** y en **Agentforce Testing Center**, que genera casos de prueba.

> ⚠️ Ojo de examen: los 5 componentes **Datos · Razonamiento · Acciones · Subagentes (topics) · Canales**. "¿Qué es la base de cualquier agente?" → **el razonamiento** (Atlas).

Tipos de agentes: [[📦 Plantillas de agente preconfiguradas]] · Qué lo hace confiable: [[🌟 Características de Agentforce]] · Dónde se construye: [[🏗️ Agentforce Builder]].

## 🔁 Repaso #flashcards
¿Qué es Agentforce?::Una solución de IA conversacional proactiva formada por agentes autónomos construidos sobre Salesforce Platform.
¿Cuáles son los 5 componentes de un agente de Agentforce?::Datos, razonamiento, acciones, subagentes (topics) y canales.
¿Cómo decide un agente qué hacer con una pregunta?::La compara con sus subagentes, elige el más relevante y ejecuta sus acciones.
¿Dónde se prueba un agente?::En el panel Agent Preview y en Agentforce Testing Center.
