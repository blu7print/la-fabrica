# La Fábrica

Una carpeta en tu computadora de la que salen los asistentes que usas para tu
negocio. Ella misma es el primero: te conoce a ti, sabe a quién le vendes, cómo
escribes y qué no debe hacer sin preguntarte.

Es gratis, es tuya, y se instala en unos minutos sin escribir una línea de código.

## La diferencia con un chat

Un chat te contesta. Le pides una cotización y te devuelve un texto en la pantalla,
que tú tienes que copiar, pegar, guardar y ordenar. El trabajo de mover las cosas de
lugar sigue siendo tuyo.

Este tiene manos y piernas.

Vive dentro de una carpeta y se mueve por ella: abre tus archivos, los lee, escribe,
guarda, crea carpetas nuevas y deja las cosas donde van. Por eso no le pides un
párrafo, le pides **el resultado terminado**. No "escríbeme un texto para la
cotización", sino "arma la cotización de este cliente y guárdamela". Y cuando
vuelvas mañana, ahí está.

## Lo que necesitas

| Qué | Detalle |
|---|---|
| **Claude o Codex** | Con **Claude** necesitas un plan de pago que incluya Claude Code (el gratuito no lo incluye). Con **Codex**, de OpenAI, puedes probarlo incluso con la cuenta gratuita de ChatGPT, aunque rinde poco antes de toparte con el límite. |
| **La app en tu computadora** | La app de Claude, pestaña **Code**. No necesitas terminal. |
| **Si estás en Windows: Git for Windows** | La app lo pide para trabajar con carpetas locales. Se instala una vez, desde git-scm.com, dándole siguiente a todo. |
| **15 minutos** | Diez son la entrevista inicial. |

Este kit está hecho y probado de punta a punta con **Claude**, que es la ruta del
video. Con **Codex** también funciona: lleva un mapa propio (`AGENTS.md`) escrito
para que cualquier asistente de este tipo sepa moverse aquí.

## Cómo se instala

**1. Crea una carpeta** con el nombre que le quieras poner a tu asistente: `luna`,
`taller`, `mi-fabrica`, el que sea.

- Ponla en tu carpeta de usuario, la que lleva tu nombre: `C:\Users\tunombre\luna`
  en Windows, `/Users/tunombre/luna` en Mac.
- **No la pongas en Documentos ni en el Escritorio.** En Windows esas dos suelen
  estar dentro de OneDrive, que deja los archivos en la nube hasta que los abres, y
  tu asistente necesita que estén de verdad ahí. Lo mismo con Google Drive y
  Dropbox.
- Escribe el nombre sin acentos, sin eñes y sin espacios (usa guiones).

**2. Abre esa carpeta** con la app de Claude: pestaña **Code**, luego **Local**,
luego **Seleccionar carpeta**. Va a estar vacía. Es normal.

**3. Te pregunta si confías en esta carpeta.** Di que sí: la acabas de crear tú. Ese
sí es lo que le da permiso de escribir en tus archivos sin interrumpirte a cada
rato.

**4. Pega esto tal cual y dale enter:**

> Instala en esta carpeta el kit de https://github.com/blu7print/la-fabrica. Baja
> el contenido de la rama main como archivo comprimido, **no lo clones**, para que
> no quede ningún `.git` del repositorio, y déjalo directamente aquí sin crear una
> subcarpeta. Después deja esta carpeta como un repositorio nuevo mío:
> `git init -b main`, todo agregado y un primer commit; si git te pide una
> identidad, configúrala solo para esta carpeta. Al terminar, dime que cierre y
> vuelva a abrir la carpeta.

No necesitas entender la última parte: es para él. Te va a pedir permiso una o dos
veces, acepta.

**5. Cierra la carpeta y vuélvela a abrir**, por el mismo camino. Esto es lo que
hace que aparezcan los comandos.

**6. Escribe `/conoceme`** y dale enter.

Lo primero que hace es presentarse y preguntarte cómo quieres llamarlo. Después
vienen siete preguntas, una por una, unos diez minutos.

### Si prefieres la terminal

Entra a la carpeta vacía y corre:

```bash
curl -L https://github.com/blu7print/la-fabrica/archive/refs/heads/main.tar.gz | tar xz --strip-components=1
git init -b main
git config user.name "mi fabrica" && git config user.email "mifabrica@local"
git add -A && git commit -m "mi fabrica, dia uno"
```

Después escribe `claude` (o `codex`) y luego `/conoceme`. Es exactamente lo mismo:
comparte la configuración, las habilidades y los comandos con la app.

## Ya adentro

Abre **`EMPIEZA-AQUI.md`**. Ahí están los siete comandos, cómo se le hace recordar
algo, cómo se actualiza y qué hacer si algo no funciona.

Tu carpeta queda siendo un repositorio de git tuyo, sin conexión con este. El día
que quieras respaldarla en tu propio GitHub, son dos comandos.

## Una aclaración honesta

Tiene manos, pero solo dentro de su carpeta. **No está conectado a nada más**: no
lee tu correo, no entra a tu WhatsApp y no toca tu calendario. Anota qué
herramientas usas, y con eso te aconseja mejor, pero no las abre.

Conectarlo de verdad es trabajo de instalación.

## Licencia

Licencia MIT: úsalo, cámbialo y quédatelo. El texto completo está en `LICENSE`.

---

Hecho por Bluprint Agency - https://bluprintagency.com
