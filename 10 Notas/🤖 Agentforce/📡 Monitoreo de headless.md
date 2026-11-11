---
tipo: nota
tema: seguridad
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 📡 Monitoreo de headless

El mínimo privilegio **reduce el riesgo, pero no lo elimina** (ni las alucinaciones). Por eso hacen falta dos cosas, **antes de pasar a producción**:
- 📡 **Monitoreo**: entender qué es normal y detectar lo que requiere atención (el chequeo de salud del árbol).
- 🚨 [[🚨 Respuesta a incidentes headless]]: una forma preparada de contener e investigar (el seguro y el teléfono del servicio de árboles).

## 🧰 Herramientas de Salesforce
| Herramienta | Qué registra | ⚠️ Qué **no** |
|-------------|--------------|----------------|
| 📊 **Event Monitoring** | Datos operativos: **logins, llamadas API**. Event Log Files, **Real-Time Monitoring** para bloquear amenazas, integración con CRM Analytics, Splunk, Datadog | — |
| 🛠️ **Setup Audit Trail** | **Cambios de configuración** en Setup: quién y cuándo | **No** registra las operaciones de datos del agente |
| 🕰️ **Field History Tracking** | Cambios de campos, **gratis** para todos, retención limitada ⚠️ | **No** registra prompts ni la interacción completa |
| 🗄️ **Field Audit Trail** | Más campos y retención **personalizada** (standalone o vía **Salesforce Shield**) | Tampoco prompts |

> [!warning]- ⚠️ Retención de Field History Tracking: por confirmar
> La unidad dice **30 días**, pero la documentación de Salesforce habla de **18 meses** (24 por API). Si sale en el examen, la idea clave es: **FHT = gratis y retención limitada**, **Field Audit Trail = más campos y retención personalizada**.

## 🌐 Monitorear la interacción completa
El monitoreo de Salesforce **termina en su frontera**, pero una interacción headless cruza varios sistemas:

```text
💬 Teams ─► 🧩 App propia (OAuth) ─► 🤖 Agente elige tool ─► ☁️ Operación en Salesforce ─► 🔙 Respuesta
```

**Ningún log por sí solo** describe todo el camino. Antes de producción, documenta: qué sistema es dueño de cada log, quién lo ve, cómo se **correlacionan** los registros, cuánto se retienen y si llevan datos regulados. Incluye:
- La app o superficie de terceros
- El middleware o API gateway
- El runtime del agente y el router de herramientas
- El **proveedor del modelo**
- Los logs y trazas propios

> ⚠️ Ojo de examen: "¿quién cambió una configuración en Setup?" → **Setup Audit Trail**. "¿Logins y llamadas API?" → **Event Monitoring**. "¿Más retención de historial de campos?" → **Field Audit Trail (Shield)**.

## 🔁 Repaso #flashcards
¿Qué registra Event Monitoring?::Datos operativos como logins y llamadas API; incluye Event Log Files y Real-Time Monitoring.
¿Qué registra Setup Audit Trail y qué no?::Los cambios de configuración en Setup (quién y cuándo); no las operaciones de datos del agente.
¿Diferencia entre Field History Tracking y Field Audit Trail?::FHT es gratis con retención corta; Field Audit Trail (Shield) cubre más campos con retención personalizada.
¿Por qué no basta el monitoreo de Salesforce en headless?::Porque termina en la frontera de Salesforce y la interacción cruza varios sistemas; hay que correlacionar logs externos.
