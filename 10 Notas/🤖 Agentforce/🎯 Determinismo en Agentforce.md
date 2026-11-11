---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-30
---
# 🎯 Determinismo en Agentforce

Cuando una regla de negocio **cuesta dinero o es crítica** (ej: dar créditos solo a clientes elegibles), no basta con pedírselo al LLM en el prompt: **las instrucciones de prompt no son deterministas**, y un LLM se equivoca o un cliente lo convence.

Agentforce trae **capacidades de programación en el Canvas** para crear flujos deterministas:

| | Herramienta | Qué controla |
|---|---|---|
| 🔣 | [[🔣 Variables de agente]] | Guardan el **estado** (ej: lifetime value, si ya se dio un crédito) |
| 🔀 | [[🔀 Instrucciones condicionales]] | **Qué prompt** recibe el LLM según el estado |
| 🚫 | [[🚫 Filtros de acciones]] | **Qué acciones puede ver** el LLM |

💡 **La idea clave:** tus **reglas y datos deciden la ruta** del agente; el **LLM conversa y razona dentro de esa ruta**. En cada turno, Agentforce resuelve la lógica, arma un **prompt a la medida** y define las **acciones elegibles**, y solo eso llega al LLM. Ver [[🌍 Atlas Reasoning Engine]] (razonamiento híbrido) y [[📜 Agent Script]].

## 🏝️ El caso Coral Cloud
Créditos de resort por lealtad, según el `Lifetime_Value__c` del contacto:
- 💎 **Platinum** (≥ 50,000) → agradecer + crédito de **$500**.
- 🥇 **Gold** (≥ 25,000 y < 50,000) → agradecer + crédito de **$250**.
- 👤 Resto → ni mensaje ni crédito.
- 🔒 **Un solo crédito por sesión**.

Pasos: el flow devuelve el campo → [[🔐 Permisos del usuario del agente|permiso al usuario del agente]] → variable → condicionales → acción + filtro.

🧭 También se puede guiar al **Agent Router** con una instrucción: "si el cliente da su email y número de membresía, corre `{!@actions.go_to_Experience_Management}`", para que entienda que se está verificando y no solo charlando. Ver [[🗺️ Explorer del Agentforce Builder]].

![[determinismo-agent-router-script.jpg]]

> ⚠️ Ojo de examen: si una regla de negocio **debe cumplirse siempre**, la respuesta es **determinismo** (variables + condicionales + **filtros de acciones**), **no** "instrucciones más estrictas en el prompt".

## 🔁 Repaso #flashcards
¿Por qué no basta con instrucciones en el prompt para hacer cumplir una regla de negocio?::Porque las instrucciones de prompt no son deterministas: el LLM puede equivocarse o un cliente puede convencerlo.
¿Qué tres herramientas da Agentforce para el determinismo?::Variables, instrucciones condicionales (if) y filtros de acciones.
En un agente determinista, ¿qué decide la ruta y qué hace el LLM?::Las reglas y los datos deciden la ruta; el LLM conversa y razona dentro de ella.
¿Qué llega al LLM en cada turno?::Solo el prompt resultante de resolver la lógica y las acciones elegibles.
