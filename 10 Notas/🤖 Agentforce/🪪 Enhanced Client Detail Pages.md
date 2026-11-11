---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-09
---
# 🪪 Enhanced Client Detail Pages

Páginas de perfil **unificadas** del cliente y de su hogar en [[🧑‍💼 Agentic Advisor]]. Muestran salud financiera, historial de la relación, reuniones y acciones recomendadas en **una sola vista**, sin saltar entre sistemas.

## 👤 Persona y 🏠 hogar
| Página | Objeto | Se centra en |
|---|---|---|
| Individual | **Person Account** | Las cuentas y metas de una persona |
| Hogar (household) | **Account** | El panorama financiero de **todos los miembros** |

🏠 Los hogares usan el **householding data model**. Se crean desde la list view de Account con un **flow incluido**, y se ven y actualizan con otros flows incluidos. El admin no los construye desde cero.

## 🔌 De dónde salen los datos
| Fuente | Datos |
|---|---|
| **Salesforce** | Cuentas, casos, tareas, historial de reuniones, relaciones (Agentforce Financial Services) |
| **Data 360** | Cuentas financieras, desempeño del portafolio y calculated insights de **otros sistemas** (por ejemplo, custodios) |

## 🧱 Componentes
- 👨‍👩‍👧 **Household Snapshot:** miembro principal, roles y contacto. **Solo en páginas de hogar.**
- 💓 **Client Pulse:** usa el componente **AI Summary** con una **plantilla de prompt incluida** para resumir el sentimiento y el engagement del cliente, sacando señales escondidas en datos estructurados. En un hogar incluye a todos los miembros.
- 💡 **Insights and Actions:** next best actions según los datos y las metas.
- 📈 **Financial Portfolio:** datos financieros en **tiempo real** de fuentes externas vía Data 360, así que los números coinciden con lo que ve el cliente.
- 🕸️ **Relationships:** miembros y contactos relacionados en un grafo del **Actionable Relationship Center**.

![[advisor-client-pulse.jpg]]
![[advisor-financial-portfolio.jpg]]

## 🧪 Ejemplo
Ryan abre la página del cliente en riesgo que le marcó Run My Day. El Client Pulse le muestra poco engagement reciente; el portafolio, un retiro grande. Insights and Actions sugiere contactarlo, y Ryan decide agendar una reunión.

> ⚠️ Ojo de examen: **Client Pulse es un ejemplo de prompt template** puesto en una página con el componente **AI Summary**: grounding en datos estructurados para generar un resumen. Persona → **Person Account**; hogar → **Account** con householding.

## 🔁 Repaso #flashcards
¿Qué objetos usan las Enhanced Client Detail Pages para persona y hogar?::Person Account para el individuo y Account (householding data model) para el hogar.
¿Cómo genera Client Pulse su resumen?::Con el componente AI Summary y una plantilla de prompt incluida, sobre datos estructurados del cliente.
¿Qué componente solo aparece en la página de hogar?::Household Snapshot.
¿De dónde vienen los datos de portafolio en tiempo real de la Client Detail Page?::De sistemas externos (custodios) a través de Data 360.
¿Qué muestra el componente Relationships?::Miembros del hogar y contactos relacionados en un grafo del Actionable Relationship Center.
