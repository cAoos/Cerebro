---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-28
---
# 🔁 Ciclo de vida de un agente (ADLC)

**ADLC = Agent Development Lifecycle.** [[🔓 Headless en Salesforce (AIforce)|AIforce]] lo cubre de punta a punta:

```text
🎨 Design ─► 🏗️ Build ─► 🧪 Test & evaluate ─► 🚀 Deploy ─► 👀 Observe
    ▲                                                          │
    └──────────────────── optimizar ◄──────────────────────────┘
```

| Fase | Qué se hace |
|------|-------------|
| 🎨 **Design** | Definir comportamiento, **subagents** (antes *topics*) y **guardrails** en lenguaje natural |
| 🏗️ **Build** | Usar [[🛠️ ADLC Skills]] y [[🔌 MCP en Salesforce\|MCP servers]] desde cualquier IDE (Vibes, Claude Code, Cursor…) |
| 🧪 **Test & evaluate** | Validar el comportamiento con **skills de prueba** prediseñadas |
| 🚀 **Deploy** | Publicar en cualquier superficie (Slack, Teams, móvil, portal) **en un clic vía HXL** |
| 👀 **Observe** | Monitorear desempeño, **auditar decisiones** y optimizar continuamente |

> ⚠️ Ojo de examen: el orden de las fases. Los guardrails se definen en **Design** (ver [[🚧 Guardrails para agentes autónomos]]) y la auditoría de decisiones es parte de **Observe**.

> 💡 En el módulo de despliegue la primera fase se llama **Plan**: Plan → Build → Test → Deploy → Observe. El detalle de Deploy está en [[🚀 Estrategia de despliegue de un agente]].

## 🔁 Repaso #flashcards
¿Cuáles son las 5 fases del ADLC?::Design, Build, Test & evaluate, Deploy, Observe.
¿En qué fase del ADLC se definen subagents y guardrails?::En Design, en lenguaje natural.
¿Con qué se despliega un agente en cualquier superficie en un clic?::Con la Headless Experience Layer (HXL).
