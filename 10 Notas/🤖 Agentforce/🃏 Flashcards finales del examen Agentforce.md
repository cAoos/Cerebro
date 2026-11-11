---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[2026-10 Agentforce Specialist]]"
creada: 2026-11-08
---
# 🃏 Flashcards finales del examen Agentforce

El mazo corto para los últimos dos días: lo que **más se pregunta** y las **trampas** típicas, ordenado por peso de sección. El detalle de cada tema está en su nota del [[MOC Agentforce]].

> ⚠️ Ojo de examen: los bancos de preguntas viejos (examen *AI Specialist*) usan nombres anteriores. Si una opción dice **Copilot**, **Topic** o **Data Cloud**, tradúcela antes de descartarla.

| Nombre viejo | Nombre actual |
|---|---|
| Einstein Copilot | Agentforce (Employee Agent) |
| Copilot Builder / Agent Builder | Agentforce Builder |
| Topic | Subagent |
| Copilot Action | Agent action |
| Planner service | Reasoning engine (Atlas) |
| Data Cloud | Data 360 |
| Einstein Bots | Reemplazados por Agentforce Service Agent |

## 🔁 Repaso #flashcards

### 🤖 AI Agents (35%)
¿Qué agrupa acciones e instrucciones de un trabajo y limita qué acciones considera el agente?::El subagente (antes topic).
¿Qué usa el reasoning engine para clasificar un mensaje en un subagente?::La descripción de clasificación del subagente.
¿Dónde se define qué puede y qué no puede hacer un subagente?::En su Scope.
¿Qué usa el agente para elegir entre dos acciones?::Las instrucciones (descripción) de cada acción.
¿Cuáles son los tipos de referencia de una acción custom?::Autolaunched flow, Apex @InvocableMethod y prompt template (además de APIs como MuleSoft o External Services).
¿Se puede usar un screen flow o un Apex trigger como acción de agente?::No.
¿Qué opción impide que una acción corra si falta un input?::Require Input to execute action.
¿Qué opción muestra el output de una acción al usuario?::Show in conversation.
¿Cómo se fuerza que una regla crítica se cumpla siempre?::Con lógica determinista: variables, filtros de acciones, instrucciones condicionales o Agent Script.
¿Qué hace un filtro de acción?::Oculta o muestra una acción según una condición sobre variables.
¿Qué hacen las instrucciones condicionales?::Cambian qué instrucciones recibe el agente según el valor de una variable.
¿Para qué sirve Agent Script?::Para combinar lógica determinista (condiciones, variables, transiciones) con razonamiento en lenguaje natural.
¿Con qué permisos corre un Employee Agent?::Con los del usuario que conversa con él.
¿Con qué permisos corre un Service Agent que atiende clientes?::Con los del usuario dedicado del agente (licencia Einstein Agent).
El agente no ve un campo custom: ¿qué revisas?::El FLS en el permission set del usuario del agente.
¿Qué pasa si activas una nueva versión de un flow que usan varios agentes?::Todos toman la nueva versión; para aislar el cambio, guárdalo como flow nuevo.
¿Se puede activar un draft de agente?::No: primero Commit Version y luego Activate.
¿Cuántas versiones de un agente pueden estar activas?::Una; activar otra desactiva la anterior.
¿Simulate frente a Live Test?::Simulate prueba la configuración sin acciones ni datos; Live Test ejecuta las acciones de verdad.
¿Dónde se ve por qué el agente eligió algo o qué paso es lento?::En el Trace del panel Preview (pasos y tiempo por subproceso).
¿Cómo escala un Service Agent a un humano?::Con un Omni-Channel flow (Route Work) hacia una cola humana, configurado en la conexión.
¿Qué piezas lleva un agente en el chat de un sitio web?::Messaging for In-App and Web (Enhanced Chat), Omni-Channel flow y un Embedded Service Deployment publicado.
¿Cómo ven los vendedores un Employee Agent?::Con Agent Access en un permission set asignado.
¿Qué agente atiende leads entrantes de alto volumen?::Agentforce SDR (Engagement agent).
¿Qué agente entrena vendedores con role-plays y feedback por etapa?::Agentforce Sales Coach.
¿Qué agente asiste al agente humano con un service plan en el Case?::Agentforce Service Assistant (asistivo, no ejecuta acciones).
¿Cuál es el camino más rápido a un agente para clientes con una sola fuente de conocimiento?::El setup guiado del Help Agent.
¿Qué ventaja tiene Agentforce sobre Einstein Bots?::Entiende la intención con un LLM y elige acciones sin guionar cada diálogo.
¿Cómo deben escribirse las instrucciones?::Imperativas o condicionales (If… Then / Never… Instead), con nombres exactos de acciones.
¿Las instrucciones viven por acción o por subagente?::Por subagente; si la acción está en varios, se repiten.
¿Qué ejecuta prompts y acciones en lote sobre muchos registros, como hoja de cálculo?::Agentforce Grid.
¿Canvas o Script View?::Canvas: bloques low-code (/ para if/else, @ para recursos). Script View: Agent Script crudo con validación. Editan el mismo agente.
¿Qué son las template expressions?::Expresiones como {!@variables.x} para usar valores, condiciones, transiciones y variables en Agent Script.
¿Qué es el razonamiento híbrido?::Lógica determinista que se cumple siempre más el razonamiento flexible del LLM.
¿Cuándo usar Agent API?::Para hablar con un agente desde una app propia, un sistema externo, una automatización headless u otro agente.
¿Cómo se autentica la Agent API?::External Client App con client credentials y un Run As user (mínimo API Only).
¿Qué conexiones tiene un Service Agent?::Telephony, Enhanced Chat, Messaging, Service Email y Marketing Email.
¿Qué conexiones tiene un Employee Agent?::Lightning Experience, Salesforce Mobile, Slack y Enhanced Web Chat.

