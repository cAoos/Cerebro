---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-09
---
# 🧑‍💼 Agentic Advisor

Espacio de trabajo **inteligente, con IA**, para asesores financieros *high-touch*. Es parte de [[💳 Agentforce for Financial Services]]: **nativo de Salesforce**, construido sobre el **modelo de datos de Agentforce Financial Services** y con cumplimiento de nivel empresarial.

🎯 El problema que ataca: los asesores gastan **casi el 70 % de su tiempo** en tareas que no son atender clientes. Pierden una hora o más cada mañana juntando información de sistemas aislados, y el cliente que se siente "un número" se va.

## 🧩 Las cuatro piezas
| Pieza | Qué hace | Nota |
|---|---|---|
| ☀️ **Run My Day** | Briefing diario **priorizado** por categorías | [[☀️ Run My Day]] |
| 🪪 **Enhanced Client Detail Pages** | Vista unificada de la persona y del hogar (Salesforce + Data 360) | [[🪪 Enhanced Client Detail Pages]] |
| 🗓️ **Meeting Concierge** | Reuniones de la preparación al seguimiento, de horas a minutos | [[🗓️ Meeting Concierge]] |
| 🤝 **Intelligent Referral Management** | Capturar, enrutar y seguir referidos | [[🤝 Intelligent Referral Management]] |

## 🔄 Cómo encajan
```text
Data 360 (DMO mappings + First Party Connectors) + datos de Agentforce Financial Services
        │
        ▼
🪪 Client Detail Pages ──► ☀️ Run My Day (prioridades, referidos) ──► 🗓️ Meeting Concierge
        ▲                                                                   │
        └──────── datos e insights nuevos vuelven al dataset ◄── 🤝 Referidos ◄┘
```
- 🗃️ **Base: Data 360.** Agentforce Financial Services trae los **mapeos a DMOs** y **First Party Connectors** de la industria para integrar rápido.
- 🔁 **Ciclo virtuoso:** todo lo que se genera vuelve al dataset y mejora la priorización del día siguiente.

## 👥 Beneficio por rol
- 🧑‍💼 **Asesor:** más tiempo con clientes; el sistema hace la preparación y la parte administrativa, y el asesor **revisa y decide**.
- 🛠️ **Admin:** setup guiado y low-code, en **días, no meses**, a partir de una plantilla.
- 📈 **Dirección:** ROI rápido; la IA pasa *"de asistencia a acción"* y crecen los ingresos y los **AUM**.

## 🧪 Ejemplo
Un día de Ryan, asesor de Cumulus Wealth:
1. Run My Day le muestra un cliente en riesgo.
2. La Client Detail Page le explica por qué.
3. Meeting Concierge prepara, acompaña y cierra la reunión.
4. En el seguimiento sale un referido para hipotecas, que va con Intelligent Referral Management.

> ⚠️ Ojo de examen: la base de Agentic Advisor es **Data 360 unificando datos**, junto con el modelo de datos de la industria. Es el mismo principio de grounding de todo Agentforce: **sin datos unificados no hay buenos insights**.

## 🔁 Repaso #flashcards
¿Qué es Agentic Advisor?::Un espacio de trabajo inteligente con IA para asesores financieros high-touch, parte de Agentforce for Financial Services.
¿Cuáles son las cuatro piezas de Agentic Advisor?::Run My Day, Enhanced Client Detail Pages, Meeting Concierge e Intelligent Referral Management.
¿Qué trae Agentforce Financial Services para integrar Data 360 rápido?::Mapeos a DMOs y First Party Connectors específicos de la industria.
¿Qué porcentaje de su tiempo dedican los asesores a tareas que no son atender clientes, según el módulo?::Casi el 70 %.
