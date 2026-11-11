---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 💰 Headless en servicios financieros

**Problema:** el asesor de patrimonio tiene la info repartida (saldos, eventos de vida, notas, documentos de planeación). Pasa más tiempo buscando que preparando la conversación, y el CRM queda incompleto.

**Headless:** los **Salesforce-Hosted MCP Servers** llevan la inteligencia de **Agentforce Financial Services** a las herramientas del asesor (Slack, panel de Teams, portal propio). Respeta permisos, FLS y guardrails de cumplimiento financiero **a nivel de protocolo**.

## 🧾 Journey-level recipes
![[fsc-journeys-asesor.jpg]]

En vez de que la herramienta junte llamadas sueltas, las herramientas MCP se agrupan en **recetas por journey**: **una petición** dispara una **secuencia prediseñada** de acciones.

| | Journey | Qué entrega |
|---|---------|-------------|
| 🌅 | **Run My Day** | Lista priorizada de reuniones, compromisos vencidos y alertas de clientes |
| 📋 | **Meeting Prep** | Paquete de preparación: agenda, puntos clave, pendientes, cambios recientes del cliente |
| 🎙️ | **Live Meeting** | Transcripción y notas en segundo plano, resumen en tiempo real |
| ✅ | **Post-Meeting Follow-Up** | Resumen y tareas que el asesor **revisa antes de guardar**: nada se escribe sin su confirmación |
| 👤 | **Client 360** | Foto completa: cuentas, eventos de vida, desempeño del portafolio, pendientes |

## 🔗 Más allá de Salesforce
- 🔗 **MuleSoft MCP Bridge**: convierte APIs existentes (por ejemplo un sistema de trading heredado) en **herramientas para agentes**, **sin cambiar código**.
- 📊 **Tableau MCP**: expone la **capa semántica gobernada** de Tableau para traer analítica de portafolio.

> ⚠️ Ojo de examen: conectar un **sistema legado** como herramienta de agente → **MuleSoft MCP Bridge**. "Nada se guarda hasta que el asesor confirma" = [[🎚️ Autoridad progresiva|impacto moderado]].

Parte de [[🔓 Headless en Salesforce (AIforce)]] · ver [[🔌 MCP en Salesforce]].

## 🔁 Repaso #flashcards
¿Qué son las journey-level recipes de Agentforce Financial Services?::Agrupaciones de herramientas MCP donde una sola petición dispara una secuencia prediseñada de acciones.
¿Cuáles son los 5 journeys del asesor?::Run My Day, Meeting Prep, Live Meeting, Post-Meeting Follow-Up, Client 360.
¿Qué hace el MuleSoft MCP Bridge?::Convierte APIs existentes, incluso de sistemas legados, en herramientas para agentes sin cambiar código.
