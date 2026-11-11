---
tipo: nota
tema: prompts
estado: nueva
debil: false
fuente: "[[Trailhead - Become an Agentblazer Champion 2026]]"
creada: 2026-10-27
---
# 🧩 Plantilla Flex

La plantilla más flexible: **no trae entradas predefinidas**. Las **defines tú** al crearla, hasta **5 entradas**, cada una de un objeto.

## 🧪 Ejemplo: descripción de producto
| Recurso | API Name | Objeto |
|---------|----------|--------|
| Account Info | `Account_Info` | Account |
| Asset Info | `Asset_Info` | Asset |
| Contact Info | `Contact_Info` | Contact |

```text
Write a detailed product description using this information:
The Account Name is {!$Input:Account_Info.Name}
The Product Info is {!$Input:Asset_Info.Description}
The Contact Info is {!$Input:Contact_Info.Name}
```

Al no tener punto de entrada fijo, se invoca desde **Apex, Flow, REST API o Agentforce**. Para meter **varios registros** se usa un [[🌊 Template-Triggered Prompt Flow]]. Paso a paso: [[🛠️ Crear una plantilla Flex paso a paso]].

Los recursos se usan igual que en [[🔗 Grounding de plantillas]]. Uno de los [[🧾 Tipos de plantillas de Prompt Builder]].

## 🔁 Repaso #flashcards
¿Cuántas entradas admite una plantilla Flex?::Hasta 5.
¿Qué diferencia a Flex de los otros tipos de plantilla?::No predefine entradas; las defines al crearla.
