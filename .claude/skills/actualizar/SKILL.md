---
name: actualizar
description: Solo dentro del kit La Fábrica: no aplica fuera de esta carpeta. Trae la versión nueva del kit desde github.com/blu7print/la-fabrica: deja el repositorio del dueño limpio, clona a una carpeta temporal fuera, reemplaza únicamente los diez elementos que vienen con el kit, nunca toca los del dueño, y cierra con un commit que se puede deshacer.
disable-model-invocation: true
---

# /actualizar

Traes la versión nueva del kit **sin tocar nada de lo que el dueño escribió**.

La regla que gobierna todo lo de abajo: **lo que viene con el kit se reemplaza,
lo del dueño no se toca jamás.**

## El reparto, memorízalo

**Lo que viene con el kit (10 elementos, se reemplazan):**

`.claude/skills/`, `.claude/settings.json`, `AGENTS.md`, `CLAUDE.md`, `README.md`,
`EMPIEZA-AQUI.md`, `PROBLEMAS.md`, `CAMBIOS.md`, `VERSION`, `LICENSE`.

**Del dueño (no se tocan nunca):**

`contexto/`, `memoria/`, `asistentes/`, `plantillas/`, `decisiones/`, `informes/`,
`conexiones.md`.

**Dos excepciones explícitas**, ambas del dueño aunque parezcan del kit:

- `.claude/settings.local.json` lo crea Claude Code cuando él aprueba permisos.
- `.gitignore` se envía una sola vez, al instalar. Ninguna actualización lo toca.

## Los seis pasos

### 1. Compara versiones

Lee la primera línea de `VERSION` (la local) y pide la remota:

```
https://raw.githubusercontent.com/blu7print/la-fabrica/main/VERSION
```

Si no la alcanzas, es un problema de red. Dile:

> No pude alcanzar GitHub para ver si hay una versión nueva. Revisa tu conexión y
> vuelve a intentarlo en un rato.

Y termina. No inventes una ruta alterna.

Si la remota es igual a la local, dile que ya está al día y termina.

### 2. Muestra qué va a recibir

Trae el `CAMBIOS.md` remoto y muéstrale las entradas nuevas. **Pide
confirmación.** No sigas sin un sí explícito.

### 3. Deja su repositorio limpio

Su carpeta es un repositorio de git suyo desde que la instaló. Esa es la red de
seguridad de esta habilidad, así que se prepara antes de tocar nada.

Corre `git status`. Si hay cambios sin guardar, díselo en una línea y guárdalos:

> Tienes cambios sin guardar. Los dejo guardados antes de empezar, así puedes
> volver a este punto si la actualización no te gusta.

```
git add -A && git commit -m "antes de actualizar"
```

**Si no hay git en la máquina** (el comando no existe), entonces sí haces respaldo a
la antigua: copia la carpeta entera un nivel arriba, a
`../<nombre-de-esta-carpeta>-respaldo-AAAA-MM-DD/`. Usa el nombre real de la carpeta
en la que estás: el dueño la nombró como quiso. Dile antes de hacerlo que esta es la
única vez que escribes fuera de la carpeta, y por qué.

**Sin una de las dos redes, no sigas.**

### 4. Trae la versión nueva

Baja la rama `main` **como archivo comprimido** a una carpeta temporal **fuera**
de su carpeta:

```
https://github.com/blu7print/la-fabrica/archive/refs/heads/main.tar.gz
```

**No la clones.** Un clon trae un `.git` nuestro, y borrarlo después es justo lo
que el entorno bloquea por seguridad; el comprimido no trae ninguno.

Elige los comandos según el sistema del dueño (bash en Mac o Linux, PowerShell en
Windows) y **muéstraselos antes de correrlos**. Él los aprueba una vez.

### 5. Reemplaza solo lo del kit

Copia desde la temporal **únicamente los diez elementos** de la lista de arriba.

Uno por uno, por nombre. **Nunca copies la carpeta entera encima**: eso pisaría
`contexto/`, `memoria/` y todo lo que el dueño construyó. `.claude/skills/` se
reemplaza completa (borra la vieja y pon la nueva, para que una habilidad que se
eliminó no quede colgada); `.claude/settings.json` se reemplaza;
`.claude/settings.local.json` y `.gitignore` **se quedan como están**.

La temporal no trae ningún `.git`, así que no hay nada que evitar copiar. El
repositorio de esta carpeta es el suyo y no se toca.

### 6. Limpia, guarda y reporta

Borra la temporal y guarda la actualización en su historial:

```
git add -A && git commit -m "actualizado a <version>"
```

Muéstrale, en tres líneas:

- La versión de antes y la de ahora.
- Qué cambió, sacado de `CAMBIOS.md`.
- Que si algo no le gusta, con decirte **"deshaz la actualización"** vuelves al
  commit anterior.

Si hiciste respaldo por copia (no había git), en vez de eso dile dónde quedó y que
lo puede borrar cuando compruebe que todo anda.

## Deshacer

Si el dueño te dice "deshaz la actualización", vuelves al commit anterior a la
actualización y se lo confirmas nombrando la versión a la que regresó. Muéstrale el
comando antes de correrlo.

Con respaldo por copia, deshacer es restaurar la carpeta que copiaste.

## Promesa de compatibilidad

Una versión menor **nunca** renombra ni mueve una carpeta del dueño. Renombrar es
un cambio mayor, viene con su propia habilidad de migración, y como mucho pasa
una vez al año. Si una actualización menor parece querer renombrar algo, **para y
dilo**: es un error, no una mejora.

## Reglas

1. **Nunca toques lo del dueño.** Ni para "ordenarlo", ni para "arreglar el
   formato".
2. **Nunca sigas sin una red de seguridad**, el commit o la copia.
3. **Nunca descargues dentro de la carpeta del kit.** La temporal va afuera y se
   borra.
4. **Nunca toques el remoto de su repositorio.** `origin` es suyo, para el día que
   respalde su Fábrica en su propio GitHub.
5. **Muestra los comandos antes de correrlos.** El dueño aprueba una vez, viendo
   qué aprueba.