### ✍️ Prompt Engineering (20%)
¿Qué plantilla llena un campo desde la página del registro?::Field Generation (requiere Dynamic Forms).
¿Qué plantilla genera un correo a un contacto?::Sales Email (se usa con Draft with AI).
¿Qué plantilla combina varias entradas libres de objetos sin relación?::Flex.
¿Qué permission set crea y edita plantillas?::Prompt Template Manager.
¿Qué permission set solo ejecuta plantillas?::Prompt Template User.
Un usuario no ve el ícono de IA de un campo y los demás sí: ¿qué falta?::Prompt Template User.
¿Cómo se vuelve reutilizable una plantilla con datos escritos a mano?::Con merge fields {!$Input:Objeto.Campo}.
¿Qué recurso agrega lógica compleja o varios registros a una plantilla?::Un Template-Triggered Prompt Flow (con Add Prompt Instructions).
¿Qué recursos de grounding acepta una plantilla?::Merge fields, flows, Apex, listas relacionadas y retrievers de Data 360.
¿Qué muestra el Resolved Prompt?::El prompt con los datos reemplazados: lo que realmente va al LLM.
¿Por qué está deshabilitado el Preview de una plantilla?::Falta elegir un registro o valores para sus entradas.
¿Por qué una plantilla falla al azar por límite de tokens?::Porque el volumen de datos de grounding cambia por registro.
¿Qué baja la variación entre ejecuciones?::Menor temperatura (configured model en Model Builder) y formato fijo.
¿Qué hiperparámetros se ajustan en Model Builder?::Temperatura, frequency penalty y presence penalty.
¿Cómo se usa un LLM propio con la Trust Layer?::BYOLLM en Model Builder de Einstein Studio.
¿Qué opción mantiene las solicitudes dentro de la infraestructura de Salesforce?::Modelos de terceros alojados en Salesforce.
¿Qué técnica asegura un formato de salida exacto?::Few-shot: dar ejemplos del formato.
¿Qué palabra acota la longitud de la respuesta?::"within" (within 50 words).
¿Qué reduce alucinaciones en un prompt?::Pedir que responda solo con el contexto y que diga cuando no lo sabe.
¿Qué hay que hacer para usar una plantilla en una acción o en la UI?::Guardarla y activarla.
¿Dónde se gestionan los modelos que pueden usar las plantillas?::En Model Builder (AI Models); el acceso se controla con permission sets.

### ☁️ Data 360 (20%)
¿Cuál es el orden de RAG en Data 360?::Ingerir no estructurados (UDLO → UDMO) → search index (chunks + embeddings) → retriever → plantilla o agente.
¿Cuándo usar hybrid search?::Cuando importan tanto el significado como términos exactos (códigos, SKU).
¿Cómo limitar qué documentos recupera un agente?::Con un custom retriever con filtros.
¿Por qué se fragmentan los documentos (chunking)?::Para traer solo lo relevante y caber en la ventana de contexto.
¿Qué crea la Agentforce Data Library por debajo?::La ingesta, el search index y el retriever (Knowledge o archivos).
¿Usar datos de Snowflake sin copiarlos?::Zero-copy federation.
¿Qué deciden las match rules y las reconciliation rules?::Match: quién es la misma persona. Reconciliation: qué valor gana.
¿Para qué se mapean DLO a DMO?::Para armonizar los datos en el modelo canónico.
¿Qué calcula métricas como LTV a nivel de perfil?::Calculated insights.
¿Qué separa datos por marca o región?::Data spaces.
¿Qué da una vista desnormalizada del perfil y sus relacionados para grounding en tiempo real?::Data graphs.
¿Qué reacciona a cambios en Data 360 con automatización?::Un Data Cloud-triggered flow.
¿Datos de un registro o un documento: cómo se aterriza cada uno?::Registro (estructurado): merge field o acción. Documento (no estructurado): RAG.
¿Qué rol tiene Data 360 en la plataforma agéntica?::System of context.

