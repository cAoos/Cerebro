---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-09
---
# 🤝 Intelligent Referral Management

Sistema de [[🧑‍💼 Agentic Advisor]] para **capturar, enrutar y seguir referidos**, que suelen perderse en el día a día. Por ejemplo, un cliente menciona que su empresa necesita un crédito y eso es negocio para otra vertical del banco.

## 🆚 Referral no es Lead
| | **Lead** | **Referral** (objeto estándar) |
|---|---|---|
| Para | Clientes **nuevos** | Clientes **existentes** (o de socios) |
| Proceso | Lineal: 1 lead → 1 oportunidad | Se relaciona con el cliente y con **varias oportunidades** |

## 👥 Dos partes
- ✍️ **Quien refiere:** usa un **intake form dinámico**; al elegir el producto (por ejemplo, hipoteca) solo aparecen los campos relevantes, con barra de progreso.
- 🎯 **El especialista:** recibe la lista de referidos con **contexto** de Salesforce y otras fuentes.

Quiénes refieren: empleados de sucursal (con **incentivos**), directivos (referidos VIP prioritarios) y externos (socios, abogados, contadores, agentes inmobiliarios del cliente).

## ⚙️ Cómo funciona
- 🔀 Un **routing engine** que el admin configura **sin código** asigna el referido al mejor usuario o cola.
- 🏅 Se mantiene la **atribución del incentivo** a quien refirió durante todo el proceso.
- 👀 Quien refiere sigue el **estado** en el registro (contactado, reunión agendada…).
- 🔄 El especialista **convierte el referido en una o varias oportunidades**, y los datos, actividades y atribución pasan a ellas.

![[advisor-referral-intake.jpg]]

## 📍 Dónde aparece
- En [[🗓️ Meeting Concierge]], etapa **Post Meeting**: Agentforce analiza las notas y **sugiere crear el referido**.
- En [[☀️ Run My Day]], grupo **Grow**: los referidos entrantes priorizados.
- Al abrir un referido entrante: notas de quien refiere, **datos enriquecidos de Data 360**, **talking points generados por Agentforce** y un **borrador de email** que se envía con un clic.

## 🧪 Ejemplo
Tras la reunión, el cliente de Ryan dice que va a comprar una casa de vacaciones. Meeting Concierge prioriza la acción "crear referido". Ryan llena el formulario de hipoteca, recibe un número de referido y este va al especialista de crédito hipotecario. El especialista lo convierte en una oportunidad y Ryan conserva su incentivo.

> ⚠️ Ojo de examen: **Referral ≠ Lead**. Referral es para clientes existentes y puede generar **varias oportunidades**. El enrutamiento es **declarativo** (routing engine), sin código.

## 🔁 Repaso #flashcards
¿En qué se diferencia el objeto Referral de un Lead?::Lead es para clientes nuevos con proceso lineal (1 lead → 1 oportunidad); Referral se relaciona con clientes existentes y con varias oportunidades.
¿Cómo se asignan los referidos al especialista correcto?::Con un routing engine que el admin configura sin código.
¿Qué se conserva al convertir un referido en oportunidades?::Los datos, las actividades y la atribución del incentivo a quien refirió.
¿Dónde aparecen los referidos en Agentic Advisor?::En Meeting Concierge (Post Meeting, sugerencia de crear) y en Run My Day (grupo Grow, entrantes).
¿Qué tiene de especial el intake form de referidos?::Es dinámico: al elegir el producto solo muestra los campos y pasos relevantes.
