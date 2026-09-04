# Cambios

Qué cambió en cada versión de La Fábrica. Lo más nuevo arriba. `/actualizar` te
muestra este archivo antes de tocar nada, para que sepas qué vas a recibir.

## Promesa de compatibilidad

Una versión menor (de 1.0.0 a 1.1.0) **nunca** te renombra ni te mueve una
carpeta. Si alguna vez hay que renombrar algo, eso es un cambio mayor (de 1.x a
2.0.0), viene con su propia habilidad que te migra, y como mucho pasa una vez al
año.

Tus siete cosas (`contexto/`, `memoria/`, `asistentes/`, `plantillas/`,
`decisiones/`, `informes/` y `conexiones.md`) no las toca ninguna versión.

---

## 1.1.0 (2026-09-04)

Cambia la forma de instalarlo y la forma de actualizarlo.

- **Se instala desde GitHub, sin descargar nada.** Creas una carpeta con el nombre
  que le quieras poner a tu asistente, la abres y le pegas un enlace. Los pasos
  están en el `README.md` nuevo.
- **Tu carpeta queda siendo un repositorio de git tuyo**, sin relación con el
  nuestro, listo para el día que quieras respaldar tu Fábrica en tu propio GitHub.
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
- Puedes ponerle a la carpeta el nombre que quieras: nada del kit depende de que
  se llame `la-fabrica`.
- La auditoría de cinco pilares con puntaje sobre 100 y tres huecos con su
  siguiente paso.
- `EMPIEZA-AQUI.md` y `PROBLEMAS.md` con las once fallas más comunes.
- Permisos pre-aprobados para que tu asistente escriba en tus carpetas sin
  interrumpirte a cada rato.

Probado en Linux con Claude. Funciona también con Codex, que lee el mapa de
`AGENTS.md`. La verificación en Windows y Mac está pendiente.
