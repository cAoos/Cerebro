---
tipo: nota
tema: apex-fundamentos
estado: nueva
debil: false
fuente: "[[Trailhead - Apex Basics for Admins]]"
creada: 2026-10-12
---
# 🔤 Tipos de datos en Apex

Apex es **fuertemente tipado** 🔒: cada vez que se crea una [[📦 Variables en Apex|variable]] hay que definir su tipo de dato.

## 📋 Tipos comunes
| Tipo | Qué guarda | Ejemplo |
|------|-----------|---------|
| 🔢 `Integer` | Número entero, positivo o negativo, sin decimales | `Integer num = 12;` |
| 💲 `Decimal` | Número con decimales | `Decimal num = 12.22222;` |
| 🔤 `String` | Texto entre comillas simples, de una letra a frases enteras | `String whatAmI = 'A String';` |
| ✅ `Boolean` | `true` o `false`. En Apex también puede ser `null`. Se usa mucho con checkboxes | `Boolean doSomething = false;` |
| 🆔 `Id` | Id de un registro de Salesforce (18 caracteres) | `Id contactId = '00300000003T2PGAA0';` |

> ⚠️ Ojo de examen: un `Boolean` en Apex **puede ser `null`**, no solo `true` o `false`.

## 🔁 Repaso #flashcards
¿Qué significa que Apex sea fuertemente tipado?::Que toda variable debe declarar su tipo de dato al crearse.
¿Qué tres valores puede tener un Boolean en Apex?::`true`, `false` y `null`.
