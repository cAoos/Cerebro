---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-04
---
# 🎯 Red-teaming de IA

Un **red team** es un grupo de expertos (normalmente de **seguridad y ética de IA**) que intenta entrar a los sistemas de una organización para encontrar y arreglar problemas de seguridad y **salidas o resultados indeseados**.

> **Red-teaming**: proceso estructurado para sondear sistemas de IA e identificar capacidades dañinas, salidas peligrosas o amenazas de infraestructura.

## 🧪 Claves para probar
1. **Entender qué daños** quieres probar: objetivos alineados al negocio y al caso de uso.
2. **Armar el equipo**: expertos **internos y externos** con pensamiento adversarial.
3. **Probar periódicamente**: la tecnología y los ataques evolucionan.

## 🧑‍🔬 Manual vs. automatizado
| Tipo | Qué aporta |
|---|---|
| 🧠 **Manual** | Creatividad y experiencia humana para **ataques complejos** que lo automático no ve; se adapta al entorno y al objetivo |
| ⚙️ **Automated** | Scripts y herramientas que **simulan muchos ataques en poco tiempo** y exploran la **superficie de riesgo**. Es un **complemento, no un reemplazo** del humano |

Salesforce usa **ambos**. Prueba **mal uso**, **ataques de integridad intencionales** (como **prompt injection**) y **mal uso accidental**, enfocado en **toxicidad, sesgo y seguridad**. Suma **pruebas de penetración** con expertos internos y externos.

## 📊 Model benchmarking
Comparar los modelos con estándares de la industria. Salesforce publicó los **primeros LLM Benchmarks for CRM**.

Para tu organización: definir **principios propios** de IA responsable (inspirados en los de [[🌟 IA agéntica confiable]]) y considerar las leyes de tu industria. Ver también [[🔒 Estándares de seguridad para agentes]] y [[🧱 Defensa del prompt]].

> ⚠️ Ojo de examen: el red-teaming **automatizado complementa, no reemplaza** al manual. Salesforce prueba **toxicidad, sesgo y seguridad**, incluyendo **prompt injection**. Publicó el **LLM Benchmark for CRM**.

## 🔁 Repaso #flashcards
¿Qué es el red-teaming de IA?::Un proceso estructurado para sondear sistemas de IA e identificar capacidades dañinas, salidas peligrosas o amenazas de infraestructura.
¿Qué tres claves se mencionan para una estrategia de pruebas de IA?::Entender qué daños probar, armar el equipo (interno y externo) y probar periódicamente.
¿El red-teaming automatizado reemplaza al manual?::No, es un complemento; el manual encuentra ataques complejos que lo automático no ve.
¿Qué ventaja tiene el red-teaming manual?::La creatividad y experiencia humana para crear ataques complejos y adaptarlos al entorno.
¿Para qué tres cosas hace Salesforce red-teaming de IA?::Toxicidad, sesgo y seguridad.
¿Qué benchmark publicó Salesforce?::Los primeros LLM Benchmarks for CRM.
