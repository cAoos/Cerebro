---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[2026-10 Agentforce Specialist]]"
creada: 2026-11-08
---
# 🚚 Desplegar una plantilla de prompt a producción

Las plantillas de Prompt Builder son metadata **`GenAiPromptTemplate`** (carpeta `genAiPromptTemplates`, sufijo `.genAiPromptTemplate`). Se mueven de sandbox a producción con **change sets** o **Salesforce CLI / Metadata API**, como el resto de la metadata.

## ✅ Antes de desplegar
- 🧠 **Einstein Generative AI / Prompt Builder** habilitados en la org destino.
- 👤 Quien despliega y administra necesita **Prompt Template Manager**.
- 🧩 Todo lo que la plantilla **referencia** existe en destino o va en el mismo despliegue: **campos y objetos** de los merge fields, **flows** (Template-Triggered Prompt Flow), **clases Apex**, **retrievers** de Data 360.
- ⚙️ Si hay que desplegar **Settings** (habilitar funciones), van **en un despliegue aparte y antes** que las plantillas.

## 🔎 Después de desplegar
- 🏷️ Revisar **qué versión quedó activa** (campo `activeVersion`): no asumas que la activa del sandbox quedó activa en producción.
- 👥 Asignar **Prompt Template User** a quienes la ejecutan.
- 🔗 Si la usa un **agente** o un campo con **Field Generation**, revisar la acción del agente y la página con **Dynamic Forms**.
- 🧪 Probar con **Preview** y un registro real de producción.

> ⚠️ Ojo de examen: si un despliegue falla o la plantilla responde mal en producción, sospecha primero de **dependencias que faltan** (campo, flow, Apex, retriever) y de la **versión activa**. Es el mismo patrón que el agente completo: [[📦 Mover un agente a producción]].

> [!note]- 🌐 Fuentes
> [GenAiPromptTemplate en la Metadata API](https://developer.salesforce.com/docs/atlas.en-us.api_meta.meta/api_meta/meta_genaiprompttemplate.htm) y foros de la comunidad. El orden Settings → plantillas viene de la comunidad: confirmarlo.

## 🔁 Repaso #flashcards
¿Qué tipo de metadata es una plantilla de Prompt Builder?::GenAiPromptTemplate.
¿Con qué se despliega una plantilla de prompt?::Change sets o Salesforce CLI / Metadata API.
¿Qué debe existir en destino para que la plantilla funcione?::Prompt Builder habilitado y todo lo que referencia: campos, flows, Apex y retrievers.
¿Qué se revisa siempre después de desplegar una plantilla?::Qué versión quedó activa.
¿Qué permission set necesitan los usuarios que ejecutan la plantilla en producción?::Prompt Template User.
