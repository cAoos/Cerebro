---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-10-31
---
# 🔏 Estrategia de confianza de un proyecto de IA

El **plan para mitigar los riesgos a la confianza**: proteger datos sensibles, cumplir la regulación y cuidar la reputación. Es el nivel proyecto de la [[⚖️ Gobernanza de IA]].

## 1️⃣ Perfil de riesgo
Dice **qué riesgos priorizar**: tipo y nivel, **probabilidad** de efectos negativos y nivel de **disrupción o costo**. Se responde en **tres áreas**:

| Área | Qué es | Pregunta clave |
|---|---|---|
| 💧 **Fuga de datos** | Exposición accidental de info segura: ciberataques, acceso no autorizado, mandar datos sensibles (**PII**) a modelos externos | ¿Dónde se puede fugar? ¿Qué datos sensibles usas? |
| 📜 **Requisitos regulatorios** | Leyes de tu jurisdicción e industria (ej: **GDPR** en la UE). Apoyo del equipo **legal** | ¿Qué regulaciones aplican? |
| 📉 **Daño a la reputación** | La IA es **la voz de la empresa**: puede generar respuestas dañinas o falsas por **toxicidad** de datos o ataques | ¿Qué pasa si responde mal? |

Coral Cloud calificó cada área de 1 a 5 y priorizó: **regulatorio → reputación → fuga de datos**.

## 2️⃣ Guardrails
Mecanismos para que la IA opere **legal y éticamente**:

| Tipo | Protege de | Herramientas |
|---|---|---|
| 🔧 **Técnicos** | Incumplir leyes, exponer datos privados | **Secure data retrieval** (solo lo que el usuario puede ver) · **data masking** (placeholders antes del modelo externo) · **zero data retention** |
| 🔐 **Seguridad** | Ataques: **prompt injection**, **jailbreaking** | Defensa del prompt |
| 🤝 **Éticos** | **Toxicidad** (contenido HAP: hateful, abusive, profane) y **sesgo** (estereotipos) | **Detección de toxicidad** y revisión |

## 3️⃣ En Salesforce: Einstein Trust Layer
Todo lo que usa Einstein Generative AI (ej: Prompt Builder) **pasa automáticamente** por el [[🛡️ Einstein Trust Layer]].

![[proyecto-ia-trust-layer.png]]

| Riesgo | Estrategia | Función del Trust Layer |
|---|---|---|
| 💧 Fuga de datos | Usuarios sin acceso no ven reservas; nombres, contacto y tarjetas enmascarados | Secure data retrieval y [[📥 Grounding dinámico\|grounding]] · data masking |
| 📉 Reputación | Políticas de sistema contra prompts inesperados | [[🧱 Defensa del prompt]] |

🔄 **No es de una sola vez**: monitorear y auditar siempre, revisar **puntajes de toxicidad** y feedback.

> ⚠️ Ojo de examen: tres áreas de riesgo = **fuga de datos, regulatorio, reputación**. Tres tipos de guardrails = **técnicos** (masking, secure retrieval, zero retention), **seguridad** (prompt injection, jailbreak), **éticos** (toxicidad, sesgo). Un humano que dispara el proceso (**human-in-the-loop**) puede ser punto de fuga.

## 🔁 Repaso #flashcards
¿Qué es una estrategia de confianza de un proyecto de IA?::El plan para mitigar riesgos a la confianza: datos sensibles, regulación y reputación.
¿Qué contiene un perfil de riesgo?::Tipo y nivel de riesgos, probabilidad de efectos negativos y nivel de disrupción o costo; dice qué priorizar.
¿Cuáles son las tres áreas de riesgo de un proyecto de IA?::Fuga de datos, requisitos regulatorios y daño a la reputación.
¿Cuáles son los tres tipos de guardrails de IA?::Técnicos, de seguridad y éticos.
¿Qué es secure data retrieval?::Que la IA solo accede a los datos que el usuario que la ejecuta tiene permiso de ver.
¿De qué protegen los guardrails de seguridad?::De ataques como prompt injection y jailbreaking.
¿Qué significa HAP en toxicidad?::Hateful, abusive and profane: contenido de odio, abusivo y profano.
