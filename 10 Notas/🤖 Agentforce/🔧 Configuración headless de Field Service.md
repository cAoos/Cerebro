---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 🔧 Configuración headless de Field Service

**Problema:** configurar **Agentforce Field Service and Operations** desde cero es pesado: territorios, work types, políticas de agenda, skills de técnicos… y cada nueva línea de servicio obliga a revisar todo.

**Headless:** pasar de **una conversación a una org configurada**, sin un solo menú de Setup. Funciona con **headless skills** en **Gemini, Claude o Slackbot**: no hay lock-in a una herramienta.

## 🏗️ Arquitectura de skills por capas
| | Capa | Qué hace |
|---|------|----------|
| 🎼 | **Orchestration Skills** | Leen el sitio web de la empresa (grounding) y arman recomendaciones |
| ⚙️ | **Configuration Skills** | Tras aprobar el plan, montan la infraestructura base |
| 🧱 | **Feature Skills** | La construcción fina: **Foundational Setup** (territorios, horarios, work types, skills, políticas de agenda) y **Mobile App Configuration** (marca, pre-work briefs, captura de datos como voice-to-form) |

## 🗣️ La conversación de diseño
```text
🌐 URL del sitio ─► 🎼 lee y entiende el negocio ─► ❓ preguntas de seguimiento ─► 📄 plan ─► ✍️ revisas y ajustas ─► ✅ apruebas ─► ⚙️ se configura
```
El plan incluye work types por línea de servicio, territorios y horarios, políticas de agenda y los skills y recursos de técnicos. **Nada es final hasta que lo apruebas.**

## #️⃣ En Slack
Slack muestra **componentes de UI dinámicos** en la conversación (territorios, work types y políticas como listas en vivo). **Las skills llevan la lógica; Slack pinta**: es headless en la práctica.

## 📱 Resultado
Lista desde el día uno en escritorio y móvil: marca aplicada, citas de ejemplo cargadas, pre-work brief, work plans y formularios de captura.

> ⚠️ Ojo de examen: el único input inicial es la **URL del sitio de la empresa**, y el orden de capas es **Orchestration → Configuration → Feature**.

Parte de [[🔓 Headless en Salesforce (AIforce)]] · ver [[🛠️ ADLC Skills]].

## 🔁 Repaso #flashcards
¿Con qué input arranca la configuración headless de Field Service?::Con la URL del sitio web de la empresa.
¿Cuáles son las 3 capas de skills de la configuración headless de Field Service?::Orchestration Skills, Configuration Skills y Feature Skills.
¿Qué dos áreas cubren las Feature Skills?::Foundational Setup (territorios, horarios, work types, skills, políticas) y Mobile App Configuration.
