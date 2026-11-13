---
name: mi-jornada
description: MI JORNADA. Cada noche, en dos minutos, la alumna revisa con Claude qué salió bien, qué no, qué cambia mañana (una sola cosa) y cómo terminó su energía; cada domingo recibe el plan de la semana siguiente con tres prioridades y qué toca cada día. Le muestra un tablero bonito en azul claro y amarillo, como una app, con su revisión, su semana, su racha, el plan y todo lo que salió bien. Úsalo cuando dice "mi jornada", "revisión de hoy", "cierro el día", "¿cómo me fue hoy?", "hoy salió bien…", "energía 3", "aprendí que…", "mi plan de la semana", "plan del domingo", "¿qué hago esta semana?", o cuando una tarea programada de la noche o del domingo la llama. Funciona en el chat de Claude (panel al lado) y en Claude Code (se abre en el navegador).
---

# MI JORNADA

> **Lo primero, siempre:** busca `mi-voz.md`. En el chat normal de Claude está en los archivos de su Proyecto (o en lo que adjuntó). Si puedes ver su computador (Claude Code o Génesis Estudio), está en su carpeta `Documentos/Mi contenido/` (o `OneDrive/Documentos/Mi contenido/`). Si no está en ningún lado, primero se hace su voz con la skill `mi-voz`.

> Antes de empezar, y cada vez que la alumna corrija: lee `biblioteca/criterio-y-correcciones.md` y síguelo.

Dos minutos cada noche para cerrar el día, y un plan cada domingo para no empezar la semana a ciegas. Lo
importante no es el tablero: es que ella vea, semana tras semana, que sí avanza.

## 0. Dónde se guarda

- **En Claude Code (su computador):** en la carpeta "Mi jornada" de sus Documentos: `noches.md` (una entrada
  por noche) y `plan-semana.md` (el plan vigente). Créala la primera vez.
- **En el chat de Claude:** Claude no recuerda de un chat a otro. Lo que funciona: **un chat por semana**
  ("Mi jornada · semana del 9") dentro de su Proyecto. Cada noche escribe en el mismo chat y el domingo pide
  ahí el plan. Si quiere conservarlo, al final de la semana le entregas `noches.md` para que lo guarde en su
  Proyecto.
- Si tiene MI DÍA (`mis-pendientes.md`, `mi-agenda.md`, `mis-proyectos.md`) o un calendario conectado, úsalos
  para el plan del domingo. Si no, el plan sale de sus noches y de lo que ella cuente.

## 1. La revisión de cada noche

Cuando escribe "mi jornada" (o la llama la tarea de la noche), haz las cuatro preguntas en UN solo mensaje,
corto:

> 1. ¿Qué salió bien hoy?
> 2. ¿Qué no salió?
> 3. ¿Qué cambias mañana? (una sola cosa)
> 4. ¿Cómo terminó tu energía, del 1 al 5?

- Ella contesta como le salga: todo junto, en desorden o con una nota de voz pasada a texto. Tú lo ordenas.
  No le pidas formato.
- Si contestó solo una parte, no insistas más de una vez. Guarda lo que hay.
- **Qué salió bien:** si dice "nada", busca con ella una cosa chica y verdadera (lo que sí hizo, aunque sea
  poco). Nunca inventes logros.
- **Qué cambio mañana:** UNA cosa, concreta y que se pueda hacer. Si da cinco, pregúntale cuál es la más
  importante.
- **Aprendí:** si en lo que cuenta hay una lección, propónla en una línea ("¿lo guardo como aprendizaje?") y
  guárdala solo si dice que sí.
- **Responde en 2 o 3 líneas**, con su voz y cálida: reconoce lo que salió, nombra la una cosa de mañana y
  despídela. Sin sermón, sin frases de gurú y sin "deberías". Si en su voz aparece la fe, puede aparecer una
  línea así, con naturalidad.
- Si se nota agotada o triste varias noches seguidas, dilo con cariño y propón un día más liviano. Si habla de
  algo serio (no poder más, sentirse en peligro), deja la revisión, acompáñala y anímala a hablar con alguien
  de confianza o con un profesional. No diagnostiques nada.

Guarda la noche en `noches.md` (formato abajo).

## 2. El plan del domingo

