---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-05
---
# 🛠️ Conectar un flow a un agente paso a paso

Proyecto práctico: el **Order Agent** de Edge Communications. Primero se le agrega un **subagente estándar** y se prueba; después se le da una **acción custom** que llama a un **flow existente** para **iniciar la devolución** de un pedido. La teoría está en [[⚡ Acciones de agente]] y [[🔩 Configurar una acción custom]].

> 💡 El proyecto se llamaba *Quick Start: Einstein Copilot*; hoy todo es **Agentforce**.

## 0️⃣ Encender Agentforce Studio
**Setup → Salesforce Go →** buscar **Agentforce Studio → Get Started → Turn On → Confirm**, y refresca.

## 1️⃣ Agregar un subagente estándar
**App Launcher → Agentforce Studio → Agents → Order Agent.** En el **Explorer**, sobre **Subagents**: **+ → Add from Asset Library →** buscar **General CRM → Select → Add to Agent → Save**.

![[flow-agente-add-from-asset-library.jpg|400]]

Los subagentes **agrupan acciones relacionadas**. **General CRM** ya trae muchas **acciones estándar**, por ejemplo *Query Records*, que busca registros según lo que pide el usuario.

![[flow-agente-general-crm-acciones.jpg|300]]

## 2️⃣ Probar en Live Test Mode
**Preview →** escribir *"Tell me about the orders for the account Edge Communications."*

![[flow-agente-live-test.jpg|500]]

El **Interaction Summary** muestra el plan del agente: **dos acciones**, primero **identificar la cuenta** y luego **buscar sus pedidos**. Ver [[🧪 Probar un agente en el Builder]].

![[flow-agente-interaction-summary.jpg|600]]

**Memoria de la conversación:** si después preguntas *"What is the oldest order?"*, entiende que hablas de los pedidos de Edge Communications sin que lo repitas.

> 💡 Como llama a un LLM, las respuestas **pueden variar** entre una prueba y otra.

## 3️⃣ Crear la acción custom que llama al flow
En el subagente **General CRM → + → New Action**:

| Campo | Valor |
|---|---|
| Action Name | Initiate Return |
| Description | *Initiate Return for requests to return or refund orders or products in an order.* |
| Reference Action Type | **Flow** |
| Reference Action | **Initiate Return** (el flow que ya existía) |

**Create and Open**, y luego:
- 📥 **Input**, descripción *"Populate this input variable with an Order recordId."* + ✅ **Require Input to execute action**
- 📤 **Output**, descripción del estado de la devolución + ✅ **Show in conversation**
- ⏳ **Additional Settings →** ✅ **Show Loading text for this action**: *"Initiating your return or refund."*

> 🔑 Las **descripciones son críticas**: forman **parte del prompt** que Agentforce manda al LLM. Con una descripción clara, el agente **reconoce cuándo usar** la acción.

## 4️⃣ Publicar
**Save → Commit Version → Activate.** Ver [[🏷️ Versiones de un agente]].

## 5️⃣ Usarlo como usuario
**Sales app → Home →** abrir el panel del Order Agent:
1. *"What is the order with the most recent order start date? Please provide a clickable link to the order."* → muestra el pedido **00000101** con link.
2. Abrir el pedido y escribir *"Start a return for this order"* → el agente elige **Initiate Return**, corre el flow y da el estado.
3. En **Details** del pedido, **Return Status = Initiated**.

![[flow-agente-return-status.jpg|400]]

**Lección:** con unos clics, la **automatización propia de la empresa** (flows que ya existen) entra al catálogo de acciones del agente.

> ⚠️ Ojo de examen:
> - Para reusar un flow existente en un agente: **acción custom** con **Reference Action Type = Flow**.
> - Las **descripciones** de la acción y de sus inputs/outputs **son prompt** y deciden si el agente la elige.
> - **Show Loading text** = el mensaje que ve el usuario mientras corre la acción.
> - Antes de que los usuarios la vean: **Commit Version → Activate**.
> - El **Interaction Summary** muestra qué acciones planeó el agente.

## 🔁 Repaso #flashcards
¿Cómo se agrega un subagente estándar como General CRM a un agente?::En el Explorer del Builder: + en Subagents → Add from Asset Library → buscar → Select → Add to Agent.
¿Cómo se convierte un flow existente en una capacidad del agente?::Creando una acción custom con Reference Action Type = Flow y Reference Action = ese flow.
¿Por qué son críticas las descripciones de una acción custom?::Porque forman parte del prompt que Agentforce envía al LLM y deciden cuándo el agente usa la acción.
¿Qué hace "Show Loading text for this action"?::Muestra al usuario un mensaje mientras la acción se ejecuta.
¿Qué hay que hacer después de guardar los cambios del agente para que los usuarios los usen?::Commit Version y luego Activate.
¿Qué muestra el Interaction Summary en Live Test?::El proceso del agente: qué acciones decidió ejecutar y en qué orden.
¿Qué hace la acción estándar Query Records?::Busca y recupera registros de Salesforce según la petición y las condiciones del usuario.
