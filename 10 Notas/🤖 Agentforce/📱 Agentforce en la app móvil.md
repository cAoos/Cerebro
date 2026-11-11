---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 📱 Agentforce en la app móvil

## ⚙️ Setup: ninguno
Si el admin ya **activó Agentforce y configuró un agente** en la org, **no hay que hacer nada más** para usarlo en la **Salesforce mobile app**. Todo lo de Agentforce está disponible **por defecto** en el móvil.

## 🚪 Puntos de acceso
| | Acceso | Cómo |
|---|---|---|
| 💬 | **Caja Ask Agentforce** | Abajo en la app. Escribir o tocar el **micrófono** (dar permiso de reconocimiento de voz y micrófono). **Opt in** a Agentforce y listo |
| ⚡ | **Shortcut (iOS)** | En la app Atajos: **Open Agentforce** y **Talk to Agentforce**. Abre la app directo en Agentforce |
| 🧩 | **Widget (iOS)** | En la pantalla de inicio, **sin abrir la app**. Mantener presionado → Edit → Add Widget → buscar Salesforce → widget de Agentforce |
| 🔒 | **Control Center / pantalla de bloqueo** | El atajo se agrega ahí: acceso al CRM **con un toque desde la pantalla bloqueada** (en iOS 18+ hasta reemplaza la linterna) |
| 🗣️ | **Siri** | "**Hey Siri, Ask Agentforce**". Funciona de forma nativa, sin desarrollo extra |

![[mobile-agentforce-ask.png|250]] ![[mobile-agentforce-shortcut.jpg|250]]
![[mobile-agentforce-widget.jpg|250]] ![[mobile-agentforce-lock-screen.jpg|250]]

## 🏃 Ejemplos con acciones estándar
Funcionan con un **agente por defecto** configurado:
- 📋 **Resumir**: "Resume la cuenta Acme y sus oportunidades" antes de una reunión.
- ✏️ **Actualizar registro**: "Actualiza el código postal a 12345". Agentforce **pregunta si el cambio es correcto** y luego se le pide **guardar**.

Las [[⚡ Acciones de agente|acciones]] y [[🗂️ Subagentes|subagentes]] estándar que se agreguen a Agentforce funcionan igual en móvil.

> ⚠️ Ojo de examen: usar Agentforce en móvil **no requiere configuración adicional** más allá de habilitar Agentforce y el agente en la org. Los accesos extra (**shortcut, widget, Control Center, Siri**) son de **iOS**. Al actualizar un registro, el agente **confirma antes de guardar**.

## 🔁 Repaso #flashcards
¿Qué configuración extra necesita Agentforce en la Salesforce mobile app?::Ninguna: si Agentforce y el agente ya están configurados en la org, funciona por defecto.
¿Cuáles son los puntos de acceso a Agentforce en móvil?::La caja Ask Agentforce (texto o micrófono), shortcuts, widget, Control Center/pantalla de bloqueo y Siri ("Hey Siri, Ask Agentforce"); los últimos cuatro en iOS.
¿Qué shortcuts trae la app Atajos para Agentforce?::Open Agentforce y Talk to Agentforce.
¿Qué hace Agentforce después de actualizar un campo por voz?::Pregunta si el cambio es correcto y luego se le pide guardar el registro.
