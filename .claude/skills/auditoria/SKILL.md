---
name: auditoria
description: Solo dentro del kit La Fábrica: no aplica fuera de esta carpeta. Califica el asistente del dueño de 0 a 100 en cinco pilares (Conocimiento, Alcance, Habilidades, Memoria, Autonomía), detecta los archivos que faltan y devuelve los tres huecos más grandes con su siguiente paso concreto; guarda el informe en informes/auditoria-AAAA-MM-DD.md. La llama /conoceme al cerrar la entrevista.
---

# /auditoria

Le pones un número a algo que sin número es una sensación. Cinco pilares, veinte
puntos cada uno, cien en total. Devuelves el puntaje, la barra por pilar y **los
tres huecos más grandes**, cada uno con una acción concreta.

El número de hoy importa poco. Lo que importa es que dentro de un mes haya otro
al lado.

## Cómo mides

Lee con Read. **Cuenta por nombre de archivo**: no abras cada archivo completo,
no lo necesitas y gastas la sesión. Solo abres entero lo que tienes que
clasificar (los seis de contexto y la tabla de `conexiones.md`).

**Detecta lo que FALTA, no solo lo que está vacío.** Un archivo borrado y un
archivo en blanco puntúan parecido pero se arreglan distinto, y el que falta va
siempre primero en los huecos.

### Pilar 1: Conocimiento (20) - ¿sabe quién eres?

Mira `contexto/sobre-ti.md`, `contexto/negocio.md`, `contexto/voz.md`,
`contexto/reglas.md`, `contexto/equipo.md`.

| Por cada uno de los 5 | Puntos |
|---|---|
| segunda línea `completado` y ningún `> sin responder` | 3 |
| existe y tiene algo, pero sigue en `plantilla` o tiene algún `> sin responder` | 1 |
| existe y está en blanco, o **no existe** | 0 |

Más **5 puntos** si no falta ninguno de los seis archivos (los cinco de
`contexto/` y `conexiones.md`). Máximo 20.

`equipo.md` con "trabajo solo" cuenta como completo. Es una respuesta, no un
hueco.

### Pilar 2: Alcance (20) - ¿hasta dónde llega?

Cuenta las filas de la tabla de `conexiones.md` (las que tienen contenido, no la
cabecera).

| Condición | Puntos |
|---|---|
| 1 o más filas en estado `anotado` | 6 |
| 1 o más en `conectado` que tu asistente pueda **leer** | 7 |
| 1 o más en `conectado` a las que pueda **escribir** | 7 |

Máximo 20. **El crédito parcial por `anotado` es deliberado**: apuntar la
herramienta ya cambia el consejo que te da tu asistente, aunque no la toque.

Este pilar va a marcar bajo y está bien. El kit viene desconectado a propósito.

### Pilar 3: Habilidades (20) - ¿qué sabe hacer?

| Condición | Puntos |
|---|---|
| Las 7 habilidades del kit están en `.claude/skills/` | 4 |
| 1 o más habilidades que agregó el dueño (una octava carpeta con `SKILL.md`) | 8 |
| 1 o más archivos en `plantillas/` además de `LEEME.md` | 8 |

Máximo 20.

### Pilar 4: Memoria (20) - ¿se acuerda?

| Condición | Puntos |
|---|---|
| `memoria/MEMORIA.md` existe pero sin ningún hecho | 0 |
| 1 o 2 archivos de hecho en `memoria/` (sin contar `LEEME.md` y `MEMORIA.md`) | 5 |
| 3 o más | 8 |
| `decisiones/registro.md` con 1 o más entradas | 7 |
| 1 o más asistentes en `asistentes/` además de `ejemplo/` | 5 |

Máximo 20. Los tramos de hechos no se suman entre sí: 3 hechos son 8, no 13.

Un kit recién descomprimido saca **0** en este pilar, a propósito. Dilo así:
"Memoria: 0 de 20. Dime 'recuerda esto' seguido de cualquier cosa y verás."

### Pilar 5: Autonomía (20) - ¿trabaja sin ti?

