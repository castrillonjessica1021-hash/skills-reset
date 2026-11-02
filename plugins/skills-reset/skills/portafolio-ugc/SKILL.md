---
name: portafolio-ugc
description: Arma el portafolio de una creadora UGC (contenido para marcas) y lo entrega listo para mandar a las marcas, en PDF, en imágenes o como página web con sus videos reproduciéndose. Son 6 partes, en el orden en que una marca lo mira (portada, por qué yo, mis videos, lo que hago, resultados y cómo trabajar conmigo), y cada parte le explica a la alumna qué va ahí y por qué. Úsalo cuando dice "hazme mi portafolio", "portafolio UGC", "quiero trabajar con marcas", "qué le mando a una marca", "media kit", "armemos mi portafolio", "quiero mi portafolio en página web", "portafolio web", o hace UGC y no tiene cómo mostrarlo. Funciona en el chat de Claude (panel al lado) y en Claude Code (se abre en el navegador).
---

# Portafolio UGC

> Antes de empezar, y cada vez que la alumna corrija: lee `biblioteca/criterio-y-correcciones.md` y síguelo.

Una marca no lee un portafolio de arriba abajo: lo mira por encima en menos de un minuto, buscando respuesta
a cuatro preguntas. **¿Qué haces? ¿Es bueno? ¿Encajas con mi marca? ¿Cómo te contrato?** Cada parte del
portafolio responde una de esas preguntas, y nada más. Corto, ordenado y con sentido: 5 o 6 partes.

## Las 6 partes (y qué pregunta responde cada una)

| # | Parte | Responde | Qué lleva |
|---|---|---|---|
| 1 | **Portada** | ¿Quién eres? | Su mejor foto, su nombre, "Creadora UGC", **una frase de lo que logra para las marcas** (no de ella) y 2 o 3 nichos |
| 2 | **Por qué yo** | ¿Encajas con mi marca? | 3 o 4 líneas: quién es, a quién le habla, qué la hace distinta. Y **lo que consigue la marca con ella**, en 3 puntos. Ciudad e idiomas si suman |
| 3 | **Mis videos** | ¿Es bueno lo que haces? | **Mínimo 6 videos, distintos entre sí**: ganchos, reseña a cámara, demostración o tutorial, unboxing, voz en off, testimonio. Cada uno con su nicho. Un QR o enlace para verlos completos, porque un PDF no reproduce videos |
| 4 | **Lo que hago** | ¿Qué me puedes entregar? | Los tipos de contenido que sabe hacer y lo que incluye: guion, ganchos, fotos, edición |
| 5 | **Resultados** | ¿Alguien más confió en ti? | **Solo si existen:** marcas con las que trabajó, lo que le dijeron (con permiso) y números reales. Si no tiene, esta parte no aparece |
| 6 | **Cómo trabajar conmigo** | ¿Cómo te contrato? | Los pasos, en cuánto entrega, cuántos cambios incluye, **los derechos de uso** (cuánto tiempo y si los anuncios se cobran aparte), su precio desde (si ya lo tiene) y su contacto bien visible |

## 1. Lo que se pregunta (una vez, todo junto)

Lee primero `mi-voz.md` y, si existe, `mi-portafolio.md`. Pregunta solo lo que falta, en un mensaje, con
sugerencias para que solo diga sí:

1. Su nombre como quiere que aparezca, su usuario y el correo donde le escriben las marcas.
2. **Sus nichos (2 o 3).** Pocos y claros venden más que "hago de todo". Si tiene videos en varios nichos,
   cada video lleva el suyo para que la marca encuentre el que le sirve.
3. A quién le habla y qué la hace distinta, para "por qué yo".
4. **Su frase de valor:** lo que logra para la marca, en una línea. Propónle una a partir de sus respuestas,
   por ejemplo: "Videos naturales, como los de una clienta real, para marcas de belleza que quieren vender sin
   que se note el anuncio."
5. Qué tipos de video sabe hacer.
6. **Sus videos:** cuántos tiene. Menos de 6 → dile cuáles le faltan para completar la variedad. Si todavía no
   ha trabajado con marcas, que grabe **videos de práctica** con productos de su casa y los marque como
   práctica: nunca hacer pasar uno de práctica por un trabajo pagado.
7. Dónde están sus videos completos (Drive, TikTok, Instagram, una página) para el QR.
8. **Solo si los tiene:** marcas, testimonios (con permiso), números, paquetes y precios.
9. Cuánto tarda en entregar, cuántos cambios incluye y qué derechos de uso da.

## 2. Armarlo

1. **Trae la plantilla más nueva.** Los estilos se mejoran seguido y la versión al día vive en la página
   de Jessica:
   - En Claude Code: `curl -fsSL https://jessicacastrillon.com/skills/portafolio.txt` (Windows: `curl.exe`).
   - En el chat de Claude: abre `https://jessicacastrillon.com/skills/portafolio.txt` con tu herramienta para
     leer páginas.
   Úsala solo si llegó completa: empieza con `<!doctype html>` y trae `/*DATOS*/` y `/*FIN*/`. Si no llegó, usa
   la copia de esta skill: `plantilla/portafolio.html`. No le digas nada a la alumna de este paso salvo que use la
   copia vieja. Reemplaza SOLO el bloque entre `/*DATOS*/` y `/*FIN*/`.
