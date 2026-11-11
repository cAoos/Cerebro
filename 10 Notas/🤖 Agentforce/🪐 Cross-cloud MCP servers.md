---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-07
---
# 🪐 Cross-cloud MCP servers

Los datos de la empresa no viven en una sola org: clientes en el CRM, transacciones en el warehouse, analítica en otro sistema. Los **cross-cloud MCP servers** conectan esos sistemas al entorno headless para que el agente tenga **la foto completa sin integraciones custom por cada fuente**. Son el **tercer pilar** de [[🪨 Data foundation para headless]].

| | Servidor | Conecta con | Le da al agente |
|---|----------|-------------|-----------------|
| ✅ | **Informatica MCP** | **IDMC** (Intelligent Data Management Cloud); el admin conecta una instancia existente | Calidad de datos, **deduplicación**, **lineage**, gobierno y **MDM**, sin reconstruir esas reglas en Salesforce |
| 🔗 | **MuleSoft MCP** | Integraciones, APIs y agentes existentes del stack | Traer datos externos **sin cambiar código**; las integraciones siguen donde están |
| 📊 | **Tableau MCP** | Analítica confiable y **capas semánticas gobernadas** | Razonar con **definiciones semánticas** (métricas, cálculos, lógica), no con datos crudos |

> ⚠️ Ojo de examen: para **calidad, deduplicación o lineage** → Informatica. Para **APIs existentes** → MuleSoft. Para una **métrica con el cálculo oficial** → Tableau.

> 💡 Son *hosted product* o *external* según [[🗄️ Tipos de MCP servers en Salesforce]]. Data 360 queda al centro de este portafolio: [[☁️ Data 360 para agentes]].

## 🔁 Repaso #flashcards
¿Cuáles son los 3 cross-cloud MCP servers de la data foundation?::Informatica, MuleSoft y Tableau.
¿Con qué se conecta el Informatica MCP Server?::Con una instancia existente de Informatica IDMC.
¿Qué aporta el Informatica MCP Server?::Calidad de datos, deduplicación, lineage, gobierno y MDM sin reconstruir reglas en Salesforce.
¿Qué aporta el MuleSoft MCP Server?::Acceso a integraciones y APIs existentes sin cambiar código.
¿Qué aporta el Tableau MCP Server?::Razonar sobre definiciones semánticas gobernadas (métricas, cálculos) en vez de datos crudos.
¿Para qué sirven los cross-cloud MCP servers?::Para dar al agente una foto completa de los datos de la empresa sin integraciones custom por fuente.
