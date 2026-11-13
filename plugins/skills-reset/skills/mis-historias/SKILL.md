---
name: mis-historias
description: Entrevista corta y periódica que le saca a la alumna historias reales de su vida, su trabajo y sus clientas, y las guarda en su archivo `mis-historias.md` para que las demás skills escriban con material suyo y nunca con ejemplos inventados. Úsalo cuando dice "entrevístame", "sácame historias", "no sé de qué hablar", "no tengo ideas", "mi entrevista de la semana", "qué me pasó esta semana que sirva", o cuando otra skill necesita una historia y no la encuentra. Entrega su archivo de historias completo y actualizado, y las ideas que salen de ahí, no un guion.
---

# Mis historias

> **Lo primero, siempre:** busca `mi-voz.md`. En el chat normal de Claude está en los archivos de su Proyecto (o en lo que adjuntó). Si puedes ver su computador (Claude Code o Génesis Estudio), está en su carpeta `Documentos/Mi contenido/` (o `OneDrive/Documentos/Mi contenido/`). Si no está en ningún lado, primero se hace su voz con la skill `mi-voz`.

> **Antes de escribir, y cada vez que la alumna corrija:** lee `biblioteca/criterio-y-correcciones.md`
> y síguelo.

La IA puede escribir, pero no vivió la vida de la alumna. Eso es lo único que no se copia. Esta
skill se encarga de que ese material no se pierda: cada semana le saca dos o tres historias
reales y las guarda, para que sus guiones, carruseles e historias salgan de su vida y no de
ejemplos genéricos.

`mi-voz.md` dice **cómo habla**. `mis-historias.md` guarda **lo que le ha pasado**. Son
archivos distintos y los dos viven en su proyecto.

**La regla que manda:** nada se inventa ni se adorna. Cada historia queda con sus palabras. Si
falta un detalle, se pregunta; si no lo recuerda, se queda sin ese detalle.

## 0. Antes de nada

- Lee `mi-voz.md` (si no está, usa `mi-voz-TEMPLATE.md`, que viene dentro de esta skill).
- Lee `mis-historias.md` si existe: lo que ya está guardado no se vuelve a preguntar, y te dice
  qué tipo de historias le faltan.
- Lee `mis-piezas.md` si existe: así sabes de qué temas ya habló y qué le está funcionando.

Dile en dos líneas cuántas historias tiene guardadas y qué tipo le falta. Así ve que no empieza
de cero.

## 0.5 La primera vez: tu banco de base

Si `mis-historias.md` tiene menos de cinco historias, la primera entrevista arma la base, en
varios mensajes, sin apuro:

1. **Tu origen, la versión real.** No la del perfil profesional. ¿Cómo empezó de verdad, con lo
   desordenado incluido?
2. **De 3 a 5 tropiezos.** Lo que salió mal. Dan más confianza que los logros.
3. **De 3 a 5 logros**, tuyos o de clientas, con el número exacto y cuándo. Nunca redondeado.
4. **El momento en que cambió tu forma de pensar.** "Antes pensaba ___, pasó ___, ahora pienso ___."
5. **Tu vida de antes.** Un trabajo, una etapa, un lugar, que te hace ver tu tema distinto que las
   demás.
6. **Lo que estás viviendo ahora** y todavía no sabes cómo termina. Esta es la que se vuelve trama
   (ver `planificar-contenido`).

Se hacen dos o tres por mensaje y se guardan con el mismo formato de siempre.

## 1. La entrevista de la semana

Corta. **Un bloque por mensaje, máximo tres preguntas**, y esperas la respuesta. Que pueda
contestar por audio o dictando, sin corregirse: eso ya es material.

Escoge **dos o tres** de estas puertas, empezando por las que menos historias tiene guardadas.
No hagas todas en una sola semana.

1. **Esta semana.** ¿Qué pasó esta semana en tu trabajo que te hizo pensar "esto lo tengo que
   contar"? ¿Qué te molestó, qué te sorprendió, qué te salió bien?
2. **Una clienta.** ¿Qué te dijo o te escribió una clienta (sin nombre)? ¿Qué le estaba pasando
   cuando llegó y qué cambió?
