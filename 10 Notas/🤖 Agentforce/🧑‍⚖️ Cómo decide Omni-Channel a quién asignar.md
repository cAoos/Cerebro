---
tipo: nota
tema: agentforce
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Innovator 2026]]"
creada: 2026-11-06
---
# 🧑‍⚖️ Cómo decide Omni-Channel a quién asignar

Caso práctico que amplía [[🔀 Enrutamiento Omni-Channel de un agente]]: qué hace cada pieza y cómo **razona el sistema** al asignar y al escalar.

## 🧩 Las tres piezas
| Pieza | Pregunta que responde | Qué define |
|---|---|---|
| 📺 **Service Channel** | ¿**Qué tipo de trabajo** es? | Convierte registros de un objeto (Messaging Session, Case, VoiceCall…) en **work items** que Omni puede repartir |
| 👥 **Queue** | ¿**Dónde espera** y **quién puede** tomarlo? | La fila de trabajo y sus **miembros**, que son los reps candidatos |
| ⚖️ **Routing Configuration** | ¿**Cómo** se reparte? | **Prioridad** frente a otras colas, **modelo** de asignación y **tamaño** de cada item (cuánta capacidad consume) |

Hay dos piezas más que casi siempre entran en juego:
- **Presence Configuration**: la **capacidad total** de cada rep, por ejemplo 100%.
- **Presence Status**: el estado del rep, por ejemplo *Online – Chat*, y **qué service channels** puede recibir con ese estado.

```text
 Cliente escribe
       │
       ▼
 MessagingSession ──(Service Channel: "es trabajo de mensajería")
       │
       ▼
 Inbound flow ──Route Work──► 🤖 Agente de IA
                                  │ (pide humano / sentimiento negativo / fuera de alcance)
                                  ▼
                           Outbound flow ──Route Work──► 👥 Queue "Messaging"
                                                              │
                                    ⚖️ Routing Configuration decide a quién
                                                              │
                                                              ▼
                                                     🧑 Rep (push al sidebar)
```

## 🧪 Ejemplo: Northern Trail Outfitters

**La configuración**

| Pieza | Valor |
|---|---|
| Service Channel | *NTO Help Center*, sobre el objeto **Messaging Session** |
| Routing Configuration | *Messaging Routing*: prioridad **1**, modelo **Least Active**, cada chat ocupa **25%** |
| Queue | *Messaging*, que usa *Messaging Routing*, con miembros Ana, Beto, Carla y Dani |
| Presence Configuration | Cada rep tiene **100%**, o sea hasta 4 chats si solo atiende chats |

Además existe otra cola, *Casos*, con su propia routing configuration: prioridad **2**, cada caso ocupa **75%**.

**El estado en este momento**

| Rep | Estado | Canales de su status | Trabajo abierto | Capacidad usada | Libre |
|---|---|---|---|---|---|
| Ana | Online | Messaging + Case | 2 chats | 50% | 50% |
| Beto | Online | Messaging + Case | 1 caso | 75% | 25% |
| Carla | Online | **solo Case** | — | 0% | 100% |
| Dani | **Away** | — | — | — | — |

## 🧠 Cómo razona el sistema paso a paso

### 1️⃣ Asignación de entrada: la conversación llega al agente de IA
Sofía abre el chat en la web.
1. Se crea una **Messaging Session**. El service channel la marca como trabajo de mensajería.
2. Se dispara el **inbound flow**. Recibe la sesión y los datos del **pre-chat**, y busca si Sofía ya es un Contact.
3. La acción **Route Work** apunta al **agente de IA**. El agente no tiene límite de capacidad, así que toma la conversación de inmediato.
4. Si no se puede enrutar al agente, por ejemplo porque está inactivo, la sesión cae en la **fallback queue** *Messaging* y la reparte un humano según el paso 3️⃣.

### 2️⃣ El agente decide escalar
Sofía escribe: *"esto no me sirve, quiero hablar con una persona"*.
1. El **Escalation subagent** revisa sus instrucciones. Se cumple una condición: pidió un humano y además el sentimiento es negativo.
2. El agente envía el **mensaje de escalamiento**: *"Un momento, reviso si hay alguien disponible"*.
3. Llama a `@utils.escalate`, que dispara el **outbound flow** (ver [[🧾 Estructura de un Agent Script]]).
4. El flow revisa si hay reps disponibles en la cola. Como sí hay, actualiza la sesión y hace **Route Work → Queue Messaging**. **El historial viaja con la sesión.**

### 3️⃣ Omni elige al rep: aquí trabaja la routing configuration
Omni toma el item de 25% y filtra a los candidatos:

| Filtro | Ana | Beto | Carla | Dani |
|---|---|---|---|---|
| ¿Es miembro de la cola? | ✅ | ✅ | ✅ | ✅ |
| ¿Está Online? | ✅ | ✅ | ✅ | ❌ Away |
| ¿Su status incluye el canal **Messaging**? | ✅ | ✅ | ❌ solo Case | — |
| ¿Tiene ≥ 25% libre? | ✅ 50% | ✅ 25% | — | — |
| **¿Es candidata?** | ✅ | ✅ | ❌ | ❌ |

