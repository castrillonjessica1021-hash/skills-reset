---
name: disena-historias
description: Diseña una secuencia de Historias de Instagram ya escrita y la entrega en imágenes listas para subir (1080 × 1920), con los colores, las letras y las fotos de la alumna, y el espacio marcado para cada sticker (encuesta, caja de preguntas, enlace). Usa su propio diseño si sube referencias, o los 5 estilos base (amiga cercana, cajas de color, frase resaltada, collage de pruebas, producto o recurso). Úsalo cuando dice "diséñame las historias", "ponlas bonitas", "hazme las historias en imágenes", "quiero las historias listas para subir", "usa mi estilo de historias", o justo después de que la skill `secuencias-de-historias` entrega el texto. Funciona en el chat de Claude (panel al lado) y en Claude Code (se abre en el navegador). No escribe la secuencia desde cero: si no hay texto, primero va `secuencias-de-historias`.
---

# Diseña historias

> Antes de empezar, y cada vez que la alumna corrija: lee `biblioteca/criterio-y-correcciones.md` y síguelo.
> Una sola versión, revisada, y las correcciones se responden con criterio.

Esta skill hace la segunda mitad de las historias: **el diseño**. El texto ya viene escrito por la skill
`secuencias-de-historias` (portada, desarrollo, prueba si hay, un solo pedido al final). Aquí se convierte en
imágenes que ella descarga y sube.

## 0. Lo que se lee primero

1. **El texto de la secuencia.** Si en la conversación no hay una secuencia escrita, no la inventes: corre
   primero `secuencias-de-historias` y vuelve aquí con su texto.
2. **Su marca.** En este orden: `mi-estilo-historias.md` (si existe, ahí está todo), `mi-estilo-carrusel.md`
   (mismos colores y letras), su manual de marca o `mi-kit-de-estilo`, y `mi-voz.md`. Si no hay colores ni
   letras guardados, pregúntalos UNA vez, juntos, con sugerencias para que solo diga sí:
   - 4 colores: fondo claro, color de texto, color de las cajas (su color fuerte) y un color de resalte.
   - Letras: una para las frases (serif, como de revista), una para el texto, una para títulos y una a mano.
   Guarda la respuesta en `mi-estilo-historias.md` (formato abajo).
3. **Su usuario de Instagram**, para la firma de la última historia.

## 1. Qué diseño usar: el suyo o los 5

**Siempre, al empezar cada secuencia, pregúntale primero esto** (un solo mensaje, corto):

> ¿Tienes una referencia visual para estas historias? Puedes subir capturas de historias que te gusten (tuyas
> o de otras cuentas). Si no, usamos mis 5 estilos.

Si ya tiene `mi-estilo-historias.md`, la pregunta incluye esa opción: "¿usamos tu estilo guardado, subes una
referencia nueva, o usamos los 5 estilos?". Nunca empieces a diseñar sin esta respuesta.

**Si sube referencias:**
1. Estudia cada captura. Anota solo la **forma**: dónde va el texto y de qué tamaño, si va en cajas, resaltado
   o suelto, qué letra (serif, gruesa, a mano), cómo pega capturas, cómo cierra.
2. Elige el estilo base de `estilos.md` que más se parece para cada tipo de historia, y escribe lo que la
   acerca a sus referencias en `css_extra` (tamaños, márgenes, bordes, sombras). Nunca copies colores,
   fotos, textos ni logos de la referencia.
3. Guárdalo en `mi-estilo-historias.md` con una línea de qué tomaste de cada referencia, y dile en una frase
   qué viste ("tus referencias ponen cada frase en una caja vino con letra de revista").

**Si no tiene referencia:** usa los 5 estilos y elige tú el de cada historia según su función (abajo). Ella
lo puede cambiar en la página con el menú de cada historia.

## 2. Qué estilo va en cada historia

| Función en la secuencia | Estilo que mejor funciona |
|---|---|
| Portada (siempre la 1) | `amiga` o `resaltada`, con foto suya y un sticker de interacción |
| Contexto o desarrollo | `cajas` (frases cortas, una por caja) o `resaltada` |
| Prueba o testimonios | `collage` (capturas pegadas) o `cajas` con una captura |
| Interpretación ("lo que esto significa") | `cajas` |
| Pedido final | `recurso` si regala o vende algo; `cajas` con `cta` si solo pide responder |

Mezclar estilos dentro de una secuencia está bien y es lo normal. Que no haya más de 3 estilos distintos.

## 3. Armar las historias

1. **Trae la plantilla más nueva.** La versión al día vive en la página de Jessica:
   - En Claude Code: `curl -fsSL https://jessicacastrillon.com/skills/historias.txt` (Windows: `curl.exe`).
   - En el chat de Claude: abre `https://jessicacastrillon.com/skills/historias.txt` con tu herramienta para
     leer páginas.
   Úsala solo si llegó completa: empieza con `<!doctype html>` y trae `/*DATOS*/` y `/*FIN*/`. Si no llegó,
   usa la copia de esta skill: `plantilla/historias.html`.
2. Reemplaza SOLO el bloque entre `/*DATOS*/` y `/*FIN*/` con el JSON de la secuencia (formato abajo).
3. Entrégalo:
   - **En el chat de Claude:** como un artefacto HTML (el archivo completo), para que se abra en el panel.
   - **En Claude Code:** guárdalo como `historias.html` en la carpeta de esa secuencia (por ejemplo
     `Mi contenido/Historias/<tema>/`) y ábrelo en su navegador. En Windows: `start "" "historias.html"`.
     En Mac: `open historias.html`.
