---
name: conectar
description: Solo dentro del kit La FactorIA: no aplica fuera de esta carpeta. Investiga cómo conectar de verdad una herramienta del dueño (correo, WhatsApp, calendario, hoja de cálculo, lo que use) para un caso concreto, le propone dos o tres caminos con sus pros y contras, y escribe un plan autocontenido en planes/AAAA-MM-DD-<tema>.md con los pasos exactos y un prompt para pegar en una sesión nueva. No instala nada.
disable-model-invocation: true
---

# /conectar

El kit llega anotando herramientas, no abriéndolas. Este comando es el puente:
**averigua cómo se conectaría de verdad una de ellas, y deja el plan escrito.**

Lo que NO haces aquí es instalar, configurar ni pedir una clave. Terminas con un
archivo en `planes/`, no con una conexión funcionando. Eso es deliberado: elegir
mal la vía cuesta mucho más que investigarla, y el plan se ejecuta con calma en
otra sesión.

## Paso 1: qué herramienta, y sobre todo para qué

Dos preguntas, en un solo turno:

> ¿Qué herramienta quieres conectar? ¿Y qué quieres que yo haga con ella,
> concretamente? Por ejemplo: "leer los mensajes nuevos de WhatsApp y armarme el
> presupuesto", no "conectar WhatsApp".

**Sin el "para qué" no sigas.** No es una formalidad: "conectar el correo" tiene
media docena de vías buenas y todas distintas según si quieres leer, escribir,
buscar o archivar. Si te contesta solo con el nombre de la herramienta, vuelve a
preguntar una vez, con un ejemplo suyo sacado de `contexto/negocio.md`.

Lee también, con Read:

- `conexiones.md`, por si esa herramienta ya está anotada y con qué notas.
- `contexto/reglas.md`, porque ahí puede estar escrito qué no quiere que toques.
- `contexto/negocio.md`, para saber qué número mueve esto.

## Paso 2: investiga las vías reales

**Busca, no adivines.** Este es el paso donde un dato inventado le cuesta una
tarde: una integración que no existe, un producto que se descontinuó, un plan de
pago que ya no se vende.

Descarta lo que no aplique a su sistema (Windows, Mac o Linux) ni a lo que paga.
Si una vía necesita un plan de pago, dilo con el precio, no lo escondas.

**Si tu herramienta no puede buscar en internet**, dilo en una línea y pídele el
enlace de la documentación:

> No tengo búsqueda en esta sesión. Pásame el enlace de la documentación de
> <herramienta> y trabajo desde ahí.

Y sigue desde ese enlace. **Nunca de memoria.**

## Paso 3: propón dos o tres caminos

Uno solo no es una decisión, y cinco no se leen. Para cada camino, cuatro
líneas:

| | |
|---|---|
| **Qué es** | En una frase, sin jerga |
| **Qué pide** | Cuenta, plan de pago, instalar algo, tiempo |
| **A favor** | Lo que gana |
| **En contra** | Lo que le va a costar o lo que se le puede romper |

Di cuál recomiendas y por qué, en una línea. Después **espera a que elija**. No
escribas el plan antes de que conteste.

## Paso 4: escribe el plan

En `planes/AAAA-MM-DD-<tema>.md`, la misma carpeta donde van todos los planes del
dueño. El `<tema>` va **en minúsculas, sin acentos y sin eñe**, con guiones en vez
de espacios: la carpeta viaja a Windows y a
OneDrive, donde un acento en el nombre rompe la ruta sin avisar.

El plan tiene que poder ejecutarse **sin ti y sin esta conversación**:

```markdown
# <Herramienta>: <qué se quiere lograr>

**Fecha:** AAAA-MM-DD
**Para qué:** <el "para qué" del paso 1, con sus palabras>
**Qué número mueve:** <horas, respuestas, ventas, errores>

## Las vías que miré

<Las dos o tres del paso 3, en una línea cada una, con lo que las descarta.>

## La que elegimos, y por qué

<Una o dos frases.>

## Lo que hace falta antes de empezar

- <Cuentas, permisos, instalaciones, precios.>

## Los pasos

1. <Paso exacto.>
2. <...>

## Cómo sabrás que quedó bien

<La prueba concreta: "le pides X y te responde Y".>

## Prompt para pegar en una sesión nueva

> <El encargo completo, autocontenido, para que otro asistente lo ejecute sin
> haber leído esta conversación.>
```

## Paso 5: deja constancia

1. Actualiza la fila de esa herramienta en `conexiones.md` (o créala si no
   existe). Sigue en estado `anotado`: **este comando no conecta nada**. En las
   notas, la ruta al plan.
2. Agrega una línea al final de `decisiones/registro.md`, con el formato de ese
   archivo.

Y díselo en dos líneas: dónde quedó el plan y qué es lo siguiente que él tiene
que hacer.

## Las claves

La regla del kit dice que **nunca se escribe una clave en un archivo**, y aquí
sigue valiendo. Pero un plan que no puede decir dónde va la clave es un plan que
no se puede ejecutar, así que la excepción, acotada, es esta:

- Las claves y los tokens van a un archivo **`.env`** en la raíz de la carpeta,
  que el `.gitignore` del kit ya ignora.
- **Nunca al chat**, nunca a `contexto/`, nunca a `memoria/` y nunca a `planes/`.
- El plan **nombra** la clave que hará falta (`una clave de API de <servicio>`) y
  dice que va en `.env`. **No la pide ahora ni la escribe nunca.**

Si el dueño pega una clave en el chat, dile que la borre de ahí y que la ponga en
`.env` él mismo.

## Reglas

1. **No instales nada.** Ni una librería, ni una app, ni una extensión. El
   comando termina en un archivo de `planes/`.
2. **No sigas sin el "para qué".**
3. **No inventes una integración.** Si no la encontraste, dilo: "no encontré una
   vía oficial para esto".
4. **Un plan por corrida.** Si quiere conectar tres herramientas, son tres
   corridas.
5. **Muestra el plan antes de darlo por bueno.**
