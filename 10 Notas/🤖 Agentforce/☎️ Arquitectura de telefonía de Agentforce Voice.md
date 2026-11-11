---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-07
---
# ☎️ Arquitectura de telefonía de Agentforce Voice

Antes de configurar [[🎙️ Agentforce Voice]] hay que decidir **qué telefonía** lleva las llamadas y **en qué punto** de la llamada entra el agente.

## 📞 Dos arquitecturas de telefonía
| | 🏠 **Salesforce Voice** (nativa) | 🔗 **Partner telephony** |
|---|---|---|
| Qué es | Salesforce maneja **todo el ciclo** de la llamada: desde **procurar el número** hasta el **análisis post-llamada** | Se conecta el CRM, la IA y Agentforce Voice a un **proveedor de telefonía que ya existe** |
| Setup | **Más simple**: sin depender de **SIP trunking** ni de transferencias **PSTN** externas | Requiere **compatibilidad** con **PSTN** (llamadas tradicionales) o **SIP** (llamadas por internet) |
| Handoff | **Sin fricción** entre agente de IA y rep | Depende de la integración |
| Contexto | **Conserva la transcripción completa** y el contexto de sesión en toda la interacción, **incluidas las transferencias** | — |
| Cuándo | Máxima personalización e integración, aprovechar **todo** Agentforce | Conservar la telefonía actual con flexibilidad |

## 🚪 Dónde entra el agente en la llamada
Ambas arquitecturas soportan los dos patrones:
- 🥇 **AI-first frontline**: el agente es el **primer punto de contacto**. Entiende la intención e intenta resolver **desde que empieza la llamada**.
- 🔢 **IVR transition**: se **mantiene el IVR** clásico ("marque 1 para el estado de su pedido") y el agente entra en **puntos específicos** del flujo de la llamada.

## 💬 Voz fuera del teléfono
**Enhanced Chat v2**, el canal de mensajería moderno para sitios web y apps móviles, **también soporta voz**. El cliente puede **cambiar entre texto y voz en la misma conversación**. Ver [[💬 Desplegar un agente en Enhanced Web Chat]].

> ⚠️ Ojo de examen: si piden **conservar la transcripción y el contexto en las transferencias** o **evitar SIP/PSTN externos**, es **Salesforce Voice nativa**. Si piden **mantener el proveedor de telefonía actual**, es **partner telephony** (PSTN o SIP). Si el cliente **no quiere quitar su IVR**, es **IVR transition**. Texto y voz **en la misma conversación** = **Enhanced Chat v2**.

## 🔁 Repaso #flashcards
¿Qué dos arquitecturas de telefonía soporta Agentforce Voice?::Salesforce Voice (telefonía nativa) e integración con proveedores de telefonía de partners.
¿Qué beneficios da Salesforce Voice nativa?::Setup más simple sin SIP trunking ni transferencias PSTN externas, handoffs sin fricción entre agente y rep, y conserva la transcripción y el contexto incluso en transferencias.
¿Qué requiere la integración con un proveedor de telefonía partner?::Compatibilidad con PSTN o SIP para conectar las llamadas entre Salesforce y el proveedor.
¿Qué es el patrón AI-first frontline?::El agente de voz es el primer punto de contacto e intenta resolver desde que empieza la llamada.
¿Qué es el patrón IVR transition?::Se mantiene el IVR clásico y el agente de voz entra en puntos específicos del flujo de la llamada.
¿Qué canal permite cambiar entre texto y voz en la misma conversación?::Enhanced Chat v2.
