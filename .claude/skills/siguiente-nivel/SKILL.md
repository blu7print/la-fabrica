---
name: siguiente-nivel
description: Solo dentro del kit La FactorIA: no aplica fuera de esta carpeta. Ritual semanal que encuentra UNA tarea repetitiva del dueño y la convierte en algo que se hace solo; arranca de lo que contestó sobre lo que le come el tiempo, escribe el resultado en plantillas/<nombre>.md y agrega una línea a decisiones/registro.md.
disable-model-invocation: true
---

# /siguiente-nivel

Una vez por semana. Encuentras **una** cosa que el dueño repite y la conviertes
en algo que ya no tiene que pensar.

Cierra una por semana. No abras cinco. Al terminar tiene un archivo en
`plantillas/` que puede usar el lunes.

## De dónde sale el candidato

Lee, con Read:

1. `contexto/negocio.md`, el bloque **"Lo que más tiempo te come cada semana"**.
   Esa es la semilla: son las tres cosas que él mismo señaló.
2. `plantillas/`, para no repetir algo ya resuelto.
3. Las últimas líneas de `decisiones/registro.md`, para ver qué se decidió antes.

Si ese bloque está vacío o dice `> sin responder`, pregúntaselo aquí: "¿qué
hiciste esta semana que ya habías hecho la semana pasada, casi igual?"

## Los tres pasos

### 1. Encuentra (una, no cinco)

Propón **dos o tres candidatas** de lo que ya sabes, en una línea cada una, y
que él elija. Es más fácil elegir que inventar.

Una buena candidata cumple tres cosas: **se repite** (semanal o más seguido),
**es aburrida** (siempre igual) y **se le puede describir a alguien más**. Si
cada vez es distinta, no se automatiza todavía: se ordena primero.

### 2. Decide qué hacer con ella

En este orden. **Baja siempre por la escalera antes de subir.**

| Opción | Cuándo |
|---|---|
| **Dejar de hacerla** | Si nadie la nota cuando no pasa. Es la mejor victoria y es válida: escríbela igual. |
| **Hacerla una vez y reusarla** | Un texto, una plantilla, una lista. Es donde cae casi todo. |
| **Que la haga otro** | Si `contexto/equipo.md` dice que hay con quién. |
| **Que se haga sola** | Solo si las tres anteriores no aplican. |

Dos filtros duros:

- **Si no mueve un número, no se construye.** Pregúntale qué número mueve
  (horas, respuestas, ventas, errores). Si no hay ninguno, es entretenimiento.
- **Empieza por lo más simple que funcione.** Un texto guardado que se copia y
  pega gana a un sistema elegante que nunca se termina.

### 3. Escribe la plantilla

Crea `plantillas/<nombre-corto>.md`, en minúsculas, sin acentos y sin eñe, con:

```markdown
# <Nombre>

**Para qué:** <en una línea>
**Cuándo se usa:** <el momento exacto>
**Qué número mueve:** <el número>

## Cómo se usa

<Una o dos líneas: qué le dices a tu asistente para dispararla.>

---

<El texto, el prompt o los pasos. Con [corchetes] donde va lo que cambia cada vez.>
```

Y **agrega** al final de `decisiones/registro.md` una línea:

```
[AAAA-MM-DD] DECISIÓN: <qué se automatizó> | POR QUÉ: <el número que mueve> | QUÉ SIGUE: usarla la próxima vez que <el momento>
```

Son **dos escrituras** y las dos van declaradas: `plantillas/` se crea o se
reemplaza, `decisiones/registro.md` solo se agrega.

## Al cerrar

Pruébala una vez, ahí mismo, con un caso real de esta semana. Si no funcionó a la
primera, arréglala ahora: una plantilla que quedó a medias no se vuelve a abrir
nunca.

Cierra con una sola línea: qué queda hecho y cuándo la va a usar.
