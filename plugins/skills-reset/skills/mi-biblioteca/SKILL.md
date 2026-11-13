---
name: mi-biblioteca
description: MI BIBLIOTECA. Guarda todo lo que la alumna quiere aprender (reels, videos, clases, podcasts, artículos, libros, carruseles) con un resumen corto, por qué lo guardó y sus temas, en su Notion o en un archivo suyo, y le contesta cuando no se acuerda de algo que vio. Le muestra un tablero bonito, como una app, con lo último que guardó, sus temas y lo que tiene por ver. Úsalo cuando pega un link o una captura y dice "guarda esto", "guárdame este reel", "esto lo quiero en mi biblioteca", "ya lo vi", o pregunta "¿qué guardé sobre…?", "¿dónde vi lo de…?", "¿qué tengo por ver?", "mi biblioteca". Funciona en el chat de Claude (panel al lado) y en Claude Code (se abre en el navegador).
---

# MI BIBLIOTECA

> **Lo primero, siempre:** busca `mi-voz.md`. En el chat normal de Claude está en los archivos de su Proyecto (o en lo que adjuntó). Si puedes ver su computador (Claude Code o Génesis Estudio), está en su carpeta `Documentos/Mi contenido/` (o `OneDrive/Documentos/Mi contenido/`). Si no está en ningún lado, primero se hace su voz con la skill `mi-voz`.

> Antes de empezar, y cada vez que la alumna corrija: lee `biblioteca/criterio-y-correcciones.md` y síguelo.

Guardas lo que te sirve, con por qué lo guardaste, y cuando no te acuerdas, le preguntas. Contesta con lo que
tú guardaste, nunca con lo que se inventa.

## 0. Dónde vive su biblioteca (revisar primero, sin preguntar lo que ya se ve)

1. **Notion (lo mejor si lo usa).** Si tienes herramientas de Notion, busca una base de datos llamada
   "Mi biblioteca".
   - Si existe, úsala.
   - Si no existe, pregunta UNA vez: "¿Te creo tu biblioteca en Notion?". Con su sí, créala con estas
     propiedades: Título (título) · Tipo (selección: Reel, Video, Clase, Podcast, Artículo, Libro, Carrusel) ·
     Autor (texto) · Link (URL) · Resumen (texto) · Por qué lo guardé (texto) · Temas (selección múltiple) ·
     Fecha (fecha) · Estado (selección: Por ver, Visto).
2. **Sin Notion:**
   - En Claude Code, guarda en el archivo `mi-biblioteca.md` de la carpeta "Mi biblioteca" de sus Documentos (formato abajo).
   - En el chat de Claude, la biblioteca vive en un archivo `mi-biblioteca.md` de su Proyecto. Claude puede
     leerlo pero no cambiarlo: cada vez que guardes algo, entrégale el archivo actualizado para que lo
     reemplace en su Proyecto (dile cómo la primera vez, en una línea). Recomiéndale Notion si va a guardar
     mucho: ahí se guarda solo.
   - Si no tiene Notion conectado, dile en una línea cómo: en Claude, **Personalización → Conectores →
     Notion → Conectar**.

## 1. Guardar algo

