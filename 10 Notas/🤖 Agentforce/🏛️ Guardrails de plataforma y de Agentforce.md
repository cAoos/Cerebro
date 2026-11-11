---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# 🏛️ Guardrails de plataforma y de Agentforce

El equipo de producto y la **Office of Ethical and Humane Use (OEHU)** atacan los riesgos de la [[☢️ Riesgos de la IA agéntica|IA agéntica]] así: identificar los controles de un agente confiable, armar una estrategia de pruebas, añadir **guardrails éticos en el producto** y dar mejor guía ética a los clientes.

Hay **dos niveles** de guardrails:

## 🌐 1. Guardrails de plataforma (globales)
| Política | Qué cubre | Ejemplo |
|---|---|---|
| 📜 **Acceptable Use Policy (AUP)** | Reglas generales de uso de los servicios de Salesforce | No usar la plataforma para **spam o phishing** |
| 🤖 **AI Acceptable Use Policy (AI AUP)** | Reglas de uso de la **IA** de Salesforce | La IA **no puede tomar decisiones legales o importantes** sin que un **humano decida al final** |
| 📦 **Model Containment Policies** | Reglas operativas del uso de modelos | **Limitar qué datos** puede acceder un modelo para evitar fugas o mal uso |

## 🤖 2. Guardrails de Agentforce
Específicos de cada Cloud, producto y caso de uso, y alineados a leyes locales. Incluyen guardrails **éticos** (minimizar alucinaciones) y de **seguridad** (frenar ataques como **prompt injection**).

![[ia-agentica-confiable-guardrails-agentforce.png|400]]

- 🧑‍💼 **Agent Type**: cada tipo de agente trae sus propios ajustes. **Service Agent (ASA)** usa las instrucciones del topic para decidir **cuándo escalar a un humano**; el **SDR** tiene **reglas de engagement** del admin (cuándo trabajar un lead, cómo y cuándo mandar emails).
- 🗂️ **Topics** (hoy [[🗂️ Subagentes|subagentes]]): categoría de acciones para un trabajo; definen el **rango de capacidades** del agente. Hay una librería de topics estándar.
- 📝 **Topic instructions**: guían las decisiones; se redactan como **"Always…", "Never…", "If x, then y…", "As a first step…"** (ver [[📝 Instrucciones de razonamiento]]).
- ⚙️ **Actions**: lo que el agente hace; las de fábrica son **standard actions**.

### ✏️ Personalizar
Para más control: **modificar las instrucciones de un topic estándar** o **crear un topic custom**. Los controla el **admin** y normalmente los **aprueba el liderazgo** de la empresa, para que reflejen sus valores y cumplimiento.

### 🛡️ Y por debajo, la Trust Layer
[[🛡️ Einstein Trust Layer]]: **data grounding**, **zero data retention**, **toxicity detection** y **AI monitoring** (event logs).

## ✅ Buenas prácticas de implementación
| Práctica | Cómo |
|---|---|
| Entender las políticas | Lista de políticas por industria, geografía y caso de uso → define qué **topics** asignar |
| Seguridad robusta | **Acceso mínimo** del agente; reglas en topic instructions |
| Supervisión humana | Guías claras de **cuándo y cómo escalar**, escritas en topic instructions |
| Monitorear y auditar | Monitoreo continuo con el **Audit Trail** de la Trust Layer |
| Respetar la privacidad | Función de **opt-out** |
| Evaluaciones periódicas | Evaluar **sesgo, explicabilidad y robustez** |

Se parece a [[🚧 Guardrails para agentes autónomos]]. Los diseños estándar de producto están en [[🧩 Trust patterns de agentes]].

> ⚠️ Ojo de examen: **AUP** es general (spam/phishing), **AI AUP** es de IA (humano decide lo importante), **Model containment** limita datos del modelo. Para **personalizar guardrails** de Agentforce → **topic instructions** (editar estándar o crear custom). Los firma el **liderazgo**, los configura el **admin**.

## 🔁 Repaso #flashcards
¿Cuáles son los tres guardrails de plataforma de Salesforce?::Acceptable Use Policy (AUP), AI Acceptable Use Policy (AI AUP) y Model Containment Policies.
¿Qué guardrail de plataforma impide que la IA tome decisiones legales sin un humano?::La AI Acceptable Use Policy (AI AUP).
¿Qué hacen las Model Containment Policies?::Ponen límites operativos al uso de modelos, por ejemplo restringir qué datos puede acceder un modelo.
¿Cuáles son los tres componentes de los guardrails de Agentforce?::Agent type, topics y topic instructions, y actions.
¿Cómo se personalizan los guardrails de un agente de Agentforce?::Con topic instructions: modificando las de un topic estándar o creando un topic custom.
¿Qué guardrail propio tiene el agente SDR?::Reglas de engagement definidas por el admin: cuándo trabajar un lead y cómo y cuándo enviar emails.
¿Con qué frases suelen redactarse las topic instructions?::"Always…", "Never…", "If x, then y…", "As a first step…".
¿Qué cuatro funciones de la Trust Layer cita el módulo para agentes?::Data grounding, zero-data retention, toxicity detection y AI monitoring.