Cuando dice "mi plan de la semana" (o la llama la tarea del domingo):
1. Lee sus noches de la semana: qué se repitió como "no salió", qué cambió, cómo anduvo su energía.
2. Mira lo que viene: agenda, fechas importantes, pendientes y proyectos con su siguiente paso.
3. Arma el plan:
   - **Tres prioridades, nunca más.** Las que más mueven su semana: lo que tiene fecha y lo que ella dijo que
     importa. Cada una con una línea de por qué.
   - **Qué toca cada día:** de 1 a 3 palabras por día. Marca el día clave (una entrega, una clase, un
     lanzamiento).
   - **Esta semana NO:** una o dos cosas que conviene no empezar, cuando su semana viene cargada.
   - Si su energía estuvo baja, pon menos y dilo.
4. Muéstraselo y pregúntale si cambia algo, una sola vez. Con su sí, guárdalo en `plan-semana.md`. Si usa MI
   DÍA, pregúntale si pasas las prioridades a sus pendientes.

## 3. El tablero

Cuando dice "mi jornada" y ya revisó, o "muéstrame mi semana", o al entregar el plan:
1. Usa `plantilla/mi-jornada.html`. Reemplaza SOLO el bloque entre `/*DATOS*/` y `/*FIN*/` con el JSON
   (formato abajo). No toques el resto.
2. Entrégalo:
   - **En el chat de Claude:** como un artefacto HTML, para que se abra en el panel.
   - **En Claude Code:** guárdalo como `mi-jornada.html` en su carpeta "Mi jornada" y ábrelo (Windows
     `start ""`, Mac `open`).

El tablero tiene: Esta noche, Mi semana, Plan del domingo y "Lo que me llevo" (Lo que salió bien, Lo que
aprendí, Lo que cambio), cada uno en su pantalla completa.

### El JSON de `DATA`

```json
{
  "nombre": "Ana",
  "colores": {},
  "fecha_txt": "Lunes 9 de marzo",
  "hora": "9:30 p.m.",
  "hoy": {"bien": ["…"], "no": ["…"], "cambio": "…", "energia": 3, "aprendi": ["…"]},
  "semana": [{"dia": "Lun", "n": 9, "estado": "revisada | sin revisar | hoy | futuro", "energia": 3, "nota": ""}],
  "racha": 1,
  "plan": {"llega": "llega el dom 15 · 7 p.m.", "rango": "16 AL 22",
           "prioridades": [{"t": "…", "detalle": "…"}],
           "dias": [{"d": "LUN", "t": "…", "clave": false}],
           "no_hacer": ["…"], "nota": ""},
  "historial": [{"fecha": "Lun 9 mar", "bien": ["…"], "no": ["…"], "cambio": "…", "aprendi": ["…"], "energia": 3}]
}
```

- `semana`: de lunes a domingo de esta semana. `energia` solo si ella la dijo; si no, `null`.
- `racha`: noches revisadas esta semana.
- `plan`: el plan vigente. Si todavía no hay, `"prioridades": []`.
- `historial`: las últimas noches, la más nueva primero (hasta 30). De ahí salen las pantallas de "Lo que me
  llevo".
- `colores`: vacío = azul claro y amarillo (el diseño de MI JORNADA). Si quiere otro acento, `{"acento": "#…", "oro": "#…"}`.

## 4. Que llegue sola (opcional, solo donde funciona)

- **En la app de escritorio de Claude con tareas programadas:** ofrécele dos tareas, la revisión de cada noche
  a la hora que ella diga (por defecto 9:30 p.m.) y el plan el domingo (por defecto 7 p.m.). Dile la verdad:
  corren si el computador está prendido y la app abierta; si no, corren apenas la abra. Créalas solo con su sí.
- **En el chat de Claude:** no hay aviso automático. Lo que funciona es escribir "mi jornada" cada noche y "mi
  plan de la semana" el domingo. No prometas que llega sola.

## Formatos

`noches.md`:
```markdown
# Mis noches
## 2026-03-09 · energía 3
Bien: terminé la propuesta · salí a caminar
No salió: no grabé el reel
Cambio mañana: grabar antes de abrir el correo
Aprendí: si grabo temprano, grabo
```

`plan-semana.md`:
```markdown
# Mi semana del 16 al 22
1. … (por qué)
2. …
3. …
Lun: … · Mar: … · Mié: … · Jue: … · Vie: … · Sáb: … (clave) · Dom: …
Esta semana NO: …
```
