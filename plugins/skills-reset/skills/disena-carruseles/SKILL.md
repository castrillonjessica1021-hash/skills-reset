---
name: disena-carruseles
description: Diseña un carrusel de Instagram ya escrito y lo entrega en imágenes listas para subir (1080 × 1350), con los colores, las letras y las fotos de la alumna. Usa su propio diseño si sube referencias o plantilla, o uno de los 8 estilos base (editorial, revista, cuaderno, foto oscura, collage, oferta, mi día, aesthetic). Úsalo cuando dice "diséñame el carrusel", "ponlo bonito", "hazlo en imágenes", "quiero el carrusel listo para subir", "usa mi diseño", "este es mi estilo", o justo después de que la skill `carruseles` entrega el texto. Funciona en el chat de Claude (panel al lado) y en Claude Code (se abre en el navegador). No escribe el carrusel desde cero: si no hay texto, primero va `carruseles`.
---

# Diseña carruseles

> Antes de empezar, y cada vez que la alumna corrija: lee `biblioteca/criterio-y-correcciones.md` y síguelo.
> Una sola versión, revisada, y las correcciones se responden con criterio.

Esta skill hace la segunda mitad del carrusel: **el diseño**. El texto ya viene escrito por la skill
`carruseles` (dos ganchos, una idea por slide, un solo pedido al final). Aquí se convierte en imágenes que
ella descarga y sube.

## 0. Lo que se lee primero

1. **El texto del carrusel.** Si en la conversación no hay un carrusel escrito, no lo inventes: corre primero
   la skill `carruseles` y vuelve aquí con su texto.
2. **Su marca.** Busca, en este orden: `mi-estilo-carrusel.md` (si ya existe, ahí está todo), su manual de
   marca o `mi-kit-de-estilo` (colores y letras), y `mi-voz.md`. Si no hay colores ni letras guardados,
   pregúntalos UNA vez, juntos, con sugerencias para que solo diga sí:
   - 3 colores: fondo claro, color de texto, color de acento (y si quiere, un color de resalte).
   - 2 o 3 letras: una para titulares, una para el texto, y si quiere una manuscrita.
   Guarda la respuesta en `mi-estilo-carrusel.md` (formato abajo) para no volver a preguntar.
3. **Su usuario de Instagram**, para la firma de cada slide (está en `mi-voz.md` o se pregunta).

## 1. Qué diseño usar: el suyo o uno de los 8

**Siempre, al empezar cada carrusel, pregúntale primero esto** (en un solo mensaje, corto):

> ¿Tienes una referencia visual para este carrusel? Puedes subir capturas o pegar links de carruseles que te
> gusten (Instagram o Pinterest), o tu propia plantilla. Si no, elegimos uno de mis 8 estilos.

Si ya tiene `mi-estilo-carrusel.md` guardado, la pregunta incluye esa opción: "¿usamos tu estilo guardado
(<nombre>), subes una referencia nueva, o elegimos de la lista?". Nunca empieces a diseñar sin esta respuesta.

**Si sube una referencia (o ya tiene su propio diseño)** (sube capturas o links de carruseles que le gustan, o una plantilla suya,
o tiene la carpeta `Mis referencias de diseño`):
1. Estudia cada referencia slide por slide. Anota solo la **forma**: dónde va el titular y qué tamaño tiene,
   si hay foto y cómo (a sangre, de lado, polaroid, recortada), qué tipo de letra (condensada, gruesa redonda,
   serif, manuscrita), cómo se resalta la palabra clave, cómo es la portada y cómo el cierre.
2. Elige el estilo base de `estilos.md` que más se parece, y escribe las reglas que lo acercan a sus
   referencias como CSS en `css_extra` (tamaños, posiciones, fondos, bordes). Nunca copies colores, fotos,
   textos ni logos de la referencia: los colores, letras y fotos siempre son los de ella.
3. Guárdalo en `mi-estilo-carrusel.md`, con una línea de qué tomaste de cada referencia. Dile en una frase qué
   viste ("tus referencias usan titular gigante arriba y foto a sangre abajo").
4. Si dice "actualiza mi estilo" y sube referencias nuevas, se vuelve a estudiar y se reemplaza el archivo.

