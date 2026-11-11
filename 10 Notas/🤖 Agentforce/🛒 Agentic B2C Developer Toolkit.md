---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 🛒 Agentic B2C Developer Toolkit

**Problema:** los asistentes de código genéricos saben programar, pero **no conocen B2C Commerce**: usan APIs equivocadas, ignoran patrones de la plataforma y generan retrabajo.

**Solución:** una **cadena de herramientas unificada** para todas las tiendas B2C y todas las capas (frontend, backend, operaciones), con **4 componentes**:

![[b2c-toolkit-componentes.jpg]]

| | Componente | Rol |
|---|-----------|-----|
| ⌨️ | **CLI** | La **base**: comandos consistentes para desplegar cartridges, correr jobs y gestionar sandboxes |
| 📘 | **Agent Skills** | **Playbooks** que enseñan al coding agent cómo funciona B2C Commerce y qué comandos correr. Sirven en Claude Code, Cursor, Codex, Copilot, Agentforce Vibes, Windsurf |
| 🔌 | **MCP Server** | Herramientas para **actuar** en el entorno: desplegar, depurar en vivo, inspeccionar |
| 🧩 | **VS Code Extension** | Donde el dev **revisa, depura y aprueba** sin saltar a Business Manager |

> 💡 Para recordarlo: **Skills = saber** · **MCP = hacer** · **CLI = desplegar y registrar** · **VS Code = revisar y aprobar**.

## 🧪 Ejemplo
Un dev necesita una tienda **Storefront Next**. Describe lo que quiere; el agente usa las **Skills** para entender las APIs, escribe el código y con **MCP + CLI** despliega a un entorno **Managed Runtime**. El dev revisa en VS Code y aprueba: **el agente hace lo pesado y el dev mantiene el control**.

## 🎭 El mismo toolkit según el rol
- 🚨 **Operadores**: diagnosticar fallas de pedidos en producción con MCP y corregir con un comando de CLI.
- 🤖 **Desarrolladores**: investigar ataques de bots o problemas de rendimiento desde la terminal.
- 📊 **Merchandisers**: pedir reportes (promociones, más vendidos) a un asistente, sin Business Manager.

Parte de [[🔓 Headless en Salesforce (AIforce)]] · parecido a [[🛠️ ADLC Skills]].

## 🔁 Repaso #flashcards
¿Cuáles son los 4 componentes del Agentic B2C Developer Toolkit?::CLI, Agent Skills, MCP Server y VS Code Extension.
¿Qué hacen las Agent Skills del toolkit B2C?::Son playbooks que enseñan al coding agent cómo funciona B2C Commerce y qué comandos de CLI correr.
¿Qué rol cumple el MCP Server frente a las Agent Skills?::Las Skills dan el conocimiento; el MCP da las herramientas para actuar (desplegar, depurar, inspeccionar).
