---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-29
---
# 🗂️ Subagentes

**Antes llamados *topics* (temas).** Son **categorías de acciones** que definen los trabajos o funciones que puede desempeñar un agente.

- 🧺 Cada subagente agrupa las [[⚡ Acciones de agente|acciones]] de un mismo trabajo.
- 📝 Lleva **instrucciones** que le dicen al agente **cómo decidir y qué debe o no debe hacer**. Al definirlos hay que poner **límites y contexto claros**: funcionan como **protecciones** (guardrails).
- 🧠 Cuando llega una pregunta, el agente **selecciona el subagente adecuado** e inicia sus acciones. Así se centra en las tareas y los datos relevantes. Lo hace el [[🌍 Atlas Reasoning Engine]] (ver [[🛤️ Ruta de un mensaje en Atlas]]).

## 🧪 Ejemplo
Subagente **Gestión de pedidos**:
- ⚡ Obtener pedidos por Id. de pedido
- ⚡ Obtener pedidos por correo electrónico
- ⚡ Buscar el estado de devolución
- ⚡ Crear etiqueta de devolución

```text
🤖 Agente
 ├─ 🗂️ Gestión de pedidos ─► ⚡ Pedido por Id · ⚡ Pedido por email · ⚡ Estado devolución · ⚡ Etiqueta
 └─ 🗂️ Gestión de envíos ──► ⚡ Revisar inventario · ⚡ Opciones de envío · ⚡ Confirmar fecha
```

![[subagente-order-management.jpg]]

## 📦 Estándar frente a personalizados
| | Qué son | Ejemplos |
|---|---------|----------|
| 📦 **Estándar** | Biblioteca de Salesforce, predefinidos con acciones frecuentes. Ideales para **implementar rápido**. Algunos requieren licencias de una nube | **CRM general** (identificar, resumir, actualizar registros, correos) · **Cerrar negociaciones** (recomendaciones a vendedores) · **Campañas de marketing** (briefs y campañas en Marketing Cloud) |
| 🛠️ **Personalizados** | Defines tú el subagente, sus acciones e instrucciones para tus procesos únicos | Cloud Kicks: **Gestión de envíos** → comprobar inventario de zapatillas azules, revisar envío y confirmar si llegan esta semana |

> ⚠️ Ojo de examen: **subagente = el trabajo** (qué y cuándo); **acción = la tarea** (cómo). Las **instrucciones del subagente** son guardrails contra alucinaciones. Si el examen dice *topic*, es lo mismo.

Componente de [[🤖 Agentforce]] · ver [[🚧 Guardrails para agentes autónomos]].

## 🔁 Repaso #flashcards
¿Qué es un subagente (antes topic)?::Una categoría de acciones que define un trabajo del agente, con instrucciones que dicen cómo decidir y qué hacer o no hacer.
¿Diferencia entre subagente y acción?::El subagente es el trabajo (agrupa acciones e instrucciones); la acción es una tarea concreta.
¿Cuándo usar subagentes estándar y cuándo personalizados?::Estándar para casos comunes e implementación rápida; personalizados para procesos únicos de la empresa.
¿Qué hace el subagente estándar CRM general?::Identifica, resume y actualiza registros, elabora correos, agrega datos y encuentra objetos de Salesforce.
