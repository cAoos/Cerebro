---
tipo: nota
tema: prompts
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-27
---
# 🔗 Grounding de plantillas

Si el prompt tiene datos **escritos a mano** (nombres, empresa, ciudad), solo sirve para un caso. El **grounding** reemplaza esos datos por **recursos** de Salesforce que se resuelven en cada ejecución, y así la plantilla se vuelve **reutilizable**.

## 📦 Recursos disponibles
En el panel izquierdo del builder, **Resources**:

![[prompt-builder-recursos.png]]

- 🔤 **Merge fields** de los objetos de la plantilla (Sender, Recipient, Account…)
- 🌊 **Flows**: los **Template-Triggered Prompt Flows** agregan lógica compleja y **solo se ejecutan desde una plantilla** (ver [[🌊 Template-Triggered Prompt Flow]])
- 💻 **Apex**
- 🏢 **Current Organization**

## 🧪 Ejemplo: Sales Email con merge fields
Antes, con los datos escritos a mano:
```text
You are a Salesforce admin and your name is Linda Rosenberg from the organization Cloud Kicks. Your prospect is Rob Hutchinson, a director from Acme Inc., and they are based in Toronto, Ontario. …
```
Después, con merge fields:
```text
You are a {!$Input:Sender.Title} and your name is {!$Input:Sender.Name} from {!$Input:Sender.CompanyName}. Your prospect is {!$Input:Recipient.Name}, a {!$Input:Recipient.Title}. They are based in {!$Input:Recipient.MailingCity}. …
```
> 💡 Sintaxis: `{!$Input:Objeto.Campo}`. Las **listas relacionadas** se insertan como `RelatedList: Case.CaseComments` y salen en otro color (ver [[🛠️ Crear una plantilla Field Generation paso a paso]]).

> [!example]- Elegir un campo del Sender
> ![[prompt-builder-recursos-sender.png]]

> ⚠️ Ojo de examen: el grounding de plantillas se puede hacer con **merge fields, Flow y Apex**. Si piden lógica compleja o datos de varios registros → **Template-Triggered Prompt Flow**.

Aplica a todos los [[🧾 Tipos de plantillas de Prompt Builder]]. Es la versión en Prompt Builder de la idea de [[✅ Validar los resultados de la IA|dar datos de grounding]].

## ⚖️ Merge field o flow/Apex
| El enunciado pide… | Usa |
|---|---|
| Datos del registro, o su lista relacionada **tal cual** | Merge field / related list merge field |
| **Filtrar, ordenar, limitar, contar** o combinar objetos (p. ej. "las 3 oportunidades más recientes") | **Template-Triggered Prompt Flow** (low-code) o **Apex @InvocableMethod** (lógica compleja) |
| Buscar en texto no estructurado (artículos, PDFs) | Retriever de Data 360 |

> ⚠️ Ojo de examen: si hay que elegir uno solo entre flow y Apex, desempatan las palabras clave: *declarative / low-code* → **flow**; *complex logic / developer* → **Apex**. "Account Opportunity object" como recurso **no existe**: es un distractor.

## 🔁 Repaso #flashcards
¿Para qué sirven los merge fields en una plantilla?::Para reemplazar datos escritos a mano por campos de Salesforce y que la plantilla sea reutilizable (grounding).
¿Qué es un Template-Triggered Prompt Flow?::Un flow que agrega lógica compleja a una plantilla y solo se ejecuta desde ella.
¿Cuál es la sintaxis de un merge field en Prompt Builder?::{!$Input:Objeto.Campo}
¿Cuándo un related list merge field NO basta para grounding?::Cuando hay que filtrar, ordenar o limitar los registros (p. ej. "las 3 oportunidades abiertas más recientes"); ahí se usa un Template-Triggered Prompt Flow o Apex.
Grounding con lógica: ¿flow o Apex si el enunciado dice "low-code"?::Template-Triggered Prompt Flow (Apex si dice "complex logic" o "developer").
¿Sirve un retriever de Data 360 para traer las últimas oportunidades de una cuenta?::No; el retriever es para búsqueda semántica en texto no estructurado. Para registros CRM con filtro/orden → flow o Apex.