> 🚨 Carla tiene 100% libre y aun así **no recibe nada**, porque su presence status no incluye mensajería. Es el error de configuración más común.

Entre Ana y Beto, el resultado **depende del modelo de enrutamiento**:

| Modelo | Criterio | Ana | Beto | Gana |
|---|---|---|---|---|
| **Least Active** | El que tenga **menos items abiertos** | 2 items | 1 item | **Beto** |
| **Most Available** | El que tenga **más capacidad libre** | 50% | 25% | **Ana** |

Como la cola usa **Least Active**, el chat le llega a **Beto**, que queda en 100% y ya no le entra nada más.

Omni le hace **push** a Beto: le suena en el Omni-Channel sidebar.
- Si Beto **acepta**, ve todo lo que Sofía habló con la IA y sigue desde ahí. Sofía **no repite nada**.
- Si **rechaza** o se vence el *push timeout*, Omni lo reenruta al siguiente candidato, Ana.

### 4️⃣ Nadie tiene capacidad: el item espera en la cola
Supongamos que Ana y Beto están al 100%.
1. El chat se queda **en la cola**, sin asignar.
2. El orden de la cola es primero la **prioridad de la routing configuration** y después **la antigüedad**. Si al mismo tiempo esperan un chat (prioridad 1) y un caso (prioridad 2), el chat sale primero aunque el caso sea más viejo.
3. Cuando Ana cierra un chat, libera 25%. Omni vuelve a evaluar y le hace push del primer item que le quepa.

### 5️⃣ No hay nadie conectado: el escalamiento falla
Son las 3 a.m. y no hay ningún rep Online.
1. El outbound flow no encuentra reps disponibles, así que **el escalamiento falla**.
2. El agente **retoma la conversación** dentro del Escalation subagent, con todo el contexto previo.
3. Según sus instrucciones, le ofrece a Sofía **crear un caso**. Ese caso puede entrar después a la cola *Casos* con su propio service channel.
4. El escalamiento **se intenta una sola vez por sesión**. Si Sofía insiste, el agente no vuelve a disparar el flow.

Así se prueba en la práctica: [[💬 Desplegar un agente en Enhanced Web Chat]] (pruebas con y sin reps). El mismo patrón aplica a llamadas en [[🎙️ Agentforce Voice]]. Contexto general: [[🔌 Conexiones y canales de un agente]] y [[📞 Canales y escalamiento de un agente]].

> ⚠️ Ojo de examen:
> - **Un rep Online que no recibe nada** tiene un presence status sin ese service channel, o no tiene capacidad libre para el tamaño del item.
> - **Least Active** cuenta **items abiertos**; **Most Available** mira **capacidad libre**. Si los items tienen tamaños distintos, eligen reps distintos.
> - **Prioridad de la routing configuration:** decide qué cola se atiende primero cuando un rep pertenece a varias. **Un número más bajo es más prioritario.**
> - **Una queue sin routing configuration** guarda el trabajo, pero Omni no le hace push a nadie.
> - **Route Work** lo usan tanto el inbound como el outbound flow. Lo que cambia es el destino: el agente de IA o la cola.

## 🔁 Repaso #flashcards
¿Qué hace el Service Channel en Omni-Channel?::Convierte los registros de un objeto (Messaging Session, Case…) en work items que Omni puede repartir.
¿Qué define la Routing Configuration?::La prioridad frente a otras colas, el modelo de asignación (Least Active o Most Available) y el tamaño (capacidad) de cada item.
¿Qué papel cumple la Queue en Omni-Channel?::Es la fila donde espera el trabajo y define qué reps (miembros) son candidatos.
¿Qué define la Presence Configuration?::La capacidad total de cada rep.
¿Qué define un Presence Status?::El estado del rep y qué service channels puede recibir con ese estado.
¿Cuándo es candidato un rep para recibir un chat?::Es miembro de la cola, está Online, su presence status incluye el service channel y tiene capacidad libre suficiente.
Un rep está Online con 100% libre y no recibe chats. ¿Causa probable?::Su presence status no incluye el service channel de mensajería.
¿Qué diferencia hay entre Least Active y Most Available?::Least Active asigna al rep con menos items abiertos; Most Available, al de más capacidad libre.
Ana tiene 2 chats (50% libre) y Beto 1 caso (25% libre). Llega un chat de 25%. ¿A quién va con Least Active y con Most Available?::Least Active → Beto (menos items); Most Available → Ana (más capacidad libre).
¿Qué pasa si el rep rechaza el push o se vence el push timeout?::Omni reenruta el item al siguiente candidato.
¿En qué orden se atienden los items que esperan en cola?::Primero por la prioridad de la routing configuration (número más bajo primero) y luego por antigüedad.
¿Qué pasa si el agente escala y no hay reps Online?::El escalamiento falla, el agente retoma la conversación con el contexto y ofrece crear un caso; solo se intenta una vez por sesión.
