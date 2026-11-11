---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-09
---
# 🧩 Skills de Agentforce for Financial Services

Seis plantillas de agente. Cada una necesita un setup un poco distinto, y algunas exigen activar otras funciones de Agentforce Financial Services (el detalle está en la Help).

| Skill | Para quién | Qué hace | Acciones típicas |
|---|---|---|---|
| 🏧 **Banking Service Customer Assistance** | **Cliente**, en web, sitios de terceros, **WhatsApp** y voz | **Verifica identidad** y luego deja que el cliente se atienda solo | Ver movimientos ("débitos de más de $500 del último mes"), **bloquear y reactivar** la tarjeta, reportar tarjeta perdida, robada, destruida o **retenida por el cajero** |
| 🧑‍💼 **Banking Service Employee Assistance** | **Service rep** | Lo mismo, pero para el rep, integrado con el **core bancario** | Get financial accounts, get transactions, get card details, **fee reversal case**, stop payment de cheque, saldos |
| 📊 **Financial Advisor Assistance** | Asesor o relationship manager | **Preparar** la reunión con el cliente | Wealth client summary, **portfolio performance summary**, asignación de activos actual frente a objetivo, planes y metas |
| 🤝 **Banking Relationship Assistance** | Banquero o asesor | **Cerrar** la reunión: notas, resumen, plan y tareas de seguimiento | Estructurar notas, interaction summary, **client plan objectives**, tareas de seguimiento |
| 🏠 **Loan Product Assistance** | **Cliente**, posible prestatario | Encontrar y **comparar** préstamos (hipoteca, auto, personal) | Detalle de producto, **estimar el monto** del préstamo |
| 💵 **Collections Assistance** | Especialista o gerente de cobranza | Cobranza más productiva y en cumplimiento | **Promise to pay**, guion de llamada según interacciones previas, **links de pago**, elegibilidad y creación de **caso legal** |

![[fs-analisis-de-metas.jpg]]
*Financial Advisor Assistance: el asesor pide un análisis de planes y metas del hogar y el agente resume el avance de cada meta.*

## 🔗 Cómo se encadenan
- **Antes** de la reunión: Financial Advisor Assistance. **Después**: Banking Relationship Assistance.
- La versión **Customer** desvía casos antes de que lleguen al rep. La versión **Employee** acelera los que sí llegan. Si algo es complejo, el agente **escala al rep con todo el contexto**.

💡 Algunas plantillas, como Financial Advisor Assistance, también funcionan con el **managed package** de Financial Services. En la Help está cuáles.

## 🧪 Ejemplo
Un hogar tiene 6 metas financieras. Antes de la revisión anual, la asesora le pide al agente un análisis de planes y metas: le marca que la jubilación está al 30 % de éxito y necesita revisión urgente. Después de la reunión, con Banking Relationship Assistance, dicta lo hablado y el agente crea la interacción, actualiza los objetivos del plan y deja las tareas de seguimiento.

> ⚠️ Ojo de examen: distingue **Customer** (el cliente se atiende solo, con verificación de identidad) de **Employee** (ayuda al rep). **Preparar** una reunión es Financial Advisor Assistance; **cerrarla** es Banking Relationship Assistance.

Parte de [[💳 Agentforce for Financial Services]] · Ejemplos: [[🏧 Agentes financieros en acción]]

## 🔁 Repaso #flashcards
¿Qué skill de Financial Services prepara la reunión con el cliente?::Financial Advisor Assistance (resumen del cliente, desempeño del portafolio, asignación de activos, planes y metas).
¿Qué skill de Financial Services cierra la reunión con el cliente?::Banking Relationship Assistance (notas, resumen, objetivos del plan, tareas de seguimiento).
¿Qué hace primero un agente de Banking Service Customer Assistance?::Verificar la identidad del cliente; luego lo ayuda a crear casos y completar tareas solo.
¿En qué canales se puede desplegar Banking Service Customer Assistance?::Portal web del banco, sitios de terceros, WhatsApp y teléfono (con Agentforce Voice).
¿Qué hace Loan Product Assistance?::Agente de cara al cliente que busca, explica y compara préstamos y estima el monto.
Acciones de Collections Assistance::Promise to pay, guion de llamada, links de pago, elegibilidad y creación de caso legal.
Diferencia entre Banking Service Customer y Employee Assistance::Customer: el cliente se atiende solo y desvía casos. Employee: ayuda al service rep integrado con el core bancario.
