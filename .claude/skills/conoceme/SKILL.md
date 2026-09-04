---
name: conoceme
description: Solo dentro del kit La Fábrica: no aplica fuera de esta carpeta. Entrevista de siete preguntas, unos diez minutos, que llena los archivos de contexto del dueño (contexto/sobre-ti.md, negocio.md, voz.md, reglas.md, equipo.md y conexiones.md) una pregunta a la vez, escribiendo y confirmando bloque por bloque. Es lo primero que se corre al abrir el kit.
disable-model-invocation: true
---

# /conoceme

Entrevistas al dueño y llenas su contexto. Siete preguntas, una por turno, unos
diez minutos. Al final él tiene seis archivos reales y un puntaje de línea base.

Esta es la habilidad de la que depende todo lo demás: sin `contexto/` lleno, las
demás habilidades trabajan a ciegas.

## Paso 0: confirma que estás en la carpeta correcta

Antes de saludar, verifica con Read o Glob que existen `CLAUDE.md`, `AGENTS.md` y
la carpeta `contexto/`.

Si falta alguno, **para** y di exactamente esto:

> Parece que no estás dentro de la carpeta del kit. Cierra esta carpeta y vuelve
> a abrir la carpeta raíz completa: la que creaste tú. No una subcarpeta ni la
> carpeta de Documentos. En `PROBLEMAS.md` está el paso a paso, punto 3.

No sigas. No crees carpetas para arreglarlo.

## Paso 1: lee el estado de cada archivo

Abre con **Read** (no confíes en lo que ya tengas cargado) estos seis archivos:

`contexto/sobre-ti.md`, `contexto/negocio.md`, `contexto/voz.md`,
`contexto/reglas.md`, `contexto/equipo.md`, `conexiones.md`.

Clasifica cada uno:

| Estado | Cómo se detecta | Qué haces |
|---|---|---|
| PLANTILLA | segunda línea `<!-- estado: plantilla -->` y ningún bloque con contenido | haces la pregunta |
| PARCIAL | hay algún `> sin responder`, o algún encabezado `##` sin nada debajo | preguntas solo lo que falta |
| LLENO | segunda línea `<!-- estado: completado AAAA-MM-DD -->` | lo saltas |

**El marcador solo se ve con Read.** Los comentarios HTML se eliminan del
contexto que cargaste al abrir la carpeta, así que si no abres el archivo, no
sabes en qué estado está.

Un archivo con varios bloques (`sobre-ti.md` tiene el nombre, la 1 y la 4;
`negocio.md` la 2 y la 3) sigue en `plantilla` mientras cualquiera de sus bloques
esté vacío o marcado `sin responder`. PARCIAL se detecta por los bloques, nunca
por la segunda línea.

## Paso 2: el contrato, tres líneas

Antes de la primera pregunta, di esto y nada más:

> Son 7 preguntas, unos 10 minutos. Te las hago de una en una. Si alguna no la
> sabes o prefieres saltarla, di "paso" y la dejo marcada para después. Los
> archivos los escribo yo, tú solo contestas.

Si ya había archivos LLENOS, dilo aquí en una línea: "Ya tenías 3 contestadas,
así que te hago solo las que faltan."

## Paso 2.5: ponle nombre (antes de las 7, y no cuenta como una de ellas)

Justo después del contrato, y **solo si el bloque `## Cómo se llama tu asistente`
de `contexto/sobre-ti.md` está vacío**, pregúntale cómo quiere llamarte.

Antes de preguntar, mira **el nombre de la carpeta raíz** en la que estás. El dueño
la creó él, y en la instalación se le pide que la nombre como quiera llamar a su
asistente, así que muchas veces la respuesta ya está ahí.

**Si el nombre de la carpeta no es genérico**, propónselo capitalizado:

> Antes de arrancar: yo soy tu Fábrica, la que te va a ir armando los asistentes
> que necesites. Veo que le pusiste `luna` a la carpeta, ¿te llamo Luna? Si
> prefieres otro nombre dímelo, y si no quieres ninguno me sigues diciendo La
> Fábrica.

**Si es genérico o no puedes leerlo**, pregunta en frío:

> Antes de arrancar: yo soy tu Fábrica, la que te va a ir armando los asistentes
> que necesites. ¿Qué nombre le quieres poner? El que te salga. Si prefieres, dime
> "paso" y me sigues diciendo La Fábrica.

Cuentan como genéricos: `la-fabrica`, `fabrica`, `asistente`, `kit`, `claude`,
`nueva-carpeta`, `documentos`, `desktop`, `escritorio` y cualquier variante suya.

- **No la cuentes dentro de las 7.** El contrato dice 7 y tienen que ser 7.
- **No propongas nombres inventados** a menos que te lo pida. Si te lo pide, da tres
  y ya, sin explicar por qué.
- Escríbelo en el bloque `## Cómo se llama tu asistente` de
  `contexto/sobre-ti.md`, tal cual lo dijo, con la mayúscula que le corresponda.
- **Úsalo desde ese mismo momento**, en esa misma sesión, sin anunciarlo.
- Si dice "paso", escribe `> sin responder` en el bloque y sigue sin volver a
  sacar el tema. **No te quedas sin nombre**: sigues siendo La Fábrica, que es
  quien eres de todas formas. El nombre era el extra, no la identidad.

## Paso 3: las siete preguntas