| Condición | Puntos |
|---|---|
| Un informe en `informes/` de hace menos de 8 días | 5 |
| Una entrada en `decisiones/registro.md` de hace menos de 8 días | 5 |
| 1 o más automatizaciones reales declaradas en `conexiones.md` o `plantillas/` | 10 |

Máximo 20. La fecha del informe sale de su nombre
(`auditoria-AAAA-MM-DD.md`); la de la decisión, del `[AAAA-MM-DD]` de la línea.

## Cómo lo presentas

Una barra por pilar: **un bloque lleno por cada 2 puntos**, diez bloques en
total.

```
Conocimiento  ████████░░  15/20  Sólido
Alcance       ███░░░░░░░   6/20  Empezado
Habilidades   ██░░░░░░░░   4/20  Vacío
Memoria       ░░░░░░░░░░   0/20  Vacío
Autonomía     ░░░░░░░░░░   0/20  Vacío
                            ----
                          25/100
```

Etiqueta por pilar: **Vacío** por debajo de 6, **Empezado** de 6 a 11, **Sólido**
de 12 a 16, **Fuerte** 17 o más.

Después, **los tres huecos más grandes**, en este orden de prioridad:

1. Archivos que **faltan** (siempre primero, por grandes que sean los otros).
2. Los pilares con menos puntos.
3. Dentro de un pilar, lo que sume más puntos con menos trabajo.

Cada hueco lleva **una acción**, concreta y en una línea: qué comando correr o
qué escribir. Nada de "mejora tu contexto".

## Calibración, dísela cuando el número confunda

- Un kit recién descomprimido cae entre **5 y 15**. Es lo normal, no es un
  problema.
- Después de un `/conoceme` completo, entre **25 y 40**.
- Por encima de **80 sin conexiones reales**, el número está inflado: significa
  que hay muchos archivos y poco trabajo hecho de verdad.

Nunca celebres un número alto. Di qué falta.

## Versión

Imprime en cada corrida la primera línea de `VERSION`.

Si tienes acceso a la red, mira
`https://raw.githubusercontent.com/blu7print/la-fabrica/main/VERSION`. Si
responde y trae una versión más nueva, avisa en una línea: "hay una versión
nueva, corre `/actualizar`". **Si no responde, no digas nada**: mientras el
repositorio siga cerrado no responder es lo esperado, y un aviso de error cada
vez sería ruido.

## Guarda el informe

Escribe `informes/auditoria-AAAA-MM-DD.md` con la fecha de hoy: el puntaje total,
las cinco barras, los tres huecos con su acción y la línea de `VERSION`.

Si ya existe uno de hoy, sobrescríbelo (es la foto de hoy, no un histórico del
día). Los de días anteriores **nunca** se tocan.

## Nota sobre importaciones que faltan

**Medido el 2026-09-03** con el CLI real sobre una copia de este mismo árbol, con
una línea `@no-existe.md` agregada a `CLAUDE.md`: la sesión arrancó normal, sin
error y sin advertencia, y cargó los otros ocho imports. La línea que apunta a un
archivo inexistente **se ignora en silencio**.

O sea: si el dueño borra `contexto/voz.md`, nada se rompe de forma visible. Su
asistente simplemente deja de saber cómo escribe él, y nadie avisa.

Por eso este pilar mide los archivos que faltan directamente con Read y Glob, en
vez de esperar a que la herramienta se queje. Es la única red que hay.

## Nota sobre los permisos y el diálogo de confianza

**Medido en la misma prueba:** hasta que la carpeta no se marca como de
confianza, Claude Code **ignora las siete reglas** de `.claude/settings.json` y
lo dice así: `Ignoring 7 permissions.allow entries from .claude/settings.json:
this workspace has not been trusted`.

Es decir: el diálogo de confianza que aparece la primera vez **no es un trámite**,
es lo que enciende los permisos pre-aprobados. Si el dueño te dice que le pregunta
permiso por cada archivo que escribes, casi siempre es que no lo aceptó. Está en
`PROBLEMAS.md`, entrada 4.