Cuando pega un link, una captura o un nombre y dice "guarda esto":
- **Tipo:** reel, video, clase, podcast, artículo, libro o carrusel.
- **Título:** el de verdad si se ve; si no, uno corto y claro (máximo 7 palabras).
- **Autor:** la cuenta o la persona, si se sabe.
- **Resumen:** 1 o 2 frases con la idea que sirve, no la descripción del contenido.
- **Por qué lo guardé:** pregúntaselo en una línea si no lo dijo ("¿Para qué lo guardas: idea, estilo,
  aprender algo?"). Es lo que más le va a servir cuando lo busque. Máximo 6 palabras.
- **Temas:** 1 o 2, reutilizando los temas que ya tiene antes de inventar uno nuevo.
- **Estado:** "Por ver" si todavía no lo vio; "Visto" si ya.

**Lo que se puede leer y lo que no (dilo, no adivines):**
- **Artículos y páginas web:** si tienes cómo abrir la página, léela y resume. Si no se puede abrir, pide que
  pegue el texto o una captura.
- **Reels, TikToks y videos:** con solo el link no puedes ver el video por dentro. Resume a partir de lo que
  ella te cuente, del texto que pegue (el caption) o de capturas. Si no hay nada de eso, guárdalo con título y
  "por qué", y el resumen vacío.
- **Libros:** con el título y el autor basta. No inventes de qué trata si no lo sabes con seguridad: pregunta.

Responde en una línea: `Guardado ✓ Reel · "Serie diaria con la misma entrada" · temas: Series, Ganchos`.

## 2. Preguntarle a su biblioteca

"¿Qué guardé sobre ganchos?", "¿dónde vi lo de la entrada que se repite?", "¿qué tengo por ver?":
- Busca SOLO en su biblioteca (Notion o el archivo). Contesta con lo que encontraste: título, autor, cuándo lo
  guardó, por qué, y el link si hay.
- Si nada coincide, dilo: "No encontré nada guardado sobre eso". Nunca rellenes con lo que tú sabes del tema
  como si fuera de su biblioteca. Si sirve, ofrécelo aparte y avisado: "No está en tu biblioteca, pero te
  puedo contar lo que sé".
- Si encuentra varias cosas, hasta 5, la más útil primero.

## 3. El tablero

Cuando dice "mi biblioteca", o después de guardar si ella lo pide:
1. Usa `plantilla/mi-biblioteca.html`. Reemplaza SOLO el bloque entre `/*DATOS*/` y `/*FIN*/` con el JSON
   (formato abajo). No toques el resto.
2. Entrégalo:
   - **En el chat de Claude:** como un artefacto HTML, para que se abra en el panel.
   - **En Claude Code:** guárdalo como `Mi biblioteca/mi-biblioteca.html` y ábrelo (Windows
     `start "" "Mi biblioteca/mi-biblioteca.html"`, Mac `open "Mi biblioteca/mi-biblioteca.html"`).

El tablero tiene: Inicio (vista general), Pregúntale (un buscador por palabra), una pantalla por tipo (Reels,
Videos y clases, Artículos, Libros, Carruseles), Temas y Por ver. Cada cosa con link se abre al tocarla.

### El JSON de `DATA`

```json
{
  "nombre": "Ana",
  "colores": {"acento": "#B00B00", "suave": "#F5E2DC", "fondo": "#F4EEE4", "oscuro": "#161412", "tinta": "#161412"},
  "fuente": "tu Notion · Mi biblioteca",
  "pregunta": {"q": "¿Qué guardé sobre ganchos?", "r": "…", "nota": "", "ejemplo": false},
  "items": [{"tipo": "reel | video | clase | podcast | articulo | libro | carrusel", "titulo": "…", "autor": "…",
             "link": "https://…", "resumen": "…", "por_que": "…", "temas": ["…"], "fecha": "2026-03-09",
             "estado": "visto | por ver"}]
}
```

- `items`: toda su biblioteca (o las 200 más recientes si es muy grande). Los conteos y los temas se calculan
  solos.
- `pregunta`: lo último que le preguntó y lo que le contestaste, en una frase. `ejemplo: true` solo si todavía
  no ha preguntado nada y le muestras cómo se pregunta con algo que SÍ está en su biblioteca. Si la biblioteca
  está vacía, `"q": ""`.
- `nota`: opcional, una frase a mano corta que conecte lo encontrado con algo suyo.
- `colores`: rojo, negro y crema por defecto; si tiene colores de marca y los quiere, los suyos.

## 4. Nunca

- Nunca inventes cosas guardadas, autores, fechas ni resúmenes de algo que no pudiste ver.
- Nunca borres algo de su biblioteca sin que lo pida con esas palabras.
- Nunca guardes contraseñas, datos de pago ni datos personales de otras personas que salgan en una captura.

## `mi-biblioteca.md` (formato, cuando no hay Notion)

```markdown
# Mi biblioteca
- 2026-03-09 · Reel · Serie diaria con la misma entrada · @cuenta · https://… · Series, Ganchos · Visto
  Resumen: Misma frase de apertura y una palabra para comentar.
  Por qué: idea de serie
```
