---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-07
---
# 🛠️ Crear un Agentforce Grid paso a paso

Ejercicio *Account Summary* del módulo *Agentforce Grid*: resumir cuentas con IA y guardar el resumen en el campo **Description**. El concepto está en [[🔲 Agentforce Grid]].

Cadena de columnas: **Account → Account.Id → Summary → Summary.content → Markup → Update Description**.

## 0️⃣ Preparar la org
1. Setup → **Salesforce Go** → **Agentforce Studio**: si dice *Completed*, listo. Si dice *Set Up* → Get Started → **Turn On**.
2. Verificar el permiso **Manage Agentforce Grids**.

## 1️⃣ Crear el Grid
App Launcher → **Agentforce Grid** → **Create Grid** → **Create from Scratch** → nombre *Account Summary* y descripción → **Create**. Abre **Worksheet1** con 10 filas.

![[grid-nuevo.png]]

## 2️⃣ Columna de datos: Account
**Add Column** → Data and Actions → **Salesforce**. Título *Account*, **One Result Per Row** con Max Results **5**, Query Mode **Object**, Object Type **Account**, revisar **Fields** y **Filters** → **Save and Run**.

![[grid-columna-salesforce.jpg]]
![[grid-datos-cuentas.jpg]]

## 3️⃣ Aislar un campo: Account.Id
Clic en una celda de Account (sin tocar el link) → panel derecho → **+ Column** junto a **Id**.

![[grid-mas-columna.jpg]]

## 4️⃣ Columna de IA: Summary
**Add Column** → AI Powered → **Prompt Template**. Título *Summary*, plantilla **Account Summary** (corre **por cada fila**). En Template Variables, **objectToSummarize** = **@Account** → **Save and Run**.

![[grid-prompt-template.jpg]]

Si hay errores: clic derecho en el encabezado → **Update Column** (muestra el costo en créditos). Si siguen: Einstein Setup → **Reconnect Agents to Salesforce Services**.

![[grid-update-column.jpg]]

## 5️⃣ Sacar el contenido: Summary.content
Clic en la celda Summary → **Output Preview** → pestaña **JSON** → **+ Column** en el campo **content**. Ese texto viene en **HTML**.

![[grid-json-content.jpg]]
![[grid-summary-content.png]]

## 6️⃣ Columna de IA libre: Markup
**Add Column** → AI Powered → **Use AI**. Título *Markup*, modelo **GPT 5**, LLM Instructions: convertir el HTML a Markdown, con **@Summary.content** al final. Response Format **Plain Text** → **Save and Run**.

![[grid-use-ai-referencia.jpg]]

## 7️⃣ Escribir de vuelta: Update Description
**Add Column** → Data and Actions → **Record Update**. Object Type **Account**, Object Field **Account Description**, valor **@Markup** → **Save and Run**.

![[grid-record-update.jpg]]

Comprobar: app **Sales** → Accounts → una cuenta → **Details** → el campo Description trae el resumen.

> ⚠️ Ojo de examen: para usar una plantilla en Grid se elige la columna **Prompt Template** y se llenan sus **Template Variables con @columna**. Para extraer un campo de la salida, **+ Column** desde la pestaña **JSON**. Para guardar en Salesforce, **Record Update**. Si fallan las columnas de IA: **Update Column** o **Reconnect Agents to Salesforce Services**.

## 🔁 Repaso #flashcards
¿Dónde se abre Agentforce Grid y cómo se crea uno vacío?::App Launcher → Agentforce Grid → Create Grid → Create from Scratch.
¿Qué columna importa registros de Salesforce y qué se configura?::Salesforce: Query Mode (Object), Object Type, Fields, Filters y One Result Per Row / Max Results.
¿Cómo se convierte un campo de una columna en su propia columna?::Clic en la celda, y en el panel derecho + Column junto al campo.
¿Cómo se pasa un registro a una plantilla en Grid?::En la columna Prompt Template, Template Variables → escribir @ y elegir la columna (por ejemplo objectToSummarize = @Account).
¿Dónde se ve la salida real de una plantilla en Grid?::En el panel derecho, pestaña JSON de Output Preview.
¿Qué hacer si una columna de IA da errores en Grid?::Clic derecho en el encabezado → Update Column; si sigue, Einstein Setup → Reconnect Agents to Salesforce Services.
¿Qué columna da instrucciones libres a un modelo elegido?::Use AI, con LLM Instructions, Model y Response Format.
¿Qué configura la columna Record Update?::Object Type, Object Field y el valor (una @columna) que se escribe en el registro.