**Si no tiene diseño**, muéstrale los 8 estilos de `estilos.md` en una lista corta (nombre + para qué sirve) y
recomienda uno según el objetivo del carrusel. Ella elige; si dice "el que tú veas", elige tú y dile cuál.

## 2. Armar el carrusel

1. **Trae la plantilla más nueva.** Los estilos se mejoran seguido y la versión al día vive en la página
   de Jessica:
   - En Claude Code: `curl -fsSL https://jessicacastrillon.com/skills/carrusel.txt` (Windows: `curl.exe`).
   - En el chat de Claude: abre `https://jessicacastrillon.com/skills/carrusel.txt` con tu herramienta para
     leer páginas.
   Úsala solo si llegó completa: empieza con `<!doctype html>` y trae `/*DATOS*/` y `/*FIN*/`. Si no llegó
   (sin internet, la herramienta no puede abrirla o llegó cortada), usa la copia de esta skill:
   `plantilla/carrusel.html`. No le digas nada a la alumna de este paso salvo que use la copia vieja.
2. Reemplaza SOLO el bloque entre `/*DATOS*/` y `/*FIN*/` con el JSON del carrusel (formato abajo). No toques
   el resto del archivo.
3. Entrégalo:
   - **En el chat de Claude:** como un artefacto HTML (el archivo completo), para que se abra en el panel.
   - **En Claude Code:** guárdalo como `carrusel.html` dentro de la carpeta de ese carrusel (por ejemplo
     `Mi contenido/Carruseles/<tema>/`) y ábrelo en su navegador. En Windows: `start "" "carrusel.html"`.
     En Mac: `open carrusel.html`.
4. Dile en 3 líneas cómo se usa:
   - Toca **📷 Foto** en cada slide para poner su foto (desde su computador o celular).
   - Toca cualquier texto para corregirlo ahí mismo.
   - Toca **✨ Elementos** para ponerle lo que quiera, como en Canva: todos los emojis, formas (recuadros, círculos, manchas, estrellas), flechas, textos (globos, burbujas de chat, post-it, etiquetas, nota a mano) y mockups (celular, laptop, polaroid, post de Instagram, ventana, foto en círculo) con su foto o captura adentro. Se arrastran y, abajo de la slide, se agrandan, se giran, se pintan, se les cambia la opacidad, se les pone sombra y se pasan al frente o atrás.
   - **↕ Mover texto** si el texto le tapa la cara. **⬇ Descargar todas** baja las slides y el caption.

### El JSON de `DATA`

```json
{
  "marca": {"usuario": "@suusuario",
    "colores": {"fondo": "#F4EFE6", "tinta": "#141414", "acento": "#B00B00", "resalte": "#F4C70F",
                "tarjeta": "#FFFFFF", "suave": "#F6E1DA"},
    "letras": {"titulo": "Anton", "serif": "Instrument Serif", "cuerpo": "Inter Tight", "mano": "Caveat"}},
  "estilo": "editorial",
  "css_extra": "",
  "slides": [ ... ],
  "caption": "el caption completo"
}
```

- `estilo`: `editorial` · `revista` · `cuaderno` · `oscura` · `collage` · `oferta` · `agenda` · `aesthetic`.
- `letras`: nombres de Google Fonts. La plantilla ya trae Anton, Bebas Neue, Archivo Black, Playfair Display,
  Instrument Serif, Inter Tight, DM Sans y Caveat. Si su letra es otra de Google Fonts, agrégala al `<link>`
  de la cabecera. Si es una letra que solo tiene ella, usa la más parecida y díselo.
- `colores.suave`: un tono muy claro de su acento (fondo del collage). `tarjeta`: fondo de las tarjetas.

Cada slide lleva `tipo` y sus campos. En `titulo`, la palabra clave va entre asteriscos: `"Yo nunca aprendí *a editar.*"`.

