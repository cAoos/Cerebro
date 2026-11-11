---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-05
---
# 🛠️ Personalizar un Service Agent paso a paso

Proyecto práctico: el agente de servicio de **Coral Cloud Resorts**, que debe aguantar los picos de temporada **sin contratar personal estacional**. Se mejoran una **plantilla**, el **modelo**, un **flow**, una **acción** y un **subagente**. La regla de fondo: **los subagentes contienen acciones, y las acciones usan flows, plantillas, etc.** Todo se puede editar después de creado.

## 0️⃣ El usuario del agente
**Setup → Users →** EinsteinServiceAgent User **→ Edit**: Company = Coral Cloud Resorts, **Profile = Einstein Agent User**. Ver [[🔐 Permisos del usuario del agente]].

![[service-agent-perfil-agent-user.jpg|400]]

## 1️⃣ Mejorar la plantilla *Generate Personalized Schedule*
Se agregan recursos nuevos:
- **Current User**: `User.FirstName User.LastName` y `User.CompanyName`. El agente se presenta con su nombre: *"Always introduce yourself with your full name…"*.
- **Contact → Record Snapshot** (`RecordSnapshot:myContact`): mete **todo el registro del contacto** de una vez.
- Ya traía un recurso **Apex** (`PersonalizeGuestExperiences`) con las actividades.

![[service-agent-record-snapshot.jpg|400]]

**Save & Preview** con Sofia Rodriguez. Se puede cambiar **Response Language** para ver la respuesta en otros idiomas.

## 2️⃣ Modelo más predecible
Modelo custom **Business Writing** con **temperatura 0.3**: la respuesta queda más formal y predecible. Ver [[🌡️ Temperatura y modelos custom]]. Luego **Activate**.

## 3️⃣ Actualizar el flow
**Get Experience Details** no devolvía el **precio**:
- En el elemento *Get Experience by Name*: **Add Field → Price__c**.
- Cambiar la **descripción** del elemento *Assign Experience Record*.
- **Save As New Version → Activate**.

![[service-agent-flow-price.jpg|300]]

## 4️⃣ Actualizar la acción del agente
**Setup → Agentforce Assets → Actions → Get Experience Details →** editar con ✏️ la instrucción del output `experienceRecord`.

> 🔑 Cuando se **crea** una acción, las descripciones del flow **se copian solas** como instrucciones de inputs y outputs. Si la acción **ya existía**, hay que **actualizarlas a mano**.

## 5️⃣ Importar el agente desde un script
**New from Script →** pegar **→ Create Agent →** asignar el **EinsteinServiceAgent User → Save**. Ver [[🧾 Estructura de un Agent Script]].

## 6️⃣ Instrucciones con el asistente de IA del Builder
En el panel del **AI assistant** del Builder, se le pide en lenguaje natural agregar dos instrucciones al subagente **Customer Experience Support**:
1. Si preguntan por nombre, descripción, nivel, tipo o **precio** de una experiencia → `{!@actions.Get_Experience_Details}`.
2. Si piden **recomendaciones** → `{!@actions.Generate_Personalized_Schedule}`, pasando el contacto de `{!@actions.Get_Customer_Details}`.

**Accept All → Save → Commit Version → Activate.**

> 💡 Decir **qué acción usar en qué caso** es un **guardrail**: limita al agente, pero la IA sigue interpretando la petición. Ver [[📝 Instrucciones de razonamiento]].

## 7️⃣ Probar
**Preview →** cambiar a **Simulate Mode**, que no afecta los datos reales. Ver [[🧪 Probar un agente en el Builder]].
- *"Tell me more about the Guided Nature Walk."* → ahora incluye el **precio**.
- *"Book 2 people … for tomorrow"* → pide **email y número de membresía** antes de reservar.
- *"Generate a personalized schedule…"* → usa los intereses de Sofia y el modelo Business Writing.

> ⚠️ Ojo de examen:
> - Si cambias un flow, la acción **existente** **no** toma las nuevas descripciones: se editan en **Agentforce Assets → Actions**.
> - Cambio en un flow activo: **Save As New Version → Activate**.
> - **Record Snapshot** mete todo el registro en el prompt.
> - El usuario del agente lleva el perfil **Einstein Agent User**.
> - Para probar sin tocar datos: **Simulate Mode**.

## 🔁 Repaso #flashcards
Actualizaste la descripción de un output en el flow. ¿La acción de agente existente la toma sola?::No. Solo se copian al crear la acción; en una existente se editan a mano en Agentforce Assets → Actions.
¿Qué perfil se le asigna al usuario de un Service Agent en el proyecto?::Einstein Agent User.
¿Qué hace el recurso Record Snapshot en Prompt Builder?::Inserta en el prompt el registro completo (p. ej. el contacto) de una sola vez.
¿Cómo se agrega el nombre del usuario actual a un prompt?::Insert Resource → Current User → First Name / Last Name / Company Name.
¿Para qué sirve el AI assistant del Agentforce Builder?::Para armar o modificar el agente en lenguaje natural, por ejemplo agregar instrucciones a un subagente.
¿Por qué indicar en las instrucciones qué acción usar en cada caso?::Es un guardrail: dirige al agente sin quitarle la interpretación de la petición.
¿Qué modo de prueba no afecta los datos reales?::Simulate Mode (Live Test sí trabaja con datos reales).