2. Sin marcas ni testimonios, deja esas listas vacías: la parte 5 no aparece. Sin precios, `paquetes` vacío.
   - `formato`: `horizontal` (como presentación o página web, para mandarlo por correo) o `vertical` (para verlo en
     el celular). Ella lo cambia arriba con un botón; el contenido, las fotos y los colores se mantienen.
   - `estilo`: `vino` (crema y vino, banda de cifras), `rosa` (rosa y café con letra a mano), `ios` (como las Notas
     del iPhone, tarjetas negras) o `editorial` (letras altas y una firma roja encima). Cada uno cambia la forma de
     las páginas, no solo los colores. Deja `colores` y `letras` en `null` para usar los del estilo, o pon los suyos.
   - `cifras` (seguidores, % de su audiencia, videos entregados) y `caso` (`{"marca","texto","n":[{"n","t"}]}`):
     **solo si son reales**. Vacío = no aparecen, y en la portada van sus nichos en su lugar.
   - `incluye` (lo que siempre entrega), `cta` (el botón de la portada) y `disponible` (la etiqueta de arriba).
3. Entrégalo como las otras skills de diseño: en el chat, como artefacto HTML; en Claude Code, guárdalo como
   `portafolio.html` en su carpeta y ábrelo en el navegador.
4. Explícale cómo se usa, en 4 líneas:
   - Arriba, **"Tu portafolio tiene"** le marca en verde lo que ya está y en rojo lo que falta (6 videos, nichos,
     foto, frase de valor, correo, enlace).
   - Debajo de cada página hay una nota amarilla que dice **qué va ahí y por qué**.
   - Toca los cuadros para poner sus fotos y videos (de cada video se toma un cuadro como portada), y toca
     cualquier texto para cambiarlo.
   - **⬇ Descargar PDF** cuando no quede nada en rojo.

## 2b. Si quiere su propio diseño

Si ninguno de los 4 estilos le gusta y manda referencias (capturas de Pinterest, Canva, otro portafolio):
1. Mira cada referencia y di en dos líneas qué tomas: la forma de las páginas (dónde va la foto, cómo se ven los
   videos, si hay banda de cifras), las letras y los colores. Nunca copies el nombre, las fotos ni los logos de otra.
2. Si una de las 4 ya se parece, empieza por esa y cambia solo `colores` y `letras`.
3. Si la forma es distinta, agrega un estilo nuevo en su copia de la plantilla: una entrada en `ESTILOS` (con sus
   colores y letras) y una en `R` con sus 6 páginas, siguiendo cómo están hechas las otras cuatro. Pon `estilo` con
   ese nombre. Aparece como un botón más en el panel, y el botón Vertical sigue funcionando con sus colores.

## 2c. Portafolio en página web (con sus videos en movimiento)

Si la alumna quiere su portafolio como página (o pregunta cuál le conviene: la página es la mejor opción para
mandarle un enlace a una marca, porque los videos se reproducen solos):

1. Usa `plantilla/portafolio-web.html`. Reemplaza SOLO el bloque entre `/*DATOS*/` y `/*FIN*/` con sus datos (los mismos
   que ya preguntaste en el paso 1). El ejemplo que trae es de Jessica: no dejes nada de ella.
2. **Sus videos:** por cada video, un recorte de 6 a 8 segundos, sin sonido, vertical, de unos 540 px de ancho (en
   Claude Code, con ffmpeg: `-ss <segundo> -t 7 -an -vf scale=540:-2 -crf 30`), y una portada `.jpg` del mismo video.
   Van en una carpeta `v/`. Sus fotos van en `img/` (`foto.jpg` arriba y `foto-2.jpg` en "Por qué yo").
3. `objetivos`: reparte sus videos según lo que busca la marca (que la conozcan, que confíen, que compren).
   `hago`: lo que de verdad entrega, cada uno con el número de un video de muestra que aparece al pasar el mouse.
4. **Solo lo real:** `marcas`, `resultados` y `paquetes` vacíos si no los tiene. Así esas secciones no aparecen.
   Cuando los tenga, se llenan y aparecen solas.
5. `colores` y `letras`: los suyos si tiene marca; si no, deja `null` (crema, rosa empolvado y café).
6. Ella prende o apaga secciones abriendo la página con `#editar` al final de la dirección.
7. **Publicarla gratis:** que entre a `app.netlify.com/drop`, cree su cuenta gratis y arrastre la carpeta completa
   (la página, `v/` e `img/`). Le da un enlace para mandarle a las marcas y ponerlo en su perfil. Explícaselo
   paso a paso, un paso a la vez.
8. Diseño: es editorial y limpio a propósito. No le agregues emojis, cajas ni tarjetas de colores: se ve hecho a mano
   por una diseñadora, no generado.

## 3. Reglas

- **Solo lo real.** Marcas con las que de verdad trabajó, testimonios que de verdad le dieron (con permiso),
  números que tiene. Nunca logos ni nombres de marcas con las que no ha trabajado.
- **Sus videos, no los de otras.** Verticales, con subtítulos, con su voz (no música con derechos que la
  marca no pueda usar en anuncios) y con un gancho en los primeros 2 segundos.
- **Calidad antes que cantidad:** sus 6 mejores, no todos los que tiene.
- **Corto:** 5 o 6 páginas, poco texto, mucha prueba.
- **Uno por marca, si puede:** antes de mandarlo, que ponga primero los videos del nicho de esa marca.

## 4. Guardar

Guarda lo que le preguntaste en `mi-portafolio.md` (nombre, nichos, frase de valor, tipos, marcas, paquetes,
derechos de uso, colores), para actualizarlo sin preguntar todo otra vez. Se entrega completo, como los otros
archivos suyos.
