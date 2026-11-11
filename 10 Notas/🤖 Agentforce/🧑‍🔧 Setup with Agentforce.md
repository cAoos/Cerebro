---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 🧑‍🔧 Setup with Agentforce

Un **agente de IA para admins dentro de Setup**: completa tareas, da información y **resuelve problemas** conversando en lenguaje natural. Menos clics entre páginas, menos trabajo repetitivo y **siguiendo las buenas prácticas** de Salesforce.

## 🔌 Cómo activarlo
1. ☁️ Completar los pasos de configuración de **Data 360**.
2. 🔐 Verificar que los admins tengan los **permisos y acceso a componentes de Data 360**.
3. ✨ Habilitar **IA generativa** en la org y luego **Agentforce**.
4. ⚙️ En Setup → **Setup with Agentforce** → activarlo.
5. 🔄 Refrescar el navegador.

![[setup-agentforce-activar.png]]

## 💬 Cómo se usa
Desde **Setup Home** o con el botón **Ask Setup Agent** en cualquier página de Setup, escribes la pregunta o eliges una recomendación. Cada conversación nueva se abre en **una pestaña nueva**.

![[setup-agentforce-home.jpg]]

El agente responde con **list views, registros, documentación** y componentes que puedes expandir, muestra los cambios dentro del flujo de trabajo, **recomienda siguientes pasos** o te lleva a la página de Setup correcta.

> [!example]- 🖼️ "¿Jose Martinez tiene acceso a cuentas?"
> ![[setup-agentforce-permisos-usuario.png]]

## 🧰 Qué puede hacer
| Tarea | 🧪 Ejemplo |
|-------|-----------|
| 👥 **Gestionar usuarios** | "Clona a Peter Raj con sus asignaciones" · "Congela la cuenta de Erin" · "Resetea la contraseña de Lincoln" |
| 🔍 **Diagnosticar acceso** a objetos, campos y registros | "¿Por qué Candance no ve el contacto Jane Doe?" · "¿Jessica puede editar Priority en casos?" |
| 🔐 **Permission sets** y grupos | "Crea un permission set con lectura y edición en Account" |
| 🧱 **Objetos y campos personalizados** | "Crea un objeto Project con Start Date, End Date y Description" |
| 🌊 **Flows** | "Flow record-triggered que copie el teléfono de la cuenta a sus contactos" |
| 🧮 **Fórmulas**: arreglar y explicar | "Arregla esta fórmula" · "Explica esta validation rule" |
| 📊 **Uso y licencias** | "¿Nos estamos quedando sin almacenamiento?" |
| 📑 **Custom report types** | "Report type con Accounts, Contacts y Opportunities" |
| 📚 **Info de funcionalidades** | "¿Qué son las user access policies?" |

## 🛡️ Siempre bajo tu control
- ✅ **Pide confirmación antes de actuar**: apruebas o pausas el cambio.
- 🔐 Solo ayuda con tareas para las que **tú tienes permisos**.
- 📜 Todos sus cambios quedan en el **Setup Audit Trail** (ver [[📡 Monitoreo de headless]]).

> ⚠️ Ojo de examen: **prerrequisito: Data 360 + IA generativa + Agentforce**. ¿Dónde se rastrean los cambios del agente de Setup? → **Setup Audit Trail**. El agente **no** puede hacer nada que el admin no tenga permiso de hacer.

Relacionado: [[🎚️ Autoridad progresiva]] (confirmar antes de cambiar) · [[🤖 Agentforce]].

## 🔁 Repaso #flashcards
¿Qué es Setup with Agentforce?::Un agente de IA dentro de Setup que ayuda a los admins a completar tareas, obtener información y diagnosticar problemas conversando.
¿Qué prerrequisitos tiene Setup with Agentforce?::Data 360 configurado con permisos para los admins, IA generativa habilitada y Agentforce habilitado.
¿Dónde quedan registrados los cambios del agente de Setup?::En el Setup Audit Trail.
¿Desde dónde se abre el agente de Setup?::Desde Setup Home o con el botón Ask Setup Agent en cualquier página de Setup.
¿El agente de Setup puede hacer cambios que el admin no puede?::No; solo ayuda con tareas para las que el admin tiene permisos, y pide confirmación antes de actuar.