3. **Un error.** ¿Qué hiciste mal en tu negocio y qué aprendiste? ¿Qué harías distinto hoy?
4. **Una decisión.** ¿Qué decidiste que te costó? ¿Qué dejaste de hacer?
5. **Una opinión que cambió.** ¿Qué creías hace un año sobre tu oficio que ya no crees?
6. **El principio.** ¿Por qué empezaste? ¿Cuál fue el primer cliente, el primer peso, el primer
   "no"?
7. **Tu vida.** Algo de tu casa, tu familia, tu fe, tus rutinas, que tenga que ver con cómo
   trabajas. Solo lo que quiera contar.
8. **Lo que nadie ve.** Algo del detrás de tu trabajo que tus clientas no se imaginan.

Cuando cuente algo, saca los detalles con **una** pregunta corta cada vez, no con un
cuestionario:
- ¿Cuándo fue y dónde estabas?
- ¿Qué dijiste o qué te dijeron, con las palabras exactas?
- ¿Qué había ahí (un objeto, una hora, un número)?
- ¿Qué cambió después?

Si dice "no me acuerdo" o "no sé", no insistas más de una vez.

## 2. Pregunta qué se puede contar

Antes de guardar cada historia, pregunta una sola vez: "¿Esto lo puedo usar en tu contenido, con
cuidado, o es solo para que yo te conozca?" Guarda la respuesta. Nada marcado como privado se
usa en una pieza, nunca. Nada con nombre o datos de una clienta se guarda: solo sus palabras, sin
quién las dijo.

## 3. Cómo se guarda cada historia

Cada historia en `mis-historias.md` va así:

```
### <título corto, con sus palabras>
- **Tipo:** origen / tropiezo / logro / cambio de idea / vida de antes / en curso / de la semana
- **Cuándo:** <fecha o época>
- **Qué pasó:** <dos a cinco líneas, con sus palabras>
- **El detalle:** <el objeto, la hora, la frase textual, el número>
- **Qué cambió:** <lo que aprendió o lo que pasó después>
- **Sirve para:** <tema o temas de su mi-voz> · <objetivo: alcance, interacción, conexión, autoridad o venta>
- **Se puede usar:** sí / con cuidado / privada
- **Usada en:** <fecha y pieza, o "todavía no">
```

Y para las de tipo **en curso**, una línea más:

```
- **Próximo capítulo:** <qué tiene que pasar para contar lo siguiente, y más o menos cuándo>
```

Si el archivo no existe, créalo con este encabezado:

```
# Mis historias

Lo que me ha pasado, con mis palabras. Las skills lo leen antes de escribir.
Nada de aquí se inventa ni se adorna.
```

## 4. Qué entregar

1. **Las historias nuevas**, ya escritas con el formato de arriba, para que ella las revise.
   Pregúntale una vez: "¿Algo de esto no lo dirías así?" Lo que señale se cambia.
2. **De dos a cuatro ideas de contenido** que salen de esas historias. Cada una en una frase,
   con la historia que la sostiene y el formato que le conviene (reel hablado, carrusel o
   historias). Si alguna se parece a algo que ya le funcionó en `mis-piezas.md`, dilo.
3. **Su `mis-historias.md` completo y actualizado**, siguiendo `biblioteca/memoria.md`: todo lo
   que ya tenía, sin quitar ni resumir nada, más lo nuevo. Y la línea de siempre: "Descarga este
   archivo y reemplaza el `mis-historias.md` de tu proyecto."

## 5. Cuando una skill usa una historia

Cuando otra skill escriba una pieza con una historia de aquí, en "Usada en" se anota la fecha y
la pieza. Así no se cuenta la misma historia dos semanas seguidas. Una historia buena se puede
volver a contar más adelante, desde otro ángulo.

## Y qué sigue

Para decidir cuál de las ideas grabar primero: `director`. Si ya sabe cuál: `estructura-de-contenido`.

## Qué evitar siempre

- Hacer una entrevista larga. Dos o tres puertas por semana.
- Mejorar la historia: hacerla más dramática, más redonda o con una moraleja que ella no dijo.
- Usar algo que marcó como privado.
- Guardar nombres o datos de clientas.
- Convertir cada historia en una clase. Hay historias que solo sirven para conectar, y está bien.
