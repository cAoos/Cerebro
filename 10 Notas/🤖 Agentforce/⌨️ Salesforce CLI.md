---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-07
---
# ⌨️ Salesforce CLI

La **interfaz de línea de comandos principal** para trabajar con orgs de Salesforce desde **cualquier terminal o IDE**. Parte del [[🧳 Headless Toolkit]].

**Para qué:** crear orgs, **desplegar y recuperar metadata**, correr Apex, consultar datos, gestionar autenticación y **scriptear CI/CD**. Ver [[📦 Mover un agente a producción]].

- 🧱 Está construida sobre **oclif**, framework open source para CLIs en **Node.js**.
- 🤖 Se usa desde **Agentforce Vibes, Claude o Cursor**.
- 📦 El ejecutable se llama **`sf`** y viene con la **extensión Salesforce CLI**.

```bash
npm install --global @salesforce/cli   # instalar
sf --version                           # versión
sf --help                              # ayuda
sf commands                            # lista de comandos
sf org list                            # orgs conectadas
sf org list metadata-types --api-version 57.0 --target-org my-dev-org
```

> ⚠️ Ojo de examen: el ejecutable es **sf**, la CLI se basa en **oclif (Node.js)** y se instala con **npm install --global @salesforce/cli**. Sirve para **desplegar metadata y CI/CD**.

## 🔁 Repaso #flashcards
¿Para qué sirve Salesforce CLI?::Crear orgs, desplegar y recuperar metadata, correr Apex, consultar datos, gestionar autenticación y scriptear CI/CD.
¿Sobre qué framework está construida Salesforce CLI?::oclif, un framework open source para CLIs en Node.js.
¿Cómo se llama el ejecutable de Salesforce CLI?::sf.
¿Cómo se instala Salesforce CLI con npm?::npm install --global @salesforce/cli.
¿Qué comando lista las orgs conectadas?::sf org list.
