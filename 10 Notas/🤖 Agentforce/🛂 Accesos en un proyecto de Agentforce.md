---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-01
---
# 🛂 Accesos en un proyecto de Agentforce

Agentforce usa la seguridad de Salesforce, incluido el [[🛡️ Einstein Trust Layer]] (**gateway seguro** y acuerdos de **zero retention**). Además hay que planear permisos para **cuatro actores**:

| Actor | Cómo funciona |
|---|---|
| 🧑‍🔧 **Admin** | Para crear y gestionar agentes: permiso **Manage AI Agents** + los del tipo de agente, **o** **Customize Application** |
| 👔 **Empleado** (agente interno) | El agente corre **en el contexto del usuario logueado**: licencias, permisos, **FLS** y **sharing** de ese usuario deciden qué ve |
| 🙋 **Cliente** (canal externo) | Ciertas acciones solo tras **autenticar** al cliente (ej: preguntar por productos = libre; ayuda con un pedido = autenticarse) |
| 🤖 **Agente** | Algunos (ej: **service agents**) corren como **agent user**, con perfil y rol propios. Por defecto tiene **permisos limitados** (**mínimo privilegio**): hay que **darle todo lo que necesita** o no funcionará |

🧪 Los permisos casi nunca salen bien a la primera: **probarlos en sandbox**. Si el agente da errores en pruebas, **revisa sus permisos**.

Ver [[🔐 Permisos del usuario del agente]] y [[🔑 Mínimo privilegio en agentes]].

> ⚠️ Ojo de examen: agente **interno** = permisos del **usuario logueado**. **Service agent** = permisos del **agent user**. Permiso para crear agentes = **Manage AI Agents** (o Customize Application). Clientes = **autenticación** antes de acciones sensibles.

## 🔁 Repaso #flashcards
¿Qué permiso necesita un admin para crear y gestionar agentes?::Manage AI Agents más los del tipo de agente, o Customize Application.
¿Con qué permisos corre un agente interno que usan los empleados?::Con los del usuario logueado: licencias, permisos, FLS y sharing.
¿Con qué permisos corre un service agent?::Con los del agent user, que tiene perfil y rol propios.
¿Qué permisos tiene el agent user por defecto?::Un conjunto limitado (mínimo privilegio); hay que darle explícitamente lo que necesita.
¿Cómo se protege una acción sensible en un canal externo?::Exigiendo que el cliente se autentique antes.
