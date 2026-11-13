---
name: que-me-funciona
description: Lee los números de las piezas que la alumna ya publicó y le dice qué le está funcionando a ELLA, medido contra su propia mediana. Úsalo cuando dice "qué me funciona", "analiza mis reels", "por qué no me ven", "mira mis números", "qué repito", "saca mi mediana", o pega una lista o una captura de sus estadísticas. Entrega una lectura con evidencia y qué hacer la próxima semana, no un guion ni un calendario. Para armar la semana después, está `planificar-contenido`.
---

# Qué me funciona

> **Lo primero, siempre:** busca `mi-voz.md`. En el chat normal de Claude está en los archivos de su Proyecto (o en lo que adjuntó). Si puedes ver su computador (Claude Code o Génesis Estudio), está en su carpeta `Documentos/Mi contenido/` (o `OneDrive/Documentos/Mi contenido/`). Si no está en ningún lado, primero se hace su voz con la skill `mi-voz`.

> **Antes de escribir, y cada vez que la alumna corrija:** lee `biblioteca/criterio-y-correcciones.md`
> y síguelo.

La alumna no necesita saber qué funciona "en Instagram". Necesita saber qué le funciona a ella.
Eso sale de sus números, no de las cuentas que admira.

## 0. Antes de nada

Lee `mi-voz.md` y `mis-piezas.md` si existen. Lee `biblioteca/medicion.md`: todo lo que se
calcula y se concluye aquí sigue esa hoja.

## 1. Consigue los datos

Mira primero qué tiene conectado en su Claude. Usa la ruta más completa que esté disponible y
dile en una línea cuál vas a usar. Esta skill solo lee **su propia cuenta**.

**Ruta A · Tiene Windsor conectado (su Instagram por dentro).** Trae sus publicaciones de los
últimos 60 a 90 días con: fecha, tipo de pieza, vistas o reproducciones, alcance, guardados,
compartidos y comentarios. Antes de pedir datos, consulta qué campos existen en su conexión y usa
esos nombres; no los adivines. Si hay un dato de retención o de tiempo de visualización, tráelo.

**Ruta B · Tiene Apify conectado (lo público).** Trae los reels de su usuario (está en
`mi-voz.md`; si no, pregúntalo): fecha, vistas, likes, comentarios, duración, el caption y, si la
herramienta lo da, lo que dice el video. Máximo los últimos 90 días o 30 piezas. Antes de
correrlo, dile cuántas piezas vas a traer. Lo público no incluye guardados, compartidos ni
cuánta gente se va al inicio: si hacen falta, pídele una captura.

**Ruta C · No tiene nada conectado.** Ella los trae, como le quede más fácil:

- Una captura de sus estadísticas, o varias.
- Una lista pegada: una pieza por línea, con la fecha, el formato y las vistas.

Si tiene las dos conexiones, usa A para los números y B para saber cómo empieza cada reel.

Lo mínimo por pieza, venga de donde venga: **formato** (reel hablado, reel de texto, carrusel) y
**vistas**. Si no se puede saber el formato por los datos, pregúntaselo: mezclar formatos daña
la mediana.

Si una herramienta falla o no trae nada, dilo y pasa a la siguiente ruta. Si una captura no se
lee bien, pídele ese número. Nunca se estima ni se rellena un dato.

## 2. Según cuántas piezas tenga

- **Ocho o más de un mismo formato:** lectura completa (pasos 3 a 6).
- **Entre tres y siete:** lectura de inicio. Calcula la mediana, pero di que es provisional y
  que cada hallazgo es una hipótesis.
- **Menos de tres, o está empezando:** no hay nada que leer todavía. Dile eso sin rodeos,
  proponle un mes de experimentos pequeños (ver el final de `medicion.md`) y mándala a
  `planificar-contenido`.

## 3. Saca su mediana

Una por formato. Nunca mezcles reels hablados con reels de texto o carruseles. Muéstrale el
número y cómo salió, en una línea.

## 4. Mide cada pieza contra su mediana

Anota cada una como múltiplo: 0,6 · 1,2 · 2,0. Sepáralas en tres grupos: las que doblaron la
mediana o más, las del medio, y las que quedaron por debajo de 0,75.

Si la pieza era para vender o para que le respondan, no la juzgues solo por vistas: mira lo que
dice la tabla "cada pieza por su trabajo" de `medicion.md`.

## 5. Busca qué tienen en común las de arriba

Compara las de arriba con las de abajo. Mira una cosa a la vez:

- El formato.
- El tema.
- Cómo empiezan (la familia de entrada, ver `biblioteca/banco-de-entradas.md`).
- La duración.
- Si enseñan algo o cuentan algo.
- Desde dónde habla: como experta o aprendiendo.

Algo cuenta como hallazgo solo si se repite **en dos piezas o más**. Lo que pasó una vez es una
hipótesis, y se dice con esa palabra.

## 6. Qué entregar

1. **Su mediana**, por formato.
2. **Una tabla corta:** sus tres piezas más altas y las tres más bajas, con su múltiplo.
3. **Tres hallazgos**, cada uno con las piezas que lo sostienen. Si solo hay dos sólidos, dos.
4. **Su 70, 20, 10** armado con sus piezas: qué repetir, qué repetir cambiando una cosa, qué
   probar.
5. **Una sola cosa para cambiar esta semana.**
6. **Su `mi-voz.md` completo**, con "Mis números" ya lleno y lo demás tal como estaba, listo
   para reemplazar el de su proyecto.

## Memoria: antes y después

Lee `biblioteca/memoria.md` y síguelo. Si tiene `mis-piezas.md`, llena tú la columna
"Resultado" con los múltiplos y devuélvele el archivo completo. El siguiente paso es `planificar-contenido`.

## Qué evitar siempre

- Concluir algo de un solo video.
- Compararla con cuentas grandes.
- Decirle que su cuenta "está dañada" o que abra otra.
- Recomendarle publicar más como solución.
- Inventar un número que no se leía en la captura.
