# Problemas

Las once fallas más comunes, con la solución en una línea. Si la tuya no está
aquí, escríbela en el canal **Preguntas** de la comunidad: así queda para el que
venga después.

---

**1. "No encuentro la terminal."**
No la necesitas. Abre la app de Claude, pestaña **Code**, elige **Local**, luego
**Seleccionar carpeta**, y selecciona la carpeta del kit.

**2. "Me pide pagar" o "no me aparece Claude Code."**
Claude Code necesita un plan de pago; el gratuito de Claude no lo incluye. Si
todavía no quieres pagar, prueba el kit con **Codex** (de OpenAI): funciona
incluso con la cuenta gratuita de ChatGPT, aunque el límite gratuito se agota
rápido. La ruta probada y la del video es la de Claude.

**3. "Escribo `/` y no me salen los comandos."**
Abriste la carpeta equivocada. Cierra y vuelve a abrir **la carpeta raíz
completa**, la que descomprimiste (`la-fabrica`, o el nombre que le hayas
puesto): nunca una subcarpeta como `contexto/`, y nunca tu carpeta de Documentos
entera.

**4. "Me pregunta si confío en la carpeta" o "me pide permiso por cada archivo."**
Di que sí a la pregunta de confianza: es tu carpeta y la acabas de descomprimir.
Ese "sí" es justo lo que enciende los permisos que dejan a tu asistente escribir
en tus archivos sin interrumpirte; **si no lo aceptaste, te va a pedir permiso a
cada rato**. Si después te pide algo distinto (borrar, mandar, instalar), lee qué
es antes de aceptar.

**5. "Cerré la ventana y perdí todo."**
No perdiste nada. Lo que ya contestaste está escrito en `contexto/`, archivo por
archivo, desde el momento en que lo contestaste. Vuelve a abrir la carpeta y
corre `/conoceme`: sigue donde quedó y solo te pregunta lo que falta.

**6. "Borré un archivo sin querer."**
Corre `/auditoria`: te dice exactamente cuál falta. Después corre `/conoceme`,
que rellena solo ese. Si prefieres, cópialo del ZIP original, que sigue en tus
descargas.

**7. "Estoy en Windows y uso OneDrive."**
Saca la carpeta de OneDrive (por ejemplo a `C:\la-fabrica`) o márcala como
**"Mantener siempre en este dispositivo"**. OneDrive descarga los archivos solo
cuando los abres, y tu asistente necesita que estén de verdad ahí. Instala
también Git for Windows.

**8. "El asistente se inventó un dato."**
Dile "eso no es cierto, corrígelo" y luego "recuerda esto" con el dato correcto.
Después abre `contexto/reglas.md` y agrega ahí lo que no debe hacer sin
preguntarte: ese archivo pesa más que su criterio.

**9. "No veo la carpeta `.claude`."**
Está oculta porque su nombre empieza con punto. No pasa nada: **copia siempre la
carpeta del kit entera**, nunca su contenido suelto, y lo oculto viaja con
ella.

**10. "¿Le puedo cambiar el nombre a la carpeta?"**
Sí. Ponle el nombre que le pusiste a tu asistente si quieres. Nada del kit
depende de que se llame `la-fabrica`. Eso sí: sin acentos, sin eñes y sin
espacios (usa guiones), porque en Windows y OneDrive esos nombres rompen la ruta
sin avisar.

**11. "¿Cómo actualizo?"**
Escribe `/actualizar`. Si te responde que el repositorio todavía no está abierto,
usa la ruta manual **"lo tuyo viaja"**: descomprime el kit nuevo, copia tus siete
cosas (`contexto/`, `memoria/`, `asistentes/`, `plantillas/`, `decisiones/`,
`informes/` y `conexiones.md`) del viejo al nuevo, y deja el viejo como respaldo.

---

Probado en Linux. La verificación en Windows y Mac está pendiente.
