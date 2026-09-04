# Problemas

Las fallas más comunes, con la solución en una línea. Si la tuya no está aquí,
escríbenos en el canal **Preguntas** de la comunidad y te contestamos ahí mismo.

---

**1. "No encuentro la terminal."**
No la necesitas. Abre la app de Claude, pestaña **Code**, elige **Local**, luego
**Seleccionar carpeta**, y selecciona la carpeta de tu asistente.

**2. "Me pide pagar" o "no me aparece Claude Code."**
Claude Code necesita un plan de pago; el gratuito de Claude no lo incluye. Si
todavía no quieres pagar, prueba el kit con **Codex** (de OpenAI): funciona
incluso con la cuenta gratuita de ChatGPT, aunque el límite gratuito se agota
rápido. La ruta probada y la del video es la de Claude.

**3. "Escribo `/` y no me salen los comandos."**
Casi siempre es una de dos. Si acabas de instalarlo, **cierra la carpeta y vuélvela
a abrir**: los comandos se cargan al abrir, no cuando aparecen los archivos. Si eso
no era, abriste la carpeta equivocada: tiene que ser **la carpeta raíz completa**,
la que creaste, nunca una subcarpeta como `contexto/` ni tu carpeta de Documentos
entera.

**4. "Me pregunta si confío en la carpeta" o "me pide permiso por cada archivo."**
Di que sí a la pregunta de confianza: es tu carpeta y la acabas de crear. Ese "sí"
es justo lo que enciende los permisos que dejan a tu asistente escribir en tus
archivos sin interrumpirte; **si no lo aceptaste, te va a pedir permiso a cada
rato**. Si después te pide algo distinto (borrar, mandar, instalar), lee qué es
antes de aceptar.

**5. "La instalación me dejó una carpeta dentro de la carpeta."**
Pasa si los archivos cayeron en una subcarpeta en vez de en la raíz. Dile: "mueve
todo lo que está dentro de esa subcarpeta a esta carpeta y borra la subcarpeta
vacía". Sabrás que quedó bien cuando veas `EMPIEZA-AQUI.md` al abrir la carpeta,
sin entrar a nada.

**6. "Cerré la ventana y perdí todo."**
No perdiste nada. Lo que ya contestaste está escrito en `contexto/`, archivo por
archivo, desde el momento en que lo contestaste. Vuelve a abrir la carpeta y
corre `/conoceme`: sigue donde quedó y solo te pregunta lo que falta.

**7. "Borré un archivo sin querer."**
Dile: "recupera el archivo que borré". Tu carpeta guarda su historial en git desde
que la instalaste, así que lo puede traer de vuelta. Si aun así no aparece, corre
`/auditoria` para saber cuál falta y después `/conoceme`, que rellena solo ese.

**8. "Estoy en Windows y uso OneDrive."**
Saca la carpeta de OneDrive (por ejemplo a `C:\Users\tunombre\luna`) o márcala como
**"Mantener siempre en este dispositivo"**. OneDrive descarga los archivos solo
cuando los abres, y tu asistente necesita que estén de verdad ahí. Instala también
Git for Windows.

**9. "El asistente se inventó un dato."**
Dile "eso no es cierto, corrígelo" y luego "recuerda esto" con el dato correcto.
Después abre `contexto/reglas.md` y agrega ahí lo que no debe hacer sin
preguntarte: ese archivo pesa más que su criterio.

**10. "No veo la carpeta `.claude`."**
Está oculta porque su nombre empieza con punto. No pasa nada: **copia siempre la
carpeta entera**, nunca su contenido suelto, y lo oculto viaja con ella.

**11. "¿Le puedo cambiar el nombre a la carpeta?"**
Sí, cuando quieras. Nada del kit depende de cómo se llame. Eso sí: sin acentos, sin
eñes y sin espacios (usa guiones), porque en Windows y OneDrive esos nombres rompen
la ruta sin avisar. Después de renombrarla, ábrela otra vez desde la app.

**12. "¿Cómo actualizo?"**
Escribe `/actualizar`. Trae la versión nueva desde GitHub y no toca nada de lo tuyo.
Si te dice que no pudo alcanzar GitHub, es tu conexión: inténtalo más tarde.

---

Probado en Linux. La verificación en Windows y Mac está pendiente.
