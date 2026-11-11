---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-09
---
# ☀️ Run My Day

Briefing diario **priorizado** del asesor dentro de [[🧑‍💼 Agentic Advisor]]. Junta señales de **Data 360 y Salesforce** en una sola vista para que no tenga que hacer triage entre sistemas.

- 🧮 Las necesidades del cliente las detectan los **Calculated Insights de Data 360**, a partir de hogares, cuentas financieras, señales del portafolio e historial de eventos.
- 🚀 Se abre desde el **App Launcher**, en la app Agentic Advisor.

![[advisor-run-my-day.jpg]]

## 🧱 Dos componentes
- 📅 **Calendar:** la agenda del día. Cada reunión trae un **indicador de preparación** enlazado a [[🗓️ Meeting Concierge]].
- 🏆 **Top Priorities:** prioridades rankeadas en tres niveles.

![[advisor-run-my-day-calendario.jpg]]

| Nivel | Qué es | Ejemplo |
|---|---|---|
| **Groups** | Necesidad de negocio | Retain, Service, Grow, Comply |
| **Insights** | Señales priorizadas dentro de un grupo | En Retain: "sin contacto reciente", "cumpleaños próximo" |
| **Details** | Tarjeta por cliente, con contexto y **acciones de un clic** | Draft Email, Schedule Meeting, Create Task |

![[advisor-top-priorities.jpg]]

## 🗂️ Los cuatro grupos
| Grupo | Qué trae |
|---|---|
| 🌱 **Grow** | **Referidos** de [[🤝 Intelligent Referral Management]] y señales de oportunidad (eventos de vida), con resumen IA |
| 🛟 **Retain** | Clientes **en riesgo**: riesgo de fuga, sin contacto reciente, **retiros grandes**. Muestra los AUM y la señal que dispara la alerta |
| 🧰 **Service** | Casos abiertos, seguimientos y tareas pendientes, ordenados por urgencia y cercanía a la próxima reunión |
| ⚖️ **Comply** | Obligaciones regulatorias con fecha: **KYC por vencer**, distribuciones mínimas requeridas (RMD) sin procesar |

⚙️ El **admin configura en Setup** qué grupos aparecen, qué insights se disparan, qué contexto muestra cada tarjeta y qué acciones hay. **Cada grupo es un frente de configuración aparte.**

## 🧪 Ejemplo
En Retain, Ryan ve un cliente sin contacto reciente. Desde la tarjeta usa **Draft Email**: Agentforce redacta el correo, Ryan lo revisa y edita, y lo envía.

> ⚠️ Ojo de examen: las prioridades **no se calculan a mano**. Salen de **Calculated Insights de Data 360** sobre datos unificados, y por eso es la forma de pasar de reactivo a proactivo. La IA **redacta**; el humano **revisa y envía**.

## 🔁 Repaso #flashcards
¿Qué herramienta de Data 360 alimenta las prioridades de Run My Day?::Calculated Insights, que construyen métricas sobre los datos unificados.
¿Cuáles son los dos componentes de Run My Day?::Calendar (agenda con enlace a Meeting Concierge) y Top Priorities.
¿Cuáles son los tres niveles de Top Priorities?::Groups (necesidad de negocio), Insights (señales priorizadas) y Details (tarjetas con acciones de un clic).
¿Cuáles son los cuatro grupos de ejemplo de Run My Day?::Grow, Retain, Service y Comply.
¿Qué grupo de Run My Day muestra KYC por vencer?::Comply.
¿Qué grupo de Run My Day muestra clientes en riesgo de irse?::Retain.
