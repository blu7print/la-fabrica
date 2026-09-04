@AGENTS.md

@contexto/sobre-ti.md
@contexto/negocio.md
@contexto/voz.md
@contexto/reglas.md
@contexto/equipo.md
@conexiones.md
@memoria/MEMORIA.md

## Claude Code

Tres cosas que solo aplican aquí. Todo lo demás está en `AGENTS.md`, arriba.

### 1. "Recuerda esto" va a `memoria/`, nunca a tu memoria automática

Cuando el dueño diga "recuerda esto", guarda el hecho como un archivo de
`memoria/` siguiendo el formato de `AGENTS.md`. **No lo guardes con tu memoria
automática.** Esa escribe en `~/.claude/`, fuera de esta carpeta: el dueño no la
ve, no la puede corregir y no viaja con la carpeta cuando la copie a otra
computadora. Aquí la memoria son archivos que él abre y edita.

### 2. Para saber si un archivo de contexto está lleno, léelo con Read

Cada archivo de `contexto/` lleva su estado en la segunda línea, dentro de un
comentario HTML: `<!-- estado: plantilla -->` o `<!-- estado: completado
AAAA-MM-DD -->`. Los comentarios HTML **se eliminan del contexto que cargas al
abrir la carpeta**, así que arriba no los ves. La única forma de leer ese
marcador es abrir el archivo con la herramienta Read. Hazlo siempre antes de
decidir si una pregunta ya está contestada.

### 3. Se abre la carpeta raíz, nunca una subcarpeta

Los comandos (`/conoceme`, `/mi-voz`, `/auditoria` y los demás) viven en
`.claude/skills/` de la raíz. Si el dueño abrió `contexto/` o
`asistentes/algo/` como si fuera el proyecto, no va a tener ningún comando y
además este archivo no se carga. Si notas que falta todo eso, dile que cierre y
vuelva a abrir la carpeta raíz completa: la que descomprimió, que se llama
`la-fabrica` salvo que él le haya puesto otro nombre.

Para usar un asistente de `asistentes/`, él sigue en la raíz y te dice "trabaja
como el asistente de `asistentes/<nombre>/`".
