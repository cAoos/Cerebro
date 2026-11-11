---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-07
---
# 🛠️ Crear un agente de voz paso a paso

Proyecto de Ursa Major Solar del módulo *Agentforce Voice: Quick Look*. El concepto está en [[🎙️ Agentforce Voice]].

![[voz-proceso-setup.png]]

## 1️⃣ Crear el agente de voz
Prerrequisito: **Agentforce activado** en la org.
1. App Launcher → **Agentforce Studio** → pestaña Agents → **New Agent**.
2. Plantilla **Agentforce Service Agent**. En Agent Details, elegir o crear el **Agent's User Record**.
3. Nombre **Inbound Voice Service Agent** → **Let's Go**.

![[voz-nombrar-agente.jpg]]

4. Settings → **Agent Details**: descripción. Settings → **System**: **instrucciones a nivel de agente** (rol y empresa que representa).
5. **Language Settings**: idioma por defecto **soportado para voz**.
6. Revisar los **subagentes** y sus acciones → **Save**.

![[voz-instrucciones-agente.jpg]]

## 2️⃣ Agregar la conexión de telefonía
Explorer → Connections → **Add Connection** → **Telephony** → **Add to Agent**. Un banner invita a ir a Voice Settings. Ver [[🔌 Conexiones y canales de un agente]].

![[voz-agregar-conexion.jpg]]

## 3️⃣ Elegir la persona de voz
Explorer → Agent Definition Settings → **Voice Settings**: persona en **Basic**, ajustes finos en **Advanced**. Detalle en [[🎙️ Agentforce Voice]].
Luego **Save** → **Commit Version** → **Activate**. Sin activar, **no se puede configurar el inbound routing**. Ver [[🏷️ Versiones de un agente]].

## 4️⃣ Flow de Omni-Channel para las llamadas entrantes
Los Omni-Channel flows son **el cerebro de enrutamiento** de Salesforce Voice: cuando entra una llamada, el **inbound flow** asociado decide quién la atiende.
1. Setup → **Flows** → **New Flow** → **Omni-Channel Flow**.

![[voz-omni-channel-flow.jpg]]

2. Toolbox → **New Resource**: Variable, API Name **recordId**, tipo **Text**, **Available for input** marcado. Guarda el **Id del registro de la llamada** (VoiceCall).

![[voz-variable-recordid.png]]

3. ➕ → elemento **Route Work**: entrega la llamada a Omni-Channel para que la encole y la empuje en tiempo real al agente.

| Campo | Valor |
|---|---|
| How Many Work Records to Route? | **Single** |
| Record ID Variable | **{!recordId}** |
| Service Channel | **Phone** |
| Route To | **Agentforce Service Agent** → Inbound Voice Service Agent |
| Fallback Queue | **Queue** → Default Queue (red de seguridad si el destino no acepta el trabajo) |

![[voz-route-work.png]]

4. Guardar como **Voice Call Handling Flow** → **Save** → **Activate**.

Es el mismo patrón que en chat. Ver [[🔀 Enrutamiento Omni-Channel de un agente]] y [[🧑‍⚖️ Cómo decide Omni-Channel a quién asignar]].

## 5️⃣ Conectar el flow al canal de voz
1. Setup → **Communication Channels** → pestaña All Channels → abrir el canal de voz.
2. Sección **Omni-Channel Routing** → **Edit** → en **Flow Definition** elegir el flow.
3. Agregar una **Fallback Queue** → **Save**.

![[voz-canal-flow-definition.jpg]]

Se puede usar un canal de voz existente o crear uno nuevo procurando un número por PSTN (ver la sección del canal PSTN en [[🎙️ Agentforce Voice]]).

> ⚠️ Ojo de examen: el orden es **agente → flow → canal**. El agente se crea con la plantilla **Agentforce Service Agent** y un idioma **soportado para voz**, y debe estar **activo** antes del routing. En el flow: variable **recordId** (Text, input), **Route Work** con Service Channel **Phone**, Route To **Agentforce Service Agent** y una **fallback queue**. El flow se pega al canal en **Communication Channels → Omni-Channel Routing → Flow Definition**.

## 🔁 Repaso #flashcards
¿Cuáles son los tres pasos para poner un agente de voz a atender llamadas?::Crear el agente de voz, construir un flow que enrute las llamadas entrantes y conectar ese flow al canal de voz.
¿Qué plantilla se usa para crear un agente de voz entrante?::Agentforce Service Agent.
¿Qué condición de idioma debe cumplir un agente de voz?::Su idioma por defecto debe estar soportado para voz.
¿Qué tipo de flow enruta las llamadas entrantes al agente de voz?::Un Omni-Channel Flow (el inbound flow).
¿Qué variable necesita el Omni-Channel flow de voz?::recordId, de tipo Text y Available for input, con el Id del registro de la llamada.
¿Cómo se configura Route Work para mandar una llamada al agente de voz?::Single, Record ID = recordId, Service Channel = Phone, Route To = Agentforce Service Agent con el agente elegido, y una fallback queue.
¿Para qué sirve la fallback queue en Route Work?::Es la red de seguridad cuando el destino principal no puede aceptar el trabajo.
¿Dónde se conecta el flow al canal de voz?::Setup → Communication Channels → el canal de voz → Omni-Channel Routing → Flow Definition, más una fallback queue.
