---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-06
---
# 🎙️ Agentforce Voice

Conversaciones **por voz** entre clientes y agentes de IA, con **transcripción en tiempo real**, recomendaciones de IA e integración con telefonía. Funciona así: **voz → texto → identificar la intención → generar la respuesta → texto → audio**.

**Dos formas de integrarlo:**
- 📞 **Salesforce Voice** (telefonía nativa)
- 🔗 **Proveedores de telefonía de partners**: por **SIP**, **PSTN** (red telefónica pública tradicional) o **dynamic routing**

Arquitecturas, patrones AI-first vs IVR y voz en Enhanced Chat v2: [[☎️ Arquitectura de telefonía de Agentforce Voice]] · Guardrails y zero data retention: [[🔈 Guardrails de Agentforce Voice]] · Paso a paso completo (agente → flow → canal): [[🛠️ Crear un agente de voz paso a paso]].

## 🪜 Configuración (caso PSTN)
1. **Conexión de voz**: Builder → **+ Connections → Add Connection → Telephony → Add to Agent**.
2. **Persona de voz**: Explorer → *Agent Definition Settings* → **Voice Settings**.
   - **Basic**: elegir una **persona** (género, idioma, estilo, edad, acento) y escucharla con **Play**.
   - **Advanced**: ajustar **speed**, **similarity** (qué tanto se parece al estilo base) y **stability** (variación frente a monotonía).
   - Opcional: **diccionario de pronunciación**, para decir palabras exactas.
   - Opcional: **key terms**, para reconocer marcas o jerga. **Con moderación**, solo si el agente no las reconoce. En la pantalla aparece como **Keyword Boosting**.
   - El diccionario pide palabra, pronunciación y tipo (por ejemplo **IPA**); se puede usar un LLM para generar la ortografía fonética y probarla con Play.
   - **Save → Commit Version → Activate.** Sin activar **no se puede configurar el inbound routing**.
3. **Flows de Omni-Channel**: son el **cerebro de enrutamiento** de Salesforce Voice. **Inbound** manda la llamada al agente y **outbound** la escala a un rep. Mismo patrón que en [[🔀 Enrutamiento Omni-Channel de un agente]] (ver también [[🧑‍⚖️ Cómo decide Omni-Channel a quién asignar]]).
4. **Canal PSTN**: Setup → **Agentforce Voice Setup →** pestaña **PSTN** (la otra es *SIP / Dynamic Routing*):
   - **New Number** → país, tipo y código de área → queda **en aprovisionamiento** (llega un email). Estará listo cuando su estado sea **Live**.
   - **New Channel** → protocolo **Phone number**, el número (solo los **Live**, y **cada número va a un solo canal**) y el **inbound flow** en *Call Routing* → **Save → Activate**.
   - Probar **llamando** al número.

![[voice-persona.jpg|450]]
![[voz-ajustes-avanzados.png]]
![[voice-canales-pstn.jpg|450]]

Resultado: atención telefónica **24/7**. Ver [[🔌 Conexiones y canales de un agente]].

> ⚠️ Ojo de examen:
> - Para que el agente hable por teléfono se agrega la conexión **Telephony**.
> - La voz se configura en **Voice Settings**: persona, speed, similarity, stability, diccionario de pronunciación y key terms (**con moderación**).
> - Un número solo sirve si está **Live** y va a **un solo canal**.
> - Las opciones de integración son **PSTN, SIP o dynamic routing**.
> - Agentforce Voice **no** está disponible en Trailhead Playground.

## 🔁 Repaso #flashcards
¿Cómo funciona Agentforce Voice?::Convierte voz a texto, identifica la intención, genera la respuesta y la convierte de nuevo a audio.
¿Qué dos enfoques de integración soporta Agentforce Voice?::Salesforce Voice (telefonía nativa) y proveedores de partners vía SIP, PSTN o dynamic routing.
¿Qué conexión se agrega al agente para habilitar voz?::Telephony.
¿Qué parámetros avanzados de la persona de voz se pueden ajustar?::Speed, similarity y stability.
¿Para qué sirven los key terms en Voice Settings y cómo se usan?::Mejoran el reconocimiento de marcas o jerga; usarlos con moderación, solo si el agente no las reconoce.
¿Cuándo se puede usar un número procurado en un canal de voz PSTN?::Cuando su estado es Live; y cada número solo puede ir a un canal.
¿Qué hay que hacer con el agente antes de configurar el inbound routing de voz?::Commit Version y Activate.
¿Cómo se llama en la pantalla de Voice Settings la opción de key terms?::Keyword Boosting; agregar términos con moderación.
