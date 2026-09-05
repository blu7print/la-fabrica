# Cambios

Qué cambió en cada versión de La FactorIA. Lo más nuevo arriba. `/actualizar` te
muestra este archivo antes de tocar nada, para que sepas qué vas a recibir.

## Promesa de compatibilidad

Una versión menor (de 1.0.0 a 1.1.0) **nunca** te renombra ni te mueve una
carpeta. Si alguna vez hay que renombrar algo, eso es un cambio mayor (de 1.x a
2.0.0), viene con su propia habilidad que te migra, y como mucho pasa una vez al
año.

Tus ocho cosas (`contexto/`, `memoria/`, `asistentes/`, `plantillas/`,
`decisiones/`, `informes/`, `planes/` y `conexiones.md`) no las toca ninguna
versión.

---

## 2.0.0 (2026-09-04)

Cambia el nombre, la forma de instalarlo, y trae un comando nuevo.

- **Ahora se llama La FactorIA.** El mismo kit, el mismo sitio, el mismo enlace:
  solo cambia el nombre con el que lo ves. Tu carpeta y tus archivos no cambian.
- **`/conectar`, el octavo comando.** Le dices qué herramienta usas y para qué,
  investiga las vías reales, te propone dos o tres caminos y te deja el plan
  escrito en la carpeta nueva `planes/`. No instala nada: el plan queda listo para
  ejecutarlo cuando quieras.
- **`planes/`, una carpeta nueva tuya.** Es donde viven tus planes: los que
  escribe `/conectar` y cualquier otro que le pidas ("hazme un plan para contratar
  a alguien"). Como el resto de lo tuyo, ninguna actualización la toca.
- **La instalación es la misma en Windows, Mac y Linux.** Antes bajaba un
  comprimido y había que elegir los comandos según el sistema; ahora es git, una
  sola receta, y tu carpeta es tu repositorio desde el primer segundo. Las
  instrucciones viven en un archivo `INSTALAR.md` que se borra solo al terminar.
- **`/actualizar` arreglado.** Su descripción decía una cosa y su procedimiento
  otra. Ahora nombra uno por uno los archivos que reemplaza, así que no hay forma
  de que pise lo que tú escribiste, y borra de verdad las habilidades que
  retiramos.

**Este cambio mayor no te renombra ni te mueve nada.** Solo agrega `planes/`. Por
eso no viene con una habilidad que te migre: no hay nada que migrar. Tu contexto,
tu memoria, tus asistentes, tus plantillas, tus decisiones, tus informes y tus
conexiones se quedan exactamente donde están.

---

## 1.1.0 (2026-09-04)

Cambia la forma de instalarlo y la forma de actualizarlo.

- **Se instala desde GitHub, sin descargar nada.** Creas una carpeta con el nombre
  que le quieras poner a tu asistente, la abres y le pegas un enlace. Los pasos
  están en el `README.md` nuevo.
- **Tu carpeta queda siendo un repositorio de git tuyo**, sin relación con el
  nuestro, listo para el día que quieras respaldar tu FactorIA en tu propio GitHub.
- **`/actualizar` ya funciona de verdad.** Trae la versión nueva desde GitHub,
  guarda antes el estado en el que está tu carpeta y lo deja todo en un punto al que
  puedes volver diciendo "deshaz la actualización". Se acabó la ruta manual de mover
  carpetas a mano.
- **`README.md` nuevo**: qué es esto, qué necesitas y cómo se instala.
  `EMPIEZA-AQUI.md` se queda con lo de adentro: los comandos, la memoria, la
  actualización y los problemas.
- **`/conoceme` te propone el nombre de la carpeta.** Si la llamaste `luna`, te
  pregunta si te llama Luna en vez de preguntar en frío.
- Textos revisados de punta a punta para que digan qué hace cada cosa, sin promesas.

---

## 1.0.0 (2026-09-03)

La primera. Incluye:

- Las siete habilidades: `/conoceme`, `/arranca`, `/mi-voz`, `/fabrica`,
  `/auditoria`, `/siguiente-nivel` y `/actualizar`.
- La entrevista de siete preguntas que llena tu contexto sin que escribas
  archivos a mano, y que arranca preguntándote cómo quieres llamar a tu
  asistente.
- Puedes ponerle a la carpeta el nombre que quieras: nada del kit depende de cómo
  se llame la carpeta.
- La auditoría de cinco pilares con puntaje sobre 100 y tres huecos con su
  siguiente paso.
- `EMPIEZA-AQUI.md` y `PROBLEMAS.md` con las once fallas más comunes.
- Permisos pre-aprobados para que tu asistente escriba en tus carpetas sin
  interrumpirte a cada rato.

Probado en Linux con Claude. Funciona también con Codex, que lee el mapa de
`AGENTS.md`.
