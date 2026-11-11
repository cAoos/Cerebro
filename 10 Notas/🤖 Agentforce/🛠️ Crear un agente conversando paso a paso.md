---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-07
---
# 🛠️ Crear un agente conversando paso a paso

Ejercicio del **Trailhead headless IDE** (beta, solo en inglés): construir un [[🆘 Help Agent]] para hotelería **solo con lenguaje natural**, sin clics. El coding agent usa **modelos Claude** acotados a Salesforce, como un proyecto de Claude Code.

## 🗣️ Construir
1. 💬 Explorar: *"What kind of service agents can you build?"*. El agente razona y puede hacer **preguntas aclaratorias** (por ejemplo, la industria).
2. 🏨 Acotar: *"What kind of service agents are good to build for a hospitality company?"*
3. 🧱 Definir con nombres exactos:
   - Agente **Bookings Help Agent**, API name `bookings_help_agent`
   - Subagente **Reservation Management**: acciones **FinalizeReservation** y **GetReservationTimeSlots**
   - Subagente **Guest Complaints**: acción **CreateCase**
   - Si no das nombre, el agente inventa uno.
4. 🎭 Si pregunta la personalidad: *"warm" y "gracious"*.
5. 📜 Revisar el [[📜 Agent Script]] generado; si algo no cuadra, **pedir cambios en la conversación**.
6. 🚀 *"Deploy it."* → enlace **View in Agents list** (puede tardar en activarse).

## 🔍 Verificar y probar
7. **Launch** → App Launcher → **Agentforce Studio** → `bookings_help_agent` → **Subagents**: revisar acciones de cada subagente.
8. **Preview** en el Builder.

![[agente-conversacional-preview.jpg]]

9. Conversación de prueba: horarios del restaurante mañana → reservar el último → nombre y email → número de invitados → confirmar.

> ⚠️ Ojo de examen: el resultado de la conversación es un agente **normal**: queda en **Agentforce Studio** con sus [[🗂️ Subagentes]] y [[⚡ Acciones de agente]], y se prueba igual en el Builder ([[🧪 Probar un agente en el Builder]]). Los **mismos prompts** sirven para otros agentes cambiando el caso de uso.

Por qué funciona: [[🧑‍💻 Coding agents en Salesforce]].

## 🔁 Repaso #flashcards
¿Cómo se construye un agente en el headless IDE de Trailhead?::Conversando en lenguaje natural con un coding agent que genera el agente, su script y lo despliega.
¿Qué se puede hacer si el Agent Script generado no está como quieres?::Pedirle cambios al coding agent en la misma conversación antes de desplegar.
¿Qué prompt despliega el agente en el ejercicio?::"Deploy it."
¿Dónde se revisan los subagentes del agente creado por conversación?::En Agentforce Studio, abriendo el agente y la sección Subagents.
¿Qué subagentes y acciones tiene el Bookings Help Agent?::Reservation Management (FinalizeReservation, GetReservationTimeSlots) y Guest Complaints (CreateCase).
¿Qué pasa si no le das nombre al agente en la conversación?::El coding agent le pone uno.
¿Qué modelos usa el coding agent del headless IDE de Trailhead?::Modelos Claude, acotados al entorno de Salesforce.
