---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-08
---
# 🛠️ Configurar Agentforce Sales Coach paso a paso

Todo pasa en **Setup > Agentforce Sales Coach**, un wizard de 4 pasos que muestra qué funcionalidades faltan y cuáles ya están. Concepto en [[🏋️ Agentforce Sales Coach]].

![[coach-enable-all.jpg]]

## 1️⃣ Enable Agentforce Sales Coach
1. **Enable All** enciende Einstein Generative AI y Agent Studio.
2. **Go to Data Cloud**: confirmar que aparece *Your Home Org Details*. Volver y refrescar.
3. Activar el **toggle** → Got It.

![[coach-toggle.png]]

## 2️⃣ Create a User for Agentforce Sales Coach
1. **Go to User Setup** → nuevo usuario *Sales Coach Agent*, licencia **Einstein Agent**, perfil **Einstein Agent User**.
2. **Go to Permission Sets** → asignarle el permission set **Sales Coach Agent**.

![[coach-nuevo-usuario.jpg]]
![[coach-permission-set-agente.jpg]]

## 3️⃣ Grant Access to Agentforce Sales Coach
| Permission set | Para quién |
|---|---|
| **Manage Agentforce Sales Coach** | Quien lo **administra y configura** |
| **Use Agentforce Sales Coach** | Vendedores que lo **usan** |

![[coach-acceso-usuarios.jpg]]

## 📄 Componente en la oportunidad
Desde el paso 1, **Go to App Builder** → arrastrar **Agentforce Sales Coach** encima de las Related Lists en la **Opportunity Record Page** → Save → Activate → **Assign as Org Default** (Desktop).

![[coach-pagina-oportunidad.png]]

## 4️⃣ Configure and Activate Agentforce Sales Coach
**Go to Agent Builder** → plantilla **Agentforce Sales Coach** → revisar que estén todos los topics → Define Settings:
- Name *Sales Coach Agent*, API Name `Sales_Coach_Agent`, descripción, **Role** y **Company**.
- **Agent User**: el Sales Coach Agent creado.
- ✅ **Keep a record of conversations with Enhanced Event Logs** para revisar el comportamiento.

Idioma y tono por defecto → Select Data en blanco → **Create**. Luego se pueden subir más recursos con el **ícono del libro** del menú lateral.

![[coach-agent-builder.jpg]]

> ⚠️ Ojo de examen: el agent user de Sales Coach usa licencia **Einstein Agent** y perfil **Einstein Agent User**. Tres permission sets distintos: **Sales Coach Agent** (el agente), **Manage** (admins) y **Use** (vendedores). Agentforce **no está** en un Trailhead Playground normal.

> 🧩 El proyecto *Build Your First Sales Coach* repite este setup y sigue con [[🛠️ Personalizar el role-play de Sales Coach paso a paso]].

## 🔁 Repaso #flashcards
¿Dónde está el wizard de Sales Coach?::En Setup > Agentforce Sales Coach.
¿Cuáles son los 4 pasos del wizard de Sales Coach?::Enable, Create a User, Grant Access, y Configure and Activate.
¿Qué licencia y perfil lleva el agent user de Sales Coach?::Licencia Einstein Agent y perfil Einstein Agent User.
¿Qué permission set se asigna al agent user de Sales Coach?::Sales Coach Agent.
¿Qué permission set necesita quien administra Sales Coach?::Manage Agentforce Sales Coach.
¿Qué permission set necesita un vendedor para usar Sales Coach?::Use Agentforce Sales Coach.
¿Dónde se agrega el componente de Sales Coach?::En la Opportunity Record Page con Lightning App Builder, activada como Org Default.
¿Qué casilla guarda las conversaciones del Sales Coach para revisarlas?::Keep a record of conversations with Enhanced Event Logs.
