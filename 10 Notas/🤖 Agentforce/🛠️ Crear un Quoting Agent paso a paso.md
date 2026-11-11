---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-08
---
# 🛠️ Crear un Quoting Agent paso a paso

Proyecto *Quick Start: Build an Agent to Create Quotes Fast* (playground con Revenue Cloud). Concepto en [[💲 Agentforce Quoting]].

## 1️⃣ Funcionalidades de soporte
1. Setup → **Salesforce Pricing Setup** → *Sync Pricing Data* → **Sync** → Confirm.
2. Setup → **Salesforce Go** → *Agentforce Studio* → Get Started → **Turn On** (ver [[🏁 Salesforce Go]]).
3. Setup → **Einstein for Sales** → **Turn on Sales Emails**.

![[cotizacion-sync-precios.jpg]]
![[cotizacion-sales-emails.jpg]]

## 2️⃣ Crear el agente
App Launcher → **Agentforce Studio** → **New Agent** → **Agentforce Employee Agent** → Name *Quoting Agent*, API `Quoting_Agent` → Let's Go.

![[cotizacion-employee-agent.png]]

## 3️⃣ Ajustar subagentes
1. Explorer → **+** junto a Subagents → **Add from Asset Library** → buscar *quote* → **Quote Management** → Add to Agent.
2. **⋯** en **General FAQ** → Delete.
3. **Save** → **Commit Version** → **Activate** (ver [[🏷️ Versiones de un agente]]).

![[cotizacion-agregar-subagente.jpg]]
![[cotizacion-borrar-general-faq.jpg]]

## 4️⃣ Dar acceso
Setup → Permission Sets → **New** (*Agentforce User*, licencia None) → **Agent Access** → Edit → agregar **Quoting Agent** → Save → Manage Assignments → asignar al usuario.

![[cotizacion-agent-access.jpg]]

## 5️⃣ Cotizar conversando
App **Revenue Cloud** → cuenta *EdgeMX* → **ícono de Agentforce** (arriba a la derecha):
- *"Create a quote for this account with 15 units of the Headset product. Please apply a 15% discount."* → elegir la oportunidad *Office Upgrade*.
- *"Please show me the quote"* → link al nombre de la cotización.
- *"Please change the discount to 10% for the first product."* → el agente actualiza la misma cotización.

## 6️⃣ Enviar la cotización
Oportunidad → Related → la cotización → **▼ → Email Quote** → enviar por Salesforce → destinatario y asunto → **Draft with AI** → *Create Quote Email* → elegir la cotización → Continue (ver [[🛠️ Crear una plantilla Sales Email paso a paso]]).

![[cotizacion-email-quote.jpg]]

> ⚠️ Ojo de examen: el agente de cotizaciones es un **Employee Agent** con el subagente **Quote Management** de la Asset Library; los vendedores lo usan desde el **panel de Agentforce** del registro, y lo ven gracias a **Agent Access** en su permission set.

## 🔁 Repaso #flashcards
¿Cuáles son las 3 funcionalidades de soporte del Quoting Agent?::Sync Pricing Data, Agentforce Studio encendido en Salesforce Go y Sales Emails en Einstein for Sales.
¿Dónde se sincronizan los datos de precios?::En Setup > Salesforce Pricing Setup > Sync Pricing Data.
¿Desde qué plantilla se crea el Quoting Agent?::Agentforce Employee Agent.
¿Cómo se agrega el subagente Quote Management?::Explorer → + junto a Subagents → Add from Asset Library → Quote Management.
¿Dónde se habilita un agente en un permission set?::En la sección Agent Access del permission set.
¿Desde dónde usa el vendedor el Quoting Agent?::Desde el ícono de Agentforce (panel de conversación) en el registro.
¿Cómo se envía la cotización con un correo generado por IA?::Email Quote → Draft with AI → plantilla Create Quote Email.