### 🧪 Testing y despliegue (10%)
¿Qué prueba cientos de frases en lote?::Agentforce Testing Center.
¿Qué define un caso de prueba de Testing Center?::La frase, el subagente, las acciones y la respuesta esperados.
¿Cómo se crean casos en Testing Center?::Con un CSV o generados con IA.
¿Por qué correr Testing Center en sandbox?::Porque ejecuta las acciones reales.
¿Cuál es el orden del ADLC?::Plan/Design → Build → Test → Deploy → Observe.
¿Qué no viaja en el paquete del agente?::El usuario del agente: se crea en destino.
¿Qué se revisa en la org destino antes de desplegar?::Licencias y que Einstein, Agentforce y Data 360 estén encendidos.
¿Qué se hace después de desplegar?::Activar el agente, asignar permission sets, revisar la versión activa de los flows y publicar el Embedded Service.
¿Qué es red-teaming?::Atacar a propósito al agente para encontrar fallas antes del lanzamiento.
¿Cómo evalúa Testing Center la respuesta?::Con un LLM como juez, por significado y no por texto exacto.
Falla el subagent assertion: ¿qué ajustas?::Las descripciones de clasificación.
¿Qué metadata es una plantilla de prompt?::GenAiPromptTemplate (change sets o CLI).
¿Qué revisas tras desplegar una plantilla?::Que existan sus dependencias (campos, flows, Apex, retrievers) y qué versión quedó activa.

### 🛡️ Gobierno y observabilidad (10%)
¿Qué impide que el proveedor del LLM guarde o entrene con los datos?::Zero data retention.
¿Qué reemplaza PII por marcadores antes del LLM?::Data masking (se desenmascara en la respuesta).
¿Qué reduce jailbreak y prompt injection?::Prompt defense.
¿Qué puntúa la respuesta en categorías dañinas?::Toxicity detection.
¿Qué paso respeta permisos, sharing y FLS antes del grounding?::Secure data retrieval.
¿Dónde se guarda el audit trail de IA generativa?::En Data 360.
¿Qué datos tiene el audit trail?::Prompt, datos enmascarados, respuesta, puntajes de toxicidad y feedback.
¿Qué detecta knowledge gaps y conversaciones sin resolver?::Agentforce Optimization (Observability).
¿Qué requieren varias herramientas de Observability?::Licencias de Data 360.
¿Qué casilla guarda conversaciones para revisar el comportamiento?::Enhanced Event Logs.

### 🔗 Multi-agente (5%)
¿Qué es A2A?::El traspaso directo de trabajo entre agentes, sin humano.
¿En qué se diferencia MCP de A2A?::MCP conecta un agente con herramientas y datos; A2A conecta agentes entre sí.
¿Dónde se registra un MCP server externo?::En el API Catalog.
¿Cuándo conviene multi-agente?::Con dominios distintos (dueños, datos, permisos), un agente sobrecargado o necesidad de escalar y controlar cada parte.
¿Herramienta externa, otro agente o llamada fija?::MCP, A2A y API, respectivamente.
¿Cómo se conecta una herramienta al Salesforce Hosted MCP Server?::Se activa en Setup y se usa una External Client App con scope mcp_api y OAuth con PKCE.

### 🧰 Funcionalidades Einstein que aparecen en bancos viejos
¿Qué sugiere respuestas de chat basadas en Knowledge?::Einstein Service Replies.
¿Qué resume una conversación de servicio al cerrarla?::Einstein Work Summaries.
¿Qué analiza llamadas de voz y video (competidores, palabras clave, próximos pasos)?::Einstein Conversation Insights.
¿Dónde se conectan modelos predictivos o LLM externos?::Model Builder en Einstein Studio.
Grounding de una plantilla: ¿merge field o flow/Apex?::Merge field si es el registro o su lista relacionada tal cual; flow (low-code) o Apex (lógica compleja) si hay que filtrar, ordenar o limitar (p. ej. "las 3 oportunidades más recientes").
Trust Layer: ¿enmascarado en agentes?::No; está desactivado para agentes de Agentforce, solo aplica a funciones generativas embebidas y plantillas.
Trust Layer: ¿dónde vive el audit trail y qué necesita?::En Data 360; requiere Data 360 aprovisionado y activar la recolección de audit y feedback.
Trust Layer: ¿qué aparece primero, la página de Trust Layer o Turn on Einstein?::Primero Turn on Einstein (IA generativa); luego aparece la Trust Layer en Setup.