4. Dile en 4 líneas cómo se usa:
   - Toca **📷 Foto** para poner su foto, y **🖼 Capturas** o el hueco punteado para pegar pruebas.
   - Toca **✨ Elementos** para ponerle lo que quiera, como en Canva: todos los emojis, formas (recuadros, círculos, manchas, estrellas), flechas, textos (globos, burbujas de chat, post-it, etiquetas, nota a mano) y mockups (celular, laptop, polaroid, post de Instagram, ventana, foto en círculo) con su foto o captura adentro. Se arrastran y, abajo de la slide, se agrandan, se giran, se pintan, se les cambia la opacidad, se les pone sombra y se pasan al frente o atrás.
   - Toca cualquier texto para corregirlo. **↕ Texto** si le tapa la cara. El menú cambia el estilo.
   - Los **cuadros punteados son el espacio del sticker**: no salen en la imagen. Debajo de cada historia
     dice qué sticker poner en Instagram y con qué texto.
   - **⬇ Descargar todas** baja las imágenes y una lista de stickers. Si una historia es un video,
     **⬇ Solo el texto** le da el diseño transparente para ponerlo encima del video.

### El JSON de `DATA`

```json
{
  "marca": {"usuario": "@suusuario",
    "colores": {"fondo": "#F4EFE6", "tinta": "#141414", "acento": "#B00B00", "resalte": "#F4C70F"},
    "letras": {"titulo": "Anton", "serif": "Playfair Display", "cuerpo": "Inter Tight", "mano": "Caveat"}},
  "css_extra": "",
  "historias": [ ... ]
}
```

Cada historia:

| campo | qué es |
|---|---|
| `estilo` | `amiga` · `cajas` · `resaltada` · `collage` · `recurso` |
| `lineas` | las frases, una por renglón o caja. La palabra clave entre asteriscos: `"Eso es *criterio.*"` |
| `foto` | `true` (ella la pone), `false` (fondo de color) o la ruta/imagen si ya la tienes |
| `pos` | `arriba`, `centro` o `abajo`: dónde va el texto |
| `sticker` | `{"tipo": "encuesta", "texto": "¿Tú editas tus videos?", "opciones": ["Sí", "Me cuesta"]}`. Tipos: `encuesta`, `preguntas`, `enlace`, `deslizador`, `cuestionario`, `mencion` |
| `capturas` | cuántos huecos para pruebas (1 a 4); `capturas_textos`: etiqueta a mano de cada una |
| `titulo` | solo en `collage`: el título grande |
| `nota` | una tarjetita blanca (en `amiga`) o una línea a mano (en `resaltada`) |
| `recurso` | `true` en `recurso`: hueco para la portada del producto o la guía |
| `cta` + `palabra` | el pedido: `"cta": "Responde", "palabra": "INFO"` |
| `firma` | `true` para poner su usuario (solo en la última) |

`css_extra` (opcional): las reglas de CSS sacadas de sus referencias. La plantilla las aplica sola.
Cada estilo tiene su clase (`.st-amiga`, `.st-cajas`, `.st-resaltada`, `.st-collage`, `.st-recurso`) y
sus partes (`.ln` frases, `.cta` pedido, `.tarjeta` nota, `.slot` capturas, `.tit` título).

## 4. Reglas que no se rompen

- **La primera historia siempre es una foto suya** con una interacción (encuesta, pregunta o deslizador).
  Nunca una historia de solo texto para abrir.
- **El texto nunca tapa la cara.** Antes de elegir `pos`, piensa dónde estará su cara en la foto. Si viste la
  foto en el chat, decide tú; si no, recuérdale el botón **↕ Texto**.
- **Las zonas de Instagram quedan libres:** arriba está la barra con su nombre y abajo la de mensajes. La
  plantilla ya deja ese margen; no pongas nada importante fuera de él con `css_extra`.
- **Secuencias cortas:** de 4 a 7 historias. Una idea por historia, frases de 12 palabras como mucho.
- **Un solo pedido**, en la última. Las de en medio pueden tener sticker de interacción, no de venta.
- **Fotos reales de ella o de su trabajo.** Nunca fotos de stock ni generadas. Las pruebas son capturas reales
  (mensajes, resultados, testimonios con permiso).
- **Solo datos reales.** Números, precios y testimonios solo si ella los dio.
- **Su marca manda.** Sus colores y letras siempre, aunque la referencia use otros.

## 5. Correcciones

Ella corrige por número ("en la 3 cambia...", "la 5 sin sticker"). Se hacen todas juntas en una sola versión
nueva. Lo que puede hacer ella sola en la página (texto, foto, posición, estilo) se lo recuerdas en vez de
regenerar.

## `mi-estilo-historias.md` (formato)

```markdown
# Mi estilo de historias
Actualizado: <fecha>
Usuario: @suusuario
Colores: fondo #..., texto #..., cajas #..., resalte #...
Letras: frases <letra> · texto <letra> · títulos <letra> · a mano <letra>
Estilos que más uso: portada <estilo> · desarrollo <estilo> · cierre <estilo>
Lo que tomé de mis referencias: <una línea por referencia>
css_extra: <el CSS, si hay>
```

**Elementos (opcional en el JSON):** cada slide o historia puede traer `"elementos": [{"k": "emoji"|"forma"|"texto"|"mock", "v": ..., "x": 540, "y": 700, "s": 1, "r": 0, "c": "acento", "o": 1, "sh": false, "t": "texto si lleva"}]`. Formas y flechas por nombre (rectángulo, redondeado, círculo, píldora, mancha, estrella, corazón, círculo a mano, subrayado, check, flecha curva, flecha a mano…); textos: globo, pensamiento, chat yo, chat otro, etiqueta, post-it, nota a mano, titular, caja de texto; mockups: celular, laptop, polaroid, post, ventana, foto círculo, foto. Pon alguno solo si ayuda a leer la slide (una flecha a la palabra clave, un círculo a un número); lo demás lo pone ella.
