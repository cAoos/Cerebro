---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 🧗 Retos para escalar la IA

Por qué los proyectos de IA se quedan en el piloto:

| | Reto | Qué pasa |
|---|------|----------|
| 🕳️ | **The Context Gap** | Los agentes no tienen acceso a datos **confiables y unificados**. Una base de datos solo guarda datos; Salesforce es **cómo funciona el negocio** |
| 🪤 | **The Do-It-Yourself Trap** | Para cerrar esa brecha se construyen integraciones y gateways **a la medida**, frágiles y caros de mantener |
| 🐢 | **Infrastructure Lag** | El piloto funciona en sandbox, pero IT o compliance no aprueban producción porque **no hay un camino gobernado y auditable** de la decisión del agente a la acción real |
| ⚖️ | **AI Governance** | Sin guardrails, controles de confianza y auditoría, no se puede desplegar a escala empresarial |

## 🧩 La respuesta: servicio gestionado frente a kit DIY
[[🔓 Headless en Salesforce (AIforce)|AIforce]] da un **servicio gestionado** sobre estándares abiertos ([[🔌 MCP en Salesforce|MCP]]), con la [[🛡️ Einstein Trust Layer]] aplicando seguridad en **cada acción**, en lugar de que cada empresa construya su propio puente.

> ⚠️ Ojo de examen: "funciona en la demo pero no está listo para producción" → **infrastructure lag**. "Construyen su propia integración y se rompe" → **DIY trap**.

> 💡 Apuntar un modelo de IA directo a **tablas crudas** crea procesos inconsistentes y sin gobierno. La lógica de negocio debe quedarse **dentro de Salesforce**, sobre [[☁️ Data 360 para agentes|Data 360]].

## 🔁 Repaso #flashcards
¿Cuáles son los 4 retos para escalar la IA?::Context gap, DIY trap, infrastructure lag y AI governance.
¿Qué es el infrastructure lag?::Cuando el piloto funciona pero no pasa a producción porque no hay un camino gobernado y auditable de la decisión del agente a la acción real.
¿Qué es la DIY trap?::Construir integraciones y gateways propios para conectar agentes con los sistemas: frágiles y caros de mantener.
