---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-08
---
# 💲 Agentforce Quoting

Agentforce Sales **genera cotizaciones con productos y precios correctos** a partir de una conversación, usando **datos transaccionales unificados y el CRM**. Es la tercera capacidad de [[💸 Agentforce for Sales]] (*agilizar las cotizaciones*).

## 🎯 Qué hace
- ✍️ **Crea, modifica y resume** cotizaciones.
- 🆕 Cotiza **negocio nuevo** y **enmiendas (amendments) sobre assets** existentes.
- 📦 Sigue las **reglas de catálogo y fulfillment** para cotizar solo productos válidos.
- 💰 Pone precios y descuentos **dentro de los guardrails del sistema**.
- 🔐 Respeta los **permisos por rol** del usuario.
- 👤 El vendedor solo **revisa la cotización final** y la envía.

## 🧩 Cómo está armado
| Pieza | Detalle |
|---|---|
| **Tipo de agente** | **Agentforce Employee Agent** (lo usa el vendedor desde el panel de Agentforce) |
| **Subagente** | **Quote Management**, agregado desde la **Asset Library**: trae las instrucciones y **acciones basadas en flows** |
| **Se quita** | El subagente **General FAQ**, que no hace falta |
| **Precios** | **Salesforce Pricing Setup > Sync Pricing Data** (Agentforce Revenue): deja los precios al día en todas las **decision tables** |
| **Correo** | **Einstein for Sales > Sales Emails** + **Draft with AI** con la plantilla *Create Quote Email* |
| **Acceso** | Permission set con el agente en **Agent Access** |

> ⚠️ Ojo de examen: los vendedores ven un Employee Agent solo si su permission set lo incluye en **Agent Access**. Antes de cotizar hay que **sincronizar los datos de precios** para que las decision tables tengan el precio actual.

Práctica: [[🛠️ Crear un Quoting Agent paso a paso]].

## 🔁 Repaso #flashcards
¿Qué hace Agentforce Quoting?::Crea, modifica y resume cotizaciones con productos y precios correctos, dentro de los guardrails de precio y descuento.
¿Qué tipos de cotización puede crear el agente?::De negocio nuevo y de enmiendas sobre assets existentes.
¿Qué subagente usa el agente de cotizaciones?::Quote Management, con acciones basadas en flows.
¿Sobre qué tipo de agente se arma el Quoting Agent?::Agentforce Employee Agent.
¿Qué subagente se elimina al crear el Quoting Agent?::General FAQ.
¿Para qué se hace Sync Pricing Data antes de cotizar?::Para que los precios actuales estén en todas las decision tables y para todos los usuarios.
¿Cómo se da acceso a un Employee Agent a los vendedores?::Con un permission set que incluya el agente en Agent Access.
¿Cómo respeta la seguridad el agente de cotizaciones?::Mantiene los permisos por rol del usuario.
