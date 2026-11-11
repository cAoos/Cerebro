---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 🧰 Casos de uso de Service Agent

[[🎧 Agentforce Service Agent]] se moldea con **[[🗂️ Subagentes|subagentes]] + [[⚡ Acciones de agente|acciones]] + instrucciones**. Una acción **no funciona sin subagente**, y un subagente **no sirve sin acciones**.

## 📦 Subagentes y acciones estándar
Dan un marco para tareas **públicas** comunes. Las tareas **privadas** (cambiar datos personales de una cita, hacer compras, pedir servicios de un contrato) **requieren configuración extra** antes de desplegar.

| Subagente estándar | El cliente pregunta | Instrucción de ejemplo | Acción estándar (Flow o Prompt Template) |
|---|---|---|---|
| 👤 **Account Management** | Número de cuenta, cuenta bloqueada, resetear contraseña | Verificar primero por **teléfono** y luego por **email** | Get Customer Details · Reset Password |
| 🎫 **Case Management** | Abrir ticket, estado del caso, actualizar caso | **Nunca mostrar el Case ID**; mostrar Case Number, Subject, Description, Status | Create a Case Record · Get Cases for Contact · Get Case by Case Number · Update Customer Contact Record |
| 📦 **Order Inquiries / Delivery** | ¿Cuándo llega?, cancelar, paquete perdido, cambiar entrega | Paquete perdido → **escalar de inmediato** a humano | Get Order by Order Number · Identify Customer by Email · Cancel Order · Get Delivery Time Slots · Finalize New Delivery Time |
| 📅 **Reservation Management** | Nueva reserva, modificar reserva | Cliente desconocido → pedir email y traer su contacto antes de reservar | Get Reservation Time Slots · Finalize Reservation |
| 🙋 **Escalation** | "¿Puedo hablar con un humano?" | Si lo pide **en cualquier momento**, escalar | Route Conversations to Agentforce for Service |
| ❓ **General FAQs** | Devoluciones, garantía, reclamos | Pregunta vaga → pedir detalles; si no sabe → ofrecer humano | **Answer Questions with Knowledge** |

## 🎨 Subagentes y acciones personalizados
Cuando se necesita algo más a la medida de la marca y el negocio. Las acciones custom pueden ser **Flow, Prompt Template o Apex**.

| Industria | El cliente pide | Acción custom de ejemplo |
|---|---|---|
| 🏥 Salud | Resumen de medicación, citas, médico en red | Confirm Patient Identity by Email or Phone · Get Appointment Time Slots · Retrieve Patient History Record |
| 🛍️ Retail | Precios, promociones, inventario, garantías | Retrieve Customer Order History · Get Current Product Pricing · Create New Claim Record |
| 💝 Nonprofit | Historial de donaciones, exención de impuestos | Access Customer Donation Records · Create New Donation |
| ✈️ Viajes | Estatus de lealtad, reservas, atracciones | Create Travel Reservation · Get Attraction Details |
| 🛡️ Seguros | Estado de reclamo, póliza, renovaciones | Create New Claim · Create Renewal Record · Modify Existing Policy |

> ⚠️ Ojo de examen: acciones **estándar** = **Flow o Prompt Template**; acciones **custom** pueden ser **Flow, Prompt Template o Apex**. Las **instrucciones** son donde pones reglas como "verifica identidad primero" o "escala si el paquete se perdió". Las tareas **privadas** necesitan configuración extra.

## 🔁 Repaso #flashcards
¿Qué relación hay entre subagente y acción?::Una acción no funciona sin estar ligada a un subagente, y un subagente no sirve sin acciones.
¿Qué tareas necesitan configuración extra antes de desplegar?::Las privadas: cambiar datos personales de una cita, hacer compras o pedir servicios de un contrato.
¿De qué tipo pueden ser las acciones custom de Service Agent?::Flow, Prompt Template o Apex.
¿Qué acción estándar responde FAQs?::Answer Questions with Knowledge, dentro del subagente General FAQs.
¿Dónde pones una regla como "nunca mostrar el Case ID"?::En las instrucciones del subagente Case Management.
