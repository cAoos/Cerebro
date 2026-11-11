---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-07
---
# 🔲 Agentforce Grid

Una **hoja de cálculo nueva dentro de Salesforce** que junta **datos, IA, agentes, prompt templates, fórmulas, evaluaciones y acciones invocables** en una sola interfaz. Sirve para construir **flujos de IA en lote** sin herramientas custom.

**Idea central:** cada **columna se apoya en la anterior**. Datos crudos → insight → acción.

## 🧱 Qué se hace en un Grid
- 📥 **Traer datos** de cualquier objeto del **CRM** o de **Data 360**: cientos de filas.
- ⚡ **Correr prompts o acciones a escala**, en paralelo sobre todas las filas.
- 🔗 **Encadenar** prompts, agentes y acciones: enriquecimiento → análisis → automatización.
- 🧪 **Prototipar en una fila, validar y escalar** a miles de registros bajo demanda.
- 🔁 **IA en batch**: pruebas multi-turn, minar transcripciones, actualizar registros.

## 🧩 Tipos de columna (los del módulo)
| Grupo | Columna | Qué hace |
|---|---|---|
| Data and Actions | **Salesforce** | Importa registros. **Query Mode** Object, Object Type, Fields, Filters y **One Result Per Row** / Max Results |
| AI Powered | **Prompt Template** | Corre una plantilla de [[🧾 Tipos de plantillas de Prompt Builder\|Prompt Builder]] **por cada fila** (Run For Each Row). Las **Template Variables** se llenan con **@columna** |
| AI Powered | **Use AI** | Instrucciones libres a un **modelo** elegido (por ejemplo GPT 5), con **Response Format** (Plain Text) |
| Data and Actions | **Record Update** | **Escribe de vuelta** en un campo del registro (Object Type, Object Field, valor = **@columna**) |
| — | **+ Column** desde el panel | **Extrae un campo** de una columna (Account.Id, o `content` del JSON de la plantilla) como columna propia |

- **@** referencia otras columnas en cualquier configuración.
- El panel derecho muestra **Output Preview** y la pestaña **JSON** con la salida real.
- Barra superior: **worksheets**, **Auto Update**, **Credits**, **Advanced Filter**.
- 💳 Correr columnas de IA **consume créditos**: *Update Column* muestra el costo estimado (por ejemplo ~20 créditos).

## 🚫 Adiós al "copy-paste tax"
Antes: exportar miles de registros a CSV, correr prompts en otra pestaña y pegar resultados en Salesforce. Con Grid **todo pasa dentro de Salesforce**: sin exportar datos ni saltar entre herramientas. El admin deja de atender pedidos de extracciones y updates masivos: **los usuarios lo hacen solos**.

## 🔐 Seguridad
Grid **respeta OLS y FLS del usuario que lo corre**: si no puede ver o editar un objeto o campo en la org, **tampoco en Grid**. El gobierno de datos existente se mantiene. Ver [[🔑 Mínimo privilegio en agentes]].

**Requisitos:** Agentforce activado (Salesforce Go → **Agentforce Studio**) y el permiso de sistema **Manage Agentforce Grids**.

## 👥 Quién lo usa
| Rol | Caso |
|---|---|
| Support lead | Miles de transcripciones → **artículos de FAQ** |
| RevOps manager | **Actualizar oportunidades viejas** en lote sin perseguir a los AEs |
| Demand gen manager | Redactar **outreach 1:1** según metas del miembro |
| Marketing ops manager | **Score y routing** de leads sin CSVs |
| SDR manager | 10K insights → **briefs de reunión** |
| Channel manager | De ciclos manuales de 12 semanas a **nudges quincenales** |
| Product ops lead | Logs de fallas de chat → **roadmaps listos para Jira** |
| Salesforce admin | **Probar modelos nuevos** contra datos reales antes de lanzar |

Paso a paso: [[🛠️ Crear un Agentforce Grid paso a paso]].

> ⚠️ Ojo de examen: Grid = **hoja de cálculo de IA en lote dentro de Salesforce**, columnas que **se encadenan**. Respeta **OLS y FLS del usuario que corre**. Requiere el permiso **Manage Agentforce Grids**. Elimina el **copy-paste tax** (exportar a CSV y pegar). Patrón: **prototipar en una fila → validar → escalar**.

## 🔁 Repaso #flashcards
¿Qué es Agentforce Grid?::Una hoja de cálculo dentro de Salesforce que junta datos, IA, agentes, prompt templates, fórmulas, evaluaciones y acciones invocables para correr flujos de IA en lote.
¿De dónde puede traer datos un Grid?::Del CRM de Salesforce o de Data 360.
¿Qué significa que en Grid "cada columna se apoya en la anterior"?::Las columnas se encadenan: datos crudos → insight (prompts, IA) → acción (actualizar registros).
¿Qué seguridad aplica Agentforce Grid?::OLS y FLS del usuario que lo corre: si no puede ver o editar un objeto o campo, tampoco en Grid.
¿Qué permiso de sistema hace falta para usar Grid?::Manage Agentforce Grids.
¿Qué es el "copy-paste tax" que elimina Grid?::Exportar registros a CSV, correr prompts en otra herramienta y pegar los resultados de vuelta en Salesforce.
¿Cuál es el patrón recomendado para construir un flujo en Grid?::Diseñar en una fila, validar y luego escalar a miles de registros bajo demanda.
¿Qué columna escribe resultados de vuelta en un registro?::Record Update.
¿Qué columna corre una plantilla de Prompt Builder por cada fila?::Prompt Template (Run For Each Row).
¿Cómo se referencia otra columna dentro de una configuración de Grid?::Con @ y el nombre de la columna.
¿Qué consume correr columnas de IA en Grid?::Créditos; Update Column muestra el costo estimado.
¿Para qué usaría un admin Agentforce Grid?::Para probar modelos nuevos contra datos reales antes de lanzarlos.
