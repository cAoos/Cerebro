---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-07
---
# 🪨 Data foundation para headless

Conectar Claude, Cursor o Agentforce Vibes a la org toma minutos. Lo difícil es que **los datos estén listos**. Si un modelo apunta directo a tablas crudas sin una base gobernada, cada usuario arma su propia versión del flujo, los procesos se vuelven inconsistentes, la IA decide lo que deberían decidir las reglas de negocio y **desaparece el gobierno**.

La respuesta: dejar la **lógica de negocio dentro de Salesforce**, sobre datos **gobernados, unificados y listos** para que el agente actúe.

## 5️⃣ Las cinco capacidades
| | Capacidad | Qué asegura | Quién la da |
|---|-----------|-------------|-------------|
| 👑 | **Master Data Management (MDM)** | Un registro **autoritativo** por entidad | Data 360 (*identity resolution*) · **Informatica MCP** para mastering y deduplicación de toda la empresa |
| ✅ | **Data Quality** | Datos completos, exactos y frescos | **Informatica MCP** (calidad, *lineage*, higiene desde IDMC) |
| 🔗 | **Data Integration and Federation** | Llegar a los datos donde estén | Data 360 con **zero-copy** a warehouses y hyperscalers (AWS, Azure, Google Cloud) · **MuleSoft MCP** expone APIs existentes como herramientas MCP |
| 🛡️ | **Governance** | Quién ve qué y reglas de cumplimiento | Plataforma: **FLS, sharing, RBAC** · Data 360: etiquetado automático y **enmascarado dinámico** |
| 📇 | **Data Catalog** | Índice para **descubrir y leer** los activos antes de actuar | **Headless 360 MCP**, con sus herramientas **Discover** y **Describe** |

> ⚠️ Ojo de examen: el gobierno **nunca es automático**: hay que configurarlo. Un servicio sin gobierno configurado opera con **acceso sin gobierno** y expone campos sensibles **sin redactar**.

## 🏛️ Los tres pilares
1. 🧼 **Metadata and Context Grounding**: [[🧼 Metadata como capa de grounding]]
2. ☁️ **Data 360**, el *system of context*: [[☁️ Data 360 para agentes]]
3. 🪐 **Cross-Cloud MCPs**: [[🪐 Cross-cloud MCP servers]]

## 🎬 Los tres pilares en una sola pregunta
> 🗣️ "¿Por qué bajó el uso de esta cuenta el mes pasado y está en riesgo?"

```text
1️⃣ Headless 360 MCP  ─► Discover + Describe sobre Account y Opportunity (campos y permisos)
2️⃣ Data 360          ─► perfil unificado por zero-copy: pagos (warehouse) + casos (CRM) + contrato (sistema externo)
3️⃣ Tableau MCP       ─► métrica governed "usage trend", con el cálculo oficial del negocio
   Informatica MCP   ─► si ve contactos viejos, revisa las banderas de calidad antes de responder
```

Antes de conectar nada: [[🛫 Checklist antes de conectar herramientas headless]]. Herramientas: [[🧳 Headless Toolkit]].

## 🔁 Repaso #flashcards
¿Cuáles son las 5 capacidades de una data foundation?::Master Data Management, Data Quality, Data Integration and Federation, Governance y Data Catalog.
¿Cuáles son los 3 pilares de la data foundation para headless?::Metadata and Context Grounding, Data 360 y Cross-Cloud MCPs.
¿Qué da la capacidad de Data Catalog en headless?::El Headless 360 MCP server, con sus herramientas Discover y Describe.
¿Qué MCP server extiende MDM y calidad de datos más allá de Salesforce?::Informatica MCP Server, conectado a IDMC.
¿Qué MCP server expone APIs e integraciones existentes como herramientas MCP?::MuleSoft MCP Server.
¿El gobierno de datos se activa solo en headless?::No. Hay que configurarlo; sin él, el servicio expone campos sensibles sin redactar.
¿Qué gobierno aporta la plataforma y cuál Data 360?::Plataforma: FLS, sharing rules y RBAC. Data 360: etiquetado automático y enmascarado dinámico.
¿Qué pasa si un modelo apunta a tablas crudas sin data foundation?::Flujos inconsistentes por usuario, la IA decide lo que deberían decidir las reglas de negocio y se pierde el gobierno.
