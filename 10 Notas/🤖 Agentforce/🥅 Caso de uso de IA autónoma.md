---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-01
---
# 🥅 Caso de uso de IA autónoma

**Aplicación de IA donde un agente toma una acción o serie de acciones que cumplen un objetivo o trabajo (job to be done)** en nombre de empleados, clientes o la organización. Primer componente de [[🗒️ Planear un agente]].

## ✅ ¿Es buen caso para IA autónoma?
| | Pregunta |
|---|---|
| 💰 **Value** | ¿Por qué delegarlo? ¿El agente es más rápido, preciso o da mejor experiencia? |
| 🛠️ **Work** | ¿Puedes describir el trabajo? ¿Entiendes todos los procesos? |
| 🧠 **Decision-making** | ¿Las decisiones se pueden tomar **sin juicio humano directo**? ¿Hay **políticas y reglas claras** que el agente pueda seguir solo? |
| ⚠️ **Risk** | ¿Puede operar dentro de los requisitos de seguridad, legales, éticos y regulatorios? |
| 🗄️ **Data** | ¿Los datos soportan ese trabajo? |

💡 A menudo lo más fácil es **construir un agente de prueba** y ver si sus capacidades encajan.

## 📝 Definir el caso de uso (el **objetivo**, no la solución técnica)
1. 🧰 **Jobs to Be Done**: describir el trabajo y sus tareas. Coral Cloud: General FAQs, Reservation Management, Experience Management, Loyalty Program.
2. 📏 **Alcance**: el **MVP** es la **unidad de trabajo más pequeña** que tiene sentido entregar. Definir **criterios de aceptación** para salir en vivo **y no moverlos**. El alcance y la **autonomía** se pueden **reducir** si hay riesgo o faltan datos, y **ampliar** con la madurez.
3. 💵 **Valor de negocio**: metas específicas y medibles (ej: menos llamadas, más **case deflection**, soporte 24/7). Ayuda: **Agentforce ROI Calculator**.
4. 🗄️ **Preparación de datos**: no te emociones si los datos no alcanzan.
5. 📊 **Evaluar y priorizar** con el consejo de IA: [[📊 Matriz impacto-esfuerzo]].

| Reservation Management | Alcance |
|---|---|
| **V1 (MVP)** | Consultar reserva · reenviar itinerario. **Todo lo demás se escala a humanos** |
| **V2** | + Reservar y modificar · solicitudes especiales |
| **V3** | + Cancelar · reembolsar |

🗄️ **No es todo o nada**: los artículos de Knowledge de FAQs estaban desordenados, desactualizados y con huecos, así que Coral Cloud pospuso ese caso, pero probó un FAQ **solo de eventos**, cuyos artículos sí estaban al día.

Coral Cloud eligió **Reservation Management**: **alto impacto, datos listos y alcance de MVP**.

> ⚠️ Ojo de examen: los 5 criterios son **Value, Work, Decision-making, Risk, Data**. **MVP** = la unidad más pequeña que vale la pena entregar, con criterios de aceptación **fijos**. Si los datos no están listos, **reduce el alcance** o empieza por un subconjunto con datos buenos.

## 🔁 Repaso #flashcards
¿Qué es un caso de uso de IA autónoma?::Una aplicación de IA donde un agente toma una o varias acciones que cumplen un objetivo o trabajo en nombre de empleados, clientes o la organización.
¿Qué cinco aspectos evalúan si un caso sirve para IA autónoma?::Value, Work, Decision-making, Risk y Data.
¿Qué framework se usa para describir el trabajo del agente?::Jobs to Be Done.
¿Qué es el MVP de un agente?::La unidad de trabajo más pequeña que tiene sentido entregar, con criterios de aceptación definidos que no se mueven.
¿Qué hacer si un riesgo es alto o faltan datos?::Reducir el alcance o hacer al agente menos autónomo; se amplía cuando crece la madurez.
¿Qué hizo Coral Cloud con las FAQs si sus artículos no estaban listos?::Pospuso el caso general y probó un FAQ solo de eventos, cuyos artículos estaban actualizados.
