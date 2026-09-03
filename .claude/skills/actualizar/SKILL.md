---
name: actualizar
description: Solo dentro del kit La Fábrica: no aplica fuera de esta carpeta. Trae la versión nueva del kit desde su repositorio: respalda la carpeta entera, reemplaza únicamente los nueve elementos que vienen con el kit y nunca toca los siete del dueño; si el repositorio no está abierto todavía, explica la ruta manual "lo tuyo viaja".
disable-model-invocation: true
---

# /actualizar

Traes la versión nueva del kit **sin tocar nada de lo que el dueño escribió**.

La regla que gobierna todo lo de abajo: **lo que viene con el kit se reemplaza,
lo del dueño no se toca jamás.**

## El reparto, memorízalo

**Lo que viene con el kit (9 elementos, se reemplazan):**

`.claude/skills/`, `.claude/settings.json`, `AGENTS.md`, `CLAUDE.md`,
`EMPIEZA-AQUI.md`, `PROBLEMAS.md`, `CAMBIOS.md`, `VERSION`, `LICENSE`.

**Del dueño (7 elementos, no se tocan nunca):**

`contexto/`, `memoria/`, `asistentes/`, `plantillas/`, `decisiones/`,
`informes/`, `conexiones.md`.

**Excepción explícita:** `.claude/settings.local.json` es del dueño. Lo crea
Claude Code cuando él aprueba permisos. **Ninguna actualización lo toca**, aunque
viva dentro de `.claude/`.

## Los seis pasos

### 1. Compara versiones

Lee la primera línea de `VERSION` (la local) y pide la remota:

```
https://raw.githubusercontent.com/blu7print/la-fabrica/main/VERSION
```

**Si no la alcanzas** (el repositorio todavía está cerrado, o no hay red),
detente aquí y dile exactamente esto:

> El repositorio todavía no está abierto, así que la actualización automática aún
> no funciona. Cuando salga una versión nueva en la comunidad, se actualiza a
> mano y toma dos minutos. Te digo cómo abajo.

Y muéstrale la **ruta manual** de la sección siguiente. **Mientras el repositorio
siga cerrado, este es el comportamiento correcto de la versión 1.0.0**, no una
falla: no lo presentes como un error.

Si la remota es igual a la local, dile que ya está al día y termina.

### 2. Muestra qué va a recibir

Trae el `CAMBIOS.md` remoto y muéstrale las entradas nuevas. **Pide
confirmación.** No sigas sin un sí explícito.

### 3. Respalda todo

Copia la carpeta entera a `../la-fabrica-respaldo-AAAA-MM-DD/`, un nivel arriba.

Dile antes de hacerlo que esta es **la única vez** que escribes fuera de la
carpeta, y por qué. Si el respaldo falla, **para**: sin respaldo no se sigue.

### 4. Trae la versión nueva

Clona a una carpeta temporal:

```
git clone --depth 1 https://github.com/blu7print/la-fabrica <temporal>
```

Elige los comandos según el sistema del dueño (bash en Mac o Linux, PowerShell en
Windows) y **muéstraselos antes de correrlos**. Él los aprueba una vez. Git está
disponible en la ruta recomendada: la app lo pide en Windows y Mac ya lo trae.

Si el clon pide credenciales, es que el repositorio sigue cerrado: vuelve al
paso 1 y dale la ruta manual.

### 5. Reemplaza solo lo del kit

Copia desde la temporal **únicamente los nueve elementos** de la lista de arriba.

Uno por uno, por nombre. **Nunca copies la carpeta entera encima**: eso pisaría
`contexto/`, `memoria/` y todo lo que el dueño construyó. `.claude/skills/` se
reemplaza completa (borra la vieja y pon la nueva, para que una habilidad que se
eliminó no quede colgada); `.claude/settings.json` se reemplaza;
`.claude/settings.local.json` **se queda como está**.

### 6. Limpia y reporta

Borra la temporal. Muéstrale, en tres líneas:

- La versión de antes y la de ahora.
- Qué cambió, sacado de `CAMBIOS.md`.
- Dónde quedó el respaldo, y que lo puede borrar cuando compruebe que todo anda.

## La ruta manual: "lo tuyo viaja"

Cuando la automática no está disponible, o si algo falla:

1. Descomprime el kit nuevo **al lado** del viejo, sin encimarlo.
2. Copia del viejo al nuevo tus siete cosas: `contexto/`, `memoria/`,
   `asistentes/`, `plantillas/`, `decisiones/`, `informes/` y `conexiones.md`.
   Reemplaza cuando pregunte: lo tuyo gana.
3. Abre el nuevo con la app de Claude y corre `/auditoria` para confirmar que
   todo llegó.
4. Deja el viejo un par de días como respaldo, y después bórralo.

## Promesa de compatibilidad

Una versión menor **nunca** renombra ni mueve una carpeta del dueño. Renombrar es
un cambio mayor, viene con su propia habilidad de migración, y como mucho pasa
una vez al año. Si una actualización menor parece querer renombrar algo, **para y
dilo**: es un error, no una mejora.

## Reglas

1. **Nunca toques los 7 elementos del dueño.** Ni para "ordenarlos", ni para
   "arreglar el formato".
2. **Nunca sigas sin el respaldo hecho.**
3. **Nunca clones dentro de la carpeta del kit.** La temporal va afuera y se borra.
4. **Muestra los comandos antes de correrlos.** El dueño aprueba una vez, viendo
   qué aprueba.