| tipo | campos | para qué |
|---|---|---|
| `portada` | eti, titulo, apoyo, foto, pos | gancho de las slides 1 y 2 |
| `texto` | eti, titulo, apoyo, foto, pos, nota | una idea con su explicación |
| `lista` | eti, titulo, items (3 a 4) | pasos o puntos |
| `comparacion` | eti, titulo, a {titulo, items}, b {titulo, items} | antes / ahora, mito / realidad |
| `chat` | eti, titulo, mensajes [{yo, t}] | mostrar cómo se le habla a Claude, un DM, un comentario |
| `oferta` | eti, titulo, apoyo, precio, precio_nota | qué incluye y precio (solo datos reales) |
| `cierre` | eti, titulo, palabra, apoyo, foto | el pedido: comenta PALABRA, guarda, comparte |

Cada estilo tiene su propio diseño para cada tipo de slide (en Revista la lista es un índice, en Cuaderno un
checklist a mano, en Collage post-its…). Además, cada slide trae el botón **🔀 Otra forma** para cambiar cómo se
organiza: `variante` (0 = la del estilo; lista: 1 checklist, 2 números grandes, 3 cuadrícula; comparación:
1 arriba y abajo, 2 tabla ✗ ✓, 3 antes → después; portada: 1 foto grande, 2 solo texto, 3 foto en círculo;
texto: 1 frase gigante, 2 cita, 3 con nota a mano; chat: 1 en un celular; oferta: 1 precio gigante; cierre:
1 palabra gigante, 2 con foto grande). Usa variantes distintas para que el carrusel no se vea repetido. En
`oferta`, `precio_antes` muestra el precio anterior tachado (solo si es real).

Opcionales en cualquier slide: `etiquetas` (lista corta de palabras que señalan, estilo aesthetic) y `nota`
(frase a mano en su color de acento). `foto: false` quita la foto de esa slide. `pos`: `arriba`, `centro` o
`abajo`.

## 3. Reglas de diseño que no se rompen

- **El texto nunca tapa la cara.** Antes de elegir `pos` de una slide con foto, piensa dónde estará la cara
  (casi siempre en el tercio de arriba de una foto vertical): el texto va abajo. Si ella sube la foto después,
  recuérdale el botón ↕. Si ves en una foto que subió al chat dónde está su cara, decide tú la posición.
- **Una idea por slide.** Titular de 6 palabras como mucho; texto de apoyo de 25 palabras como mucho. Si el
  texto de `carruseles` no cabe, se acorta conservando su voz, nunca se achica la letra.
- **De 5 a 10 slides.** La 1 y la 2 son portadas (las dos funcionan solas). La última es el cierre.
- **Fotos reales de ella.** Nunca fotos de stock ni generadas. Si no tiene fotos, usa estilos sin foto
  (`cuaderno`, `collage`) o slides con `foto: false`.
- **Solo datos reales.** Precios, fechas, números y testimonios solo si ella los dio.
- **Su marca manda.** Colores y letras de ella siempre, aunque el estilo base o la referencia usen otros.

## 4. Correcciones

Ella corrige por número de slide ("en la 3 cambia...", "la 5 con otra foto"). Se hacen todas juntas en una
sola versión nueva del archivo. Lo que puede cambiar ella sola (texto, foto, posición) se lo recuerdas en
vez de regenerar.

## `mi-estilo-carrusel.md` (formato)

```markdown
# Mi estilo de carrusel
Actualizado: <fecha>
Usuario: @suusuario
Colores: fondo #..., texto #..., acento #..., resalte #...
Letras: titulares <letra> · texto <letra> · a mano <letra>
Estilo base: <uno de los 8> (o "propio, a partir de mis referencias")
Lo que tomé de mis referencias: <una línea por referencia>
css_extra: <el CSS, si hay>
```

**Elementos (opcional en el JSON):** cada slide o historia puede traer `"elementos": [{"k": "emoji"|"forma"|"texto"|"mock", "v": ..., "x": 540, "y": 700, "s": 1, "r": 0, "c": "acento", "o": 1, "sh": false, "t": "texto si lleva"}]`. Formas y flechas por nombre (rectángulo, redondeado, círculo, píldora, mancha, estrella, corazón, círculo a mano, subrayado, check, flecha curva, flecha a mano…); textos: globo, pensamiento, chat yo, chat otro, etiqueta, post-it, nota a mano, titular, caja de texto; mockups: celular, laptop, polaroid, post, ventana, foto círculo, foto. Pon alguno solo si ayuda a leer la slide (una flecha a la palabra clave, un círculo a un número); lo demás lo pone ella.
