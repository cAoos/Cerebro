---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 🔌 MCP en Salesforce

**MCP (Model Context Protocol)** es el **estándar abierto** que deja que **cualquier agente de IA** llame herramientas de Salesforce.

- 🏢 **Platform-hosted MCP servers**: servidores **gestionados por Salesforce** que exponen sus APIs, datos y lógica como herramientas que cualquier agente puede llamar.
- 🔒 Cada acción por MCP pasa por la [[🛡️ Einstein Trust Layer]]: se respetan **FLS y sharing rules** (ver [[🚪 Open access, not open bypass]]).
- 🌐 Hay MCP **de Salesforce** y **de terceros (independientes)**.

## 🧰 Catálogo de MCP
| MCP | Para qué |
|-----|----------|
| 🎯 **Headless 360 MCP** (Beta) | **Una sola conexión** para usar Salesforce desde cualquier agente compatible con MCP. Expone 4 herramientas: [[🧭 Herramientas del Headless 360 MCP\|Discover · Describe · Dispatch]] |
| 📊 **Tableau MCP** | Analítica gobernada para cualquier agente |
| 🧼 **Informatica MCP** | Gestión de datos como herramientas: datos limpios y gobernados |
| ☁️ **Data 360 MCP** | Contexto en tiempo real: perfil unificado, eventos y segmentación |
| 🔗 **MuleSoft MCP** | Construir, desplegar y gobernar integraciones, agentes, APIs y MCP |
| #️⃣ **Slack MCP** | Leer y actuar sobre mensajes, canales y Canvases |
| 🛒 **Agentforce Commerce MCPs** | +60 herramientas de comercio: catálogo, precios locales, inventario, checkout |

## 🧪 Ejemplo
**Claude Code** se conecta a la org por los MCP servers de la plataforma, consulta objetos y campos, y crea un agente **sin entrar a Salesforce**. Si el usuario no tiene permiso sobre un campo, **el MCP tampoco lo deja verlo**.

> ⚠️ Ojo de examen: "¿cómo se conecta un agente externo a Salesforce con un **estándar abierto**?" → **MCP**. "¿Con una sola conexión?" → **Headless 360 MCP**.

Va de la mano con [[🛠️ ADLC Skills]] y [[🔓 Headless en Salesforce (AIforce)]].

> 🗄️ Tipos de servidor (standard, product, external, custom), activación y reglas: [[🗄️ Tipos de MCP servers en Salesforce]]. Se conecta con **OAuth**: se configura una vez y sirve a cualquier cliente compatible. Es una de las cuatro piezas del [[🧳 Headless Toolkit]].

## 🔁 Repaso #flashcards
¿Qué es MCP?::Model Context Protocol: el estándar abierto que deja que cualquier agente de IA llame herramientas de Salesforce.
¿Qué son los platform-hosted MCP servers?::Servidores gestionados por Salesforce que exponen sus APIs, datos y lógica como herramientas para cualquier agente.
¿Un agente que entra por MCP se salta los permisos?::No: pasa por la Trust Layer y se respetan FLS y sharing rules.
¿Qué MCP da una sola conexión a Salesforce para cualquier agente?::Headless 360 MCP (Beta).
