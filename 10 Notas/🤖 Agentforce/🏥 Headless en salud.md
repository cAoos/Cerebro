---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 🏥 Headless en salud

**Problema: el "toggle tax"** 🔀. Los coordinadores de cuidado saltan entre tablets clínicas, portales de EHR y herramientas de agenda que no se hablan. Pierden contexto, foco y tiempo, e IT vive rehaciendo integraciones punto a punto frágiles.

## 🏗️ Backend unificado
| Rol | Producto |
|-----|----------|
| 🧠 **System of Context** | ☁️ **Data 360**: une datos del EHR externo con el CRM **sin moverlos ni duplicarlos** |
| 📁 **System of Record** | 🏥 **Agentforce Health**: pacientes, planes de cuidado, cobertura y proveedores en un perfil unificado |

Las superficies se conectan por APIs y **Salesforce-Hosted MCP Servers**, que heredan **permisos por rol, sharing y audit trails a nivel de protocolo** → cumplimiento **HIPAA**.

## 🧰 Herramientas MCP de Agentforce Health
- ⚙️ **Agentforce Health Setup**: configurar la org y el modelo de datos clínico con coding agents, sin clics.
- 🩺 **Integrated Care Management**: foto clínica (plan, visitas, tareas) en la tablet del coordinador.
- 🏠 **Home Health**: los auxiliares registran visitas desde apps móviles propias, escribiendo en Salesforce.
- 🔎 **Provider Search**: especialistas en red para portales de pacientes.
- 📅 **Intelligent Appointment Management**: verificar cobertura y agendar citas (un recurso, varios, recurrentes).

## 📱 Cuidado en cualquier lugar
Con **HXL** se define un widget **una vez** (reserva de cita, tarjeta de resumen del paciente) y se muestra en la app del paciente, la tablet del clínico o el portal web.

> 💡 *"Mientras menos visible es Salesforce, a más lugares llega su inteligencia."*

> ⚠️ Ojo de examen: Data 360 = **System of Context**; Agentforce Health = **System of Record**. El cumplimiento viene **heredado** por pasar por MCP + Trust Layer.

Parte de [[🔓 Headless en Salesforce (AIforce)]] · ver [[🏛️ Capas de la plataforma agéntica]].

## 🔁 Repaso #flashcards
¿Qué es el "toggle tax" en salud?::La pérdida de contexto, foco y tiempo por saltar entre sistemas clínicos desconectados.
¿Qué rol cumplen Data 360 y Agentforce Health en el caso headless de salud?::Data 360 es el System of Context; Agentforce Health es el System of Record.
¿Cómo se mantiene el cumplimiento HIPAA en apps externas?::Al conectarse por Salesforce-Hosted MCP y la Trust Layer, heredan permisos, sharing y audit trails a nivel de protocolo.
