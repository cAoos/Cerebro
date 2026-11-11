---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-06
---
# 🔌 Conexiones y canales de un agente

- 📺 **Canal**: la plataforma, app o interfaz donde el agente **se encuentra con los usuarios** (chat web, teléfono…).
- 🔌 **Conexión**: se crea al **desplegar el agente a un canal**. **Empaqueta** todo lo que lo ata a ese canal:
  - **Adaptive response formats** (imágenes, botones, links) adecuados al canal
  - **Flows de Omni-Channel** que enrutan conversaciones **hacia y desde** el agente
  - **Contexto** para razonar y responder bien en ese canal (**connection instructions**)

**Un agente, muchas conexiones:** el agente es **el mismo** y cada canal tiene su conexión. Se configura la experiencia **por canal sin reconstruir el agente**, lo que permite escalar y evita repetir configuración.

## 📋 Conexiones disponibles
| Tipo de agente | Conexiones |
|---|---|
| 🎧 **Service Agent** | **Telephony**, **Enhanced Chat v2**, **Messaging**, **Service Email**, **Marketing Email** |
| 🧑‍💼 **Employee Agent** | **Lightning Experience**, **Salesforce Mobile**, **Slack**, **Enhanced Web Chat** |

## ➕ Agregar una conexión
**Agentforce Studio →** el agente **→ Explorer → + junto a Connections → Add Connection →** elegir (Messaging, Telephony…) **→ Add to Agent.**

Después se afinan las **connection instructions** (cómo razonar y responder en **ese** canal) y los **adaptive response formats** (cómo estructurar la respuesta).

Detalle por canal: [[🔀 Enrutamiento Omni-Channel de un agente]], [[💬 Desplegar un agente en Enhanced Web Chat]] y [[🎙️ Agentforce Voice]]. Ver también [[📞 Canales y escalamiento de un agente]].

> ⚠️ Ojo de examen:
> - **Conexión ≠ canal**: la conexión es el paquete (formatos, flows, instrucciones) que ata el agente al canal.
> - Un agente puede tener **varias conexiones** sin duplicarlo.
> - **Slack y Lightning/Mobile → Employee Agent**.
> - **Telephony, Service Email y Marketing Email → Service Agent**.

> 💲 Ejemplo de Employee Agent: el [[💲 Agentforce Quoting|Quoting Agent]], que los vendedores ven si su permission set lo incluye en **Agent Access**.

## 🔁 Repaso #flashcards
¿Qué es una conexión en Agentforce?::El paquete que ata un agente a un canal: adaptive response formats, flows de Omni-Channel y contexto para responder en ese canal.
¿Hay que duplicar el agente para ponerlo en varios canales?::No, un mismo agente puede tener varias conexiones, una por canal.
¿Qué conexiones tiene un Service Agent?::Telephony, Enhanced Chat v2, Messaging, Service Email y Marketing Email.
¿Qué conexiones tiene un Employee Agent?::Lightning Experience, Salesforce Mobile, Slack y Enhanced Web Chat.
¿Qué son las connection instructions?::Instrucciones que guían cómo el agente razona y responde en un canal específico.
¿Qué son los adaptive response formats?::Formatos de respuesta (imágenes, botones, links) adaptados a cada canal.
