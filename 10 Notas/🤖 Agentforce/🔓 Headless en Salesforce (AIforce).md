---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 🔓 Headless en Salesforce (AIforce)

Hace que **la data, la lógica y el gobierno de Salesforce sean accesibles desde cualquier sitio**. Los desarrolladores construyen desde donde trabajan y los usuarios hacen las cosas **sin entrar a Salesforce**.

> *"One platform. Anywhere humans and agents work."* Esa es la promesa de AIforce.

- 🔌 **Headless** = desacoplar la inteligencia del backend (datos, lógica y APIs) de cualquier **UI o pantalla fija**.
- 🏗️ **AIforce no es un producto nuevo**: es un **cambio de arquitectura** que abre la plataforma a cualquier agente, cualquier IDE y cualquier superficie, como **servicio gestionado** sobre estándares abiertos y con la [[🛡️ Einstein Trust Layer]] en cada acción.
- ➕ Es un **"y", no un "o"**: Lightning Experience **no desaparece**. Headless amplía dónde se usan las capacidades de Salesforce.

## 3️⃣ Las tres cosas que hay que saber
| | Capacidad | Cómo |
|---|-----------|------|
| 💻 | **Construir con cualquier coding agent o IDE** | +60 herramientas [[🔌 MCP en Salesforce\|MCP]] y +30 [[🛠️ ADLC Skills]] |
| ⚛️ | **Construir con cualquier framework de UI** | **Salesforce Multi-Framework**: React y otros, dentro de un entorno gobernado. Los componentes React se pueden poner en páginas de Lightning App Builder, junto a los LWC |
| 📱 | **Desplegar en cualquier superficie** | **Headless Experience Layer (HXL)**: separa la lógica del lugar donde se muestra. Se define la intención una vez y se pinta nativa en Slack, web, WhatsApp, voz… |

## 🧪 Ejemplo
La plataforma de viajes **Engine** construye su lógica de **cambio de reservas una sola vez**. El mismo agente aparece nativo en **Slack** para el equipo de soporte y como **componente web** para los viajeros, sin reescribir código por canal.

> [!note]- 📖 Glosario rápido
> - **API**: conectores que dejan a apps, agentes y herramientas externas pedir datos, disparar procesos o actuar sin abrir la UI.
> - **Salesforce CLI**: herramienta de terminal para crear, desplegar y gestionar componentes sin navegador.
> - **IDE**: donde se escribe, prueba y despliega código: Agentforce Vibes, VS Code, Cursor, Windsurf.
> - **Salesforce Metadata Catalog**: índice estructurado de todo lo que hay en la org (objetos, campos, relaciones, procesos, permisos) en un formato que los agentes entienden.

> ⚠️ Ojo de examen: si preguntan qué permite **definir la experiencia una vez y mostrarla en cualquier canal** → **HXL**. Si preguntan si headless **reemplaza** Lightning → **no**, lo amplía.

Contexto: [[🏛️ Capas de la plataforma agéntica]] · [[🧗 Retos para escalar la IA]].

> 🧳 Lo hace posible el [[🧳 Headless Toolkit]]: MCP, APIs, CLI y Skills, usados desde Claude, Cursor, ChatGPT, Agentforce Vibes o Slack.

> 🧲 Por qué conviene (Adoption, Reach, Speed, AI agent strategy): [[🧲 Pilares de valor de headless]]. Quién construye: [[🧑‍💻 Coding agents en Salesforce]].

## 🔁 Repaso #flashcards
¿Qué significa headless en Salesforce?::Desacoplar los datos, la lógica y las APIs de Salesforce de cualquier UI fija, para usarlos desde cualquier lugar.
¿Qué es AIforce?::No es un producto: es un cambio de arquitectura que abre la plataforma a cualquier agente, IDE y superficie, como servicio gestionado con la Trust Layer.
¿Qué hace la Headless Experience Layer (HXL)?::Separa la lógica y los datos de la pantalla: se define la intención una vez y se muestra nativa en cualquier superficie.
¿Headless reemplaza a Lightning Experience?::No, es un "y" y no un "o": amplía dónde se usa Salesforce.
¿Qué es Salesforce Multi-Framework?::Permite construir apps y agentes con frameworks estándar como React dentro de un entorno gobernado.
¿Headless requiere entrar a la org de Salesforce?::No: se usa todo Salesforce sin iniciar sesión en la org, desde las superficies donde ya trabajas.
