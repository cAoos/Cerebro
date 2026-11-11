---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 🧭 Herramientas del Headless 360 MCP

Para ser rápido, el **Headless 360 MCP server** no expone miles de funciones del CRM: presenta **solo 4 herramientas estables** al agente.

| | Herramienta | Qué hace |
|---|-------------|----------|
| 🔎 | **Discover** | **Búsqueda semántica** sobre un índice vectorial de skills para encontrar la acción candidata |
| 📄 | **Describe** | Revisa el **contrato técnico**: parámetros y pasos ordenados de la skill |
| 🚀 | **Dispatch** | **Invoca** la skill, enruta al endpoint y **aplica los controles de acceso** del usuario |
| 👁️ | **Dispatch Read Only** | Ejecuta acciones de **solo lectura** de forma segura |

```text
🗣️ "Prepárame la llamada con Acme" ─► 🔎 Discover (¿qué skill?) ─► 📄 Describe (¿qué parámetros?) ─► 🚀 Dispatch (ejecuta con mis permisos)
```

> 💡 Es el mismo ciclo que haría una persona: **buscar** la herramienta, **leer** cómo se usa y **usarla**. Discover usa [[🔎 Búsqueda semántica]].

> ⚠️ Ojo de examen: los controles de acceso se aplican en **Dispatch**. Separar **Dispatch Read Only** sigue el [[🔑 Mínimo privilegio en agentes|mínimo privilegio]].

Ver [[🔌 MCP en Salesforce]] · lo usa [[🤝 Sales Cloud en Claude]].

> 📈 **Superficie pequeña y estable**: las 4 herramientas no cambian, pero la **biblioteca de operaciones crece** con cada release. En la beta hay **decenas de operaciones**, sobre todo de **Setup para admins**: consultar, crear y actualizar registros, gestionar **usuarios y permission sets**, configurar **named credentials**. Tipos de servidor en [[🗄️ Tipos de MCP servers en Salesforce]].

> 🔀 **Otra lectura de Discover y Describe** (módulo *Data Foundation*): **Discover** lista los **objetos** de la org y **Describe** detalla los **campos** de uno (tipo, picklists, relaciones). Es la cara de *data catalog* de las mismas herramientas: ver [[🧼 Metadata como capa de grounding]].

## 🔁 Repaso #flashcards
¿Cuáles son las 4 herramientas del Headless 360 MCP server?::Discover, Describe, Dispatch y Dispatch Read Only.
¿Qué hace Discover?::Búsqueda semántica sobre un índice vectorial de skills para encontrar la acción correcta.
¿En qué herramienta se aplican los controles de acceso del usuario?::En Dispatch, que invoca la skill y enruta al endpoint.
¿Por qué el Headless 360 MCP expone solo 4 herramientas?::Para ser rápido y estable, en vez de exponer miles de funciones del CRM.
