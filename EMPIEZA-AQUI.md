# Empieza aquí

Esta carpeta es tu asistente. Todavía no sabe nada de ti: en unos diez minutos
va a saber quién eres, a quién le vendes, cómo escribes y qué no debe hacer sin
preguntarte.

No hay nada que instalar dentro de la carpeta y no hay nada que programar.

---

## Lo que necesitas antes de empezar

| Qué | Detalle |
|---|---|
| **Claude o Codex** | Con **Claude** necesitas un plan de pago que incluya Claude Code (el gratuito no lo incluye). Con **Codex**, de OpenAI, puedes probarlo incluso con la cuenta gratuita de ChatGPT, aunque rinde poco antes de toparte con el límite. |
| **La app en tu computadora** | La app de Claude, pestaña **Code**, es la forma recomendada y no necesita terminal. |
| **Si estás en Windows: Git for Windows** | La app lo pide para trabajar con carpetas locales. Se instala una vez, desde git-scm.com, dándole siguiente a todo. |
| **15 minutos** | Diez son la entrevista. |

Este kit está hecho y probado de punta a punta con **Claude**, y es la ruta del
video. Con **Codex** también funciona: lleva un mapa propio (`AGENTS.md`) escrito
para que cualquier asistente de este tipo sepa moverse aquí. Si te trabas en
Codex, prueba en Claude antes de dar por roto el kit.

---

## Cómo se instala (la forma recomendada, sin terminal)

1. **Descarga** el archivo del kit. Viene comprimido (un `.zip`).
2. **Descomprímelo.** En Windows: clic derecho sobre el archivo, "Extraer todo".
   En Mac: doble clic. Te queda una **carpeta**, no un archivo suelto.
3. **Ponla donde la encuentres fácil**, por ejemplo el Escritorio. Se llama
   `la-fabrica`, y si quieres **le puedes cambiar el nombre** por el que le vayas
   a poner a tu asistente: `mi-fabrica`, `el-taller`, `luna`, lo que sea. No se
   rompe nada, todo aquí adentro funciona igual.
   *Una sola condición:* escríbelo sin acentos, sin eñes y sin espacios (usa
   guiones). En Windows y en OneDrive, un nombre con acentos rompe la ruta sin
   avisar.
4. Abre la **app de Claude** en tu computadora.
5. Entra a la pestaña **Code**.
6. Elige **Local** y luego **Seleccionar carpeta**.
7. Selecciona **esa carpeta**, completa.
8. Te va a preguntar **si confías en esta carpeta**. Di que sí: es tuya, la
   acabas de descomprimir. Ese "sí" es lo que le da permiso de escribir en tus
   archivos sin interrumpirte a cada rato.
9. Escribe **`/conoceme`** y dale enter.

Ya está. Lo primero que va a hacer es preguntarte **cómo lo quieres llamar**, y
después vienen las siete preguntas.

> **Punto 1, el error más común:** abre **la carpeta completa**, la raíz, nunca
> una subcarpeta (`contexto/`, `asistentes/`) y nunca tu carpeta de Documentos
> entera. Si abres la carpeta equivocada, escribes `/` y no te aparece ningún
> comando. Es la señal.

**¿Prefieres la terminal?** Entra a la carpeta y escribe `claude` (o `codex`). Es
exactamente lo mismo: comparte la configuración, las habilidades y los comandos
con la app.

---

## Las siete cosas que sabe hacer

Escribe el comando con la barra `/` y dale enter.

| Comando | Qué hace |
|---|---|
| `/conoceme` | Te pregunta cómo quieres llamarlo, te hace 7 preguntas y llena tu contexto. **Empieza por aquí.** |
| `/mi-voz` | Te redacta un mensaje, un correo o una publicación **con tu forma de escribir**. Esta es la que te va a hacer volver mañana. |
| `/arranca` | Cinco minutos cada mañana para ordenar qué toca hoy. |
| `/auditoria` | Te pone un puntaje de 0 a 100 y te dice los tres huecos más grandes. |
| `/fabrica` | Crea un asistente que hace una sola cosa (cotizar, contestar clientes). |
| `/siguiente-nivel` | Una vez por semana: encuentra algo repetitivo y lo convierte en algo que se hace solo. |
| `/actualizar` | Trae la versión nueva del kit sin tocar nada de lo tuyo. |

---

## Cómo se le hace recordar algo

Escribe **"recuerda esto"** y luego el dato. Por ejemplo:

> recuerda esto: mi proveedor cierra los sábados

Queda como un archivo en `memoria/`, que puedes abrir, corregir o borrar cuando
quieras. Es tuyo y viaja contigo si copias la carpeta a otra computadora.

---

## Qué es tuyo y qué es del kit

**Tuyo** (nadie lo toca nunca, ni una actualización): `contexto/`, `memoria/`,
`asistentes/`, `plantillas/`, `decisiones/`, `informes/` y `conexiones.md`.

**Del kit** (esto es lo que se reemplaza al actualizar): todo lo demás.

## Cómo se actualiza

Escribe `/actualizar`. Si te dice que el repositorio todavía no está abierto,
significa que la actualización automática aún no está disponible: entonces la
ruta es manual y se llama **"lo tuyo viaja"**. Descomprime el kit nuevo al lado
del viejo y copia tus siete cosas de arriba, del viejo al nuevo. El viejo se
queda como respaldo.

---

## Si algo no funciona

Abre **`PROBLEMAS.md`**. Están las once fallas más comunes con su solución en una
línea. Si no está ahí, escribe en el canal **Preguntas** de la comunidad: las
respuestas se quedan ahí para el que venga después.

---

## Licencia

Licencia MIT: úsalo, cámbialo y quédatelo. El texto completo está en `LICENSE`.

---

Hecho por Bluprint Agency - https://bluprintagency.com