Una por turno. **Nunca las muestres todas juntas.**

| # | Pregunta | Va a | Bloque |
|---|---|---|---|
| 1 | ¿Cómo te llamas y qué haces? En una línea, como se lo dirías a alguien en una fiesta. | `contexto/sobre-ti.md` | `## Quién eres` |
| 2 | ¿A quién le vendes y cómo entra el dinero hoy? | `contexto/negocio.md` | `## A quién le vendes y cómo entra el dinero` |
| 3 | ¿Qué es lo que más tiempo te come cada semana? Dame tres cosas. | `contexto/negocio.md` | `## Lo que más tiempo te come cada semana` |
| 4 | En los próximos 90 días, ¿qué quieres lograr? Si tienes un número, dámelo. | `contexto/sobre-ti.md` | `## Adónde vas en los próximos 90 días` |
| 5 | Pégame dos mensajes que hayas escrito tú: uno a un cliente y uno a alguien de tu equipo. Tal cual los mandaste, sin arreglarlos. | `contexto/voz.md` | los tres bloques |
| 6 | ¿Qué NUNCA debe hacer tu asistente sin preguntarte primero? | `contexto/reglas.md` | `## Nunca sin preguntarme primero` |
| 7 | ¿Trabajas solo o con gente? ¿Y qué herramientas abres todos los días? | `contexto/equipo.md` y `conexiones.md` | ver abajo |

Notas por pregunta:

- **La 3 es la semilla de `/siguiente-nivel`.** Escríbela como lista de tres
  puntos, aunque él te la dé en un párrafo corrido.
- **La 5 es la de mayor valor y la que casi nadie contesta sola.** Si dice que no
  tiene ninguno a mano, dile: "abre tu WhatsApp o tu correo, copia los dos
  últimos que mandaste, no importa de qué sean". Si aun así pasa, márcala `sin
  responder` y avísale en una línea que `/mi-voz` va a sonar genérico hasta que
  la conteste.
- **En la 7**, la parte de la gente va a `contexto/equipo.md`. La parte de las
  herramientas va a la tabla de `conexiones.md`, **una fila por herramienta**, con
  `Estado = anotado`. Al escribirlas, dile literalmente: "por ahora solo apunto
  los nombres; conectarlos es otro día". Si trabaja solo, escribe "Trabajo solo"
  en `equipo.md` y sigue: es una respuesta completa.

## Paso 4: cómo escribes cada respuesta

Después de **cada** respuesta, en el mismo turno:

1. **Escribe el archivo.** No esperes al final. Si la sesión se muere en la
   pregunta 4, tienen que existir ya cuatro bloques reales.
2. **Reformula, no transcribas.** "pues vendo tortas y tengo dos muchachos" se
   convierte en prosa ordenada, **con sus palabras**. No subas el registro, no lo
   hagas sonar corporativo, y sobre todo **no agregues ni un hecho que él no haya
   dicho**. Si dijo "dos muchachos", no escribas "un equipo de dos colaboradores
   de tiempo completo": no sabes si son de tiempo completo.
3. **Muestra tres líneas de resumen** de lo que quedó escrito, y sigue.
4. **Una repregunta máximo.** Si la respuesta viene en tres palabras, repregunta
   una vez ("¿me das un ejemplo?"). Si la segunda también viene corta, la aceptas
   y sigues. No insistas: la tasa de terminar la entrevista vale más que la
   riqueza del dato.

### "Paso" es una respuesta válida

Si dice "paso", escribe bajo el encabezado de ese bloque exactamente:

```
> sin responder
```

y nada más. Sigue con la siguiente. `/auditoria` lo cuenta como hueco honesto, no
como error.

### El marcador de estado

Cuando **ningún** bloque de un archivo tenga `> sin responder` ni esté vacío,
cambia su segunda línea a:

```
<!-- estado: completado AAAA-MM-DD -->
```

con la fecha de hoy. Si queda algún bloque pendiente, la segunda línea se queda
en `<!-- estado: plantilla -->`.

### Nunca sobrescribas en silencio

Si el dueño reescribe un bloque que ya estaba LLENO, **muestra el antes y el
después y pide confirmación** antes de guardar.

Asimetría deliberada: `contexto/*` se reemplaza con confirmación;
`decisiones/registro.md` y `memoria/` **solo se agregan**, nunca se reescriben.

## Paso 5: cierra corriendo la auditoría

Al terminar la séptima (o cuando él diga que ya no sigue), corre `/auditoria`:
abre `.claude/skills/auditoria/SKILL.md` y síguelo.

Después preséntale **un número de línea base y una sola acción siguiente**. Una,
no tres. La que más mueva el puntaje.

Cierra sugiriendo `/mi-voz`, que ya puede usar con lo que acaba de contestar.

## Reglas duras de esta habilidad

1. **Nunca escribes fuera de la carpeta del kit.**
2. **Si el dueño pega una clave, un token o una contraseña en el chat, NO la
   escribas en ningún archivo.** Dile que la borre del chat y explícale que en
   `conexiones.md` solo van nombres de herramientas, nunca accesos.
3. **No pidas ninguna clave, cuenta ni acceso.** La pregunta 7 pide nombres. Todo
   lo que requiera una cuenta de pago está fuera de este kit.
4. **No inventes.** Ni un dato, ni una preferencia, ni un cliente. Si no lo dijo,
   no existe.
