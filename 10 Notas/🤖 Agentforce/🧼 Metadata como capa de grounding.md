---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-07
---
# 🧼 Metadata como capa de grounding

En el navegador, el layout, las etiquetas y los tooltips explican qué significa un valor como `STAT_3`. Un caller programático **no ve esa capa visual**: solo tiene la **metadata del schema**. Cada objeto y campo ya trae labels, descriptions, help text y relaciones: es el **grounding que la org trae de fábrica**. La pregunta es si está lo bastante cuidada para servir.

## 🔭 Cómo lee un agente la org
Al conectarse por el **Headless 360 MCP server**, el agente **no consulta datos ni actúa primero**: lee **la forma de la org**.

| | Herramienta | Devuelve |
|---|-------------|----------|
| 🔎 | **Discover** | Lista de objetos: API name, label y description |
| 📄 | **Describe** | Detalle de un objeto: por campo, API name, label, tipo, description, picklist values y relaciones |

> ⚠️ Ojo de examen: devuelven solo la metadata **visible para el usuario autenticado** (respetan permisos). **No** traen la lógica de validation rules, flows ni Apex: la metadata ayuda a interpretar, pero no reemplaza esas reglas.

## ⚖️ Metadata cuidada frente a descuidada
| El agente pregunta | ✅ Cuidada | ❌ Descuidada |
|---|---|---|
| ¿Qué representa este objeto? | "Contratos de servicio activos de cuentas enterprise, con fechas de renovación y nivel de SLA" | En blanco: solo ve el API name |
| ¿Qué significa este campo? | Label **Contract Renewal Date** + descripción de para qué se usa | Label **CRD_Auto**, sin descripción |
| ¿Qué valor de picklist elijo? | **Pending — Legacy Contract Review** | **PND_LGCY_2** |

Si la descripción está vacía, el servidor **devuelve el API name y nada más**: quien busque "revenue" no lo conecta con `Opp_Rev_Adj_Q3`. Con metadata incompleta el agente **infiere, pide aclaración o falla**, y la inferencia sin soporte causa **errores silenciosos**.

## 🧾 Auditoría antes de salir a producción
Empezar por los **objetos de más tráfico** e ir hacia afuera.

| Revisar | Buscar |
|---|---|
| Object labels | Claros y de negocio |
| Object descriptions | **Todo** objeto custom con descripción detallada |
| Field labels | Significativos, no abreviaturas de developer |
| Field descriptions | Sobre todo campos custom y picklists |
| Help text | Al día: el **help text viejo engaña activamente** al agente |
| Picklist values | Sin abreviaturas ni códigos legacy |

> 💡 Mismo principio que en [[🛰️ Enfoque API-first]]: Apex, flows y validation rules deben devolver **mensajes de error explícitos**, no excepciones genéricas, para que el agente pueda **recuperarse y reintentar**.

Parte de [[🪨 Data foundation para headless]] · herramientas en [[🧭 Herramientas del Headless 360 MCP]].

> 🧬 En el módulo de ventas la **metadata** incluye también validation rules, flows y el sales path: el agente valida si un cambio de etapa es posible. Ver [[🪟 Cuatro pilares técnicos de headless]].

## 🔁 Repaso #flashcards
¿Qué hace primero un agente al conectarse por el Headless 360 MCP server?::Lee la forma de la org con Discover y Describe, antes de consultar datos o actuar.
¿Qué devuelve Discover?::La lista de objetos de la org con su API name, label y description.
¿Qué devuelve Describe?::El detalle de un objeto: por campo, API name, label, tipo, description, picklist values y relaciones.
¿Discover y Describe devuelven validation rules, flows o Apex?::No. Solo la metadata del schema visible para el usuario autenticado.
¿Qué devuelve el servidor si un campo no tiene descripción?::Solo el API name.
¿Por qué el help text desactualizado es peor que no tenerlo?::Porque engaña activamente al agente al razonar.
¿Cómo deben nombrarse los picklist values para agentes?::Con nombres explícitos (Pending — Legacy Contract Review), no códigos legacy (PND_LGCY_2).
¿Por dónde empezar la auditoría de metadata?::Por los objetos de más tráfico, e ir hacia afuera.
¿Qué pasa cuando la metadata está incompleta?::El agente infiere, pide aclaración o falla; inferir sin soporte causa errores silenciosos.
