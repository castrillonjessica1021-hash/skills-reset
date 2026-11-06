---
name: mi-dia
description: MI DÍA. Arma cada mañana un tablero muy bonito, como una app, con el calendario de la alumna (Google Calendar o su propia agenda), sus correos importantes (Gmail), pendientes, notas, hábitos y proyectos, una frase para el día y un resumen corto de lo que viene. Úsalo cuando dice "mi día", "buenos días", "¿qué tengo hoy?", "resumen de hoy", "arma mi día", "mis pendientes son…", "agrega a mis pendientes", "ya hice…", "anota que…", "mis hábitos son…", "hoy cumplí…", "mi proyecto es…", "agrega esta frase a mi lista", "mis frases", o cuando una tarea programada de la mañana la llama. Funciona en el chat de Claude (se abre en el panel) y en Claude Code (se abre en el navegador). Solo LEE su calendario y sus correos: nunca responde, borra ni crea nada sin que ella lo pida.
---

# MI DÍA

> Antes de empezar, y cada vez que la alumna corrija: lee `biblioteca/criterio-y-correcciones.md` y síguelo.

Una página que se abre en la mañana y te dice cómo viene el día: lo que tienes en el calendario, los correos
que de verdad piden algo, tus pendientes, una frase para arrancar y la única cosa que importa hoy.

## 0. Lo que se revisa primero (sin preguntarle nada que ya esté a la vista)

1. **Conectores.** Mira si tienes herramientas de **Google Calendar** y de **Gmail**.
   - Si falta alguno, díselo en UNA línea y sigue igual con lo que hay:
     > Para ver tu calendario (o tus correos) aquí, conéctalo una vez: en Claude, **Personalización →
     > Conectores → Google Calendar / Gmail → Conectar**, y entra con tu cuenta de Google.
   - **Muchas no usan Google Calendar, y está bien.** Sin calendario, la agenda sale de `mi-agenda.md`
     (formato abajo): ella te dice sus fechas como le salgan ("el sábado 14 tengo la clase a las 7") y tú
     las guardas ahí. No la mandes a aprender Google Calendar. Si algún día quiere pasarlas a su calendario,
     se lo haces tú, mostrándole antes la lista de lo que vas a crear.
   - **Un correo lleno no es problema.** No hace falta tener la bandeja limpia: MI DÍA solo mira lo que llegó
     desde ayer y descarta promociones, boletines y notificaciones. Nunca le pidas que borre correos para
     usarlo. Sin Gmail, la tarjeta de correos muestra cómo conectarlo (`"conectado": false`).
   - Nunca inventes eventos ni correos.
2. **Su nombre y sus colores.** Búscalos en `mi-voz.md`, `mi-estilo-carrusel.md` o su manual de marca. Si no
   hay colores, usa los de la plantilla (rojo, negro y crema). No preguntes por colores salvo que ella quiera
   cambiarlos.
3. **Sus archivos de MI DÍA** (si existen): `mis-pendientes.md`, `mis-frases.md`, `mis-notas.md`,
   `mis-habitos.md`, `mis-proyectos.md` y, si no usa calendario, `mi-agenda.md` (formatos abajo).
   - En Claude Code viven en la carpeta `Mi día/` de su computador. Créala la primera vez.
   - En el chat de Claude viven en los archivos del Proyecto. Claude no puede editar esos archivos: cuando
     algo cambia, le entregas el archivo actualizado para que lo reemplace (una línea de cómo, la primera
     vez).

## 1. Leer el día

- **Zona horaria:** la de su calendario. Si no hay calendario, la de su computador o la que ella diga.
- **Calendario:** eventos de hoy y de los próximos 7 días, de todos sus calendarios. Para el mes, los días que
  tienen algo (para los puntos del mini calendario).
- **Gmail:** correos de las últimas 24 horas (el lunes, desde el viernes) en la bandeja principal. Separa:
  - **Piden respuesta:** alguien espera algo de ella (una pregunta, un pedido, una fecha). `responder: true`.
  - **Para saber:** pagos, confirmaciones, avisos que sí le importan.
  - **Lo demás no se muestra:** promociones, boletines, notificaciones de redes.
  Máximo 4 en el tablero, los que piden respuesta primero. De cada uno: quién, el asunto y una línea de qué
  pide. Nunca copies el correo completo ni datos sensibles (claves, números de tarjeta, documentos).
- **Pendientes:** los de `mis-pendientes.md`, más los que salgan del día (un correo con fecha de entrega, un
  evento que necesita preparación). Lo que salga de un correo o evento lleva la nota de dónde salió.
  Máximo 6. Marca con estrella solo el más importante.

## 2. La frase del día (mezcla de tres fuentes)

Una sola frase arriba, debajo del saludo. Corta: 15 palabras como mucho.

- **Casi todos los días: escrita para hoy**, con la voz de la alumna (`mi-voz.md`). Que le hable a su día
  real: si el día viene cargado, que lo acompañe; si es tranquilo, que lo aproveche.
- **Uno o dos días por semana: de su lista** (`mis-frases.md`, sección "Mis frases"), elegida al azar.
- **Uno o dos días por semana: un versículo**, si ella tiene fe y lo quiere (sección "Versículos" de
  `mis-frases.md`, o uno muy conocido). Siempre con su cita en `"cita"` (por ejemplo "Salmo 46:10") y con la
  traducción que ella use. Si no estás seguro de las palabras exactas, usa uno de su lista.
- **Nunca:** frases de gurú, "desbloquea", "el siguiente nivel", "manifiesta", "intención", promesas de
  éxito ni de plata. Que suene a una amiga que la conoce, no a una taza de café.
- **Sin repetir:** en Claude Code, anota cada frase usada en `mis-frases.md` (sección "Ya usadas", con la
  fecha) y no repitas ninguna de los últimos 60 días. En el chat no hay memoria de un día a otro: no lo
  prometas; si hay lista, rota en orden según el día del mes.

## 3. El resumen y la única cosa

- **Resumen:** 3 o 4 frases cortas, en su voz. Primero cómo viene el día (cargado, tranquilo, de cerrar…),
  después lo que tiene hora o fecha, después lo que puede esperar. Una palabra clave entre asteriscos
  (`*cerrar*`) sale en cursiva y en su color.
- **Si hoy solo haces una cosa:** UNA tarea concreta, de 3 a 7 palabras, la que más mueve su día. Se elige
  por fecha de entrega y por lo que más le importa a ella, no por lo más fácil.
- **Solo datos reales.** Nada de "tienes 12 correos" si no los contaste. Si algo no se pudo leer, se dice.

## 4. Armar el tablero

1. Usa `plantilla/mi-dia.html`. Reemplaza SOLO el bloque entre `/*DATOS*/` y `/*FIN*/` con el JSON del día
   (formato abajo). No toques el resto.
2. Entrégalo:
   - **En el chat de Claude:** como un artefacto HTML (el archivo completo), para que se abra en el panel.
   - **En Claude Code:** guárdalo como `Mi día/mi-dia.html` (siempre el mismo nombre, para que quede en
     favoritos) y ábrelo: Windows `start "" "Mi día/mi-dia.html"`, Mac `open "Mi día/mi-dia.html"`.
3. Debajo, en el chat, solo dos líneas: la frase del día y la única cosa. El resto está en el tablero.

### El JSON de `DATA`

```json
{
  "nombre": "Ana",
  "fecha": "Lunes, 9 de marzo de *2026*",
  "hora": "7:00 a.m.",
  "colores": {"acento": "#B00B00", "suave": "#F7E3DF", "fondo": "#F7F2EA", "tinta": "#141414"},
  "frase": {"texto": "…", "cita": "", "fuente": "escrita | mi lista | versículo"},
  "resumen": {"texto": "Hoy es día de *cerrar*…", "una_cosa": "Enviar la propuesta a Laura"},
  "numeros": [
    {"n": "2", "lb": "Eventos hoy", "icono": "calendario"},
    {"n": "1", "lb": "Correos por responder", "icono": "correo"},
    {"n": "3", "lb": "Pendientes abiertos", "icono": "check"},
    {"n": "5", "lb": "Días para …", "icono": "estrella"}
  ],
  "mes": {"anio": 2026, "mes": 3, "hoy": 9, "marcados": [9, 12, 20]},
  "proximos": [{"dia": "Jue 12", "que": "…", "tono": "rojo | negro"}],
  "agenda_rango": "hoy y mañana",
  "agenda": [{"cuando": "10:00", "que": "…", "detalle": "10:00 – 11:00 · Zoom", "icono": "video", "tono": "rojo | negro | crema"}],
  "correos": {"conectado": true, "lista": [{"de": "…", "asunto": "…", "pide": "…", "responder": true}]},
  "pendientes": [{"t": "…", "nota": "vence hoy", "hecho": false, "estrella": true}],
  "cuenta_atras": {"n": 5, "texto": "días para …", "nota": "sábado 14 · 7 p.m."}
}
```

- `numeros`: 4 tarjetas. Si Gmail no está conectado, la de correos lleva `"n": "—"`.
- `cuenta_atras`: la fecha importante más cercana (un lanzamiento, un viaje, una entrega). Si no hay ninguna,
  quítala y el recuadro desaparece.
- `agenda`: hoy primero, con hora. Si hoy hay pocas cosas, completa con los próximos días (`"cuando": "MAR"`).
  Máximo 5. El evento más importante va en `rojo`, los fijos de siempre en `negro`, lo demás en `crema`.
- `icono`: calendario, correo, check, estrella, video, clase, cohete, persona, telefono, corazon, casa,
  dinero, reloj.
- `mes.marcados`: días del mes con algo en el calendario.
- `calendario_fuente`: una línea de dónde salen las fechas ("De tu Google Calendar" o "De tu agenda de MI DÍA").

**Las otras secciones del menú** (cada una abre su propia página dentro del tablero):

```json
"notas": [{"t": "…", "etiqueta": "ideas", "fecha": "9 mar"}],
"habitos": {"hoy": 0, "lista": [{"t": "Caminar 20 minutos", "dias": [1, 0, 1, 0, 0, 0, 0]}]},
"proyectos": [{"t": "…", "fecha": "20 mar", "siguiente": "…", "tareas": [{"t": "…", "hecho": true}]}]
```

- `notas`: las más recientes primero, máximo 9. Solo lo que ella anotó.
- `habitos.hoy`: el día de la semana de hoy (0 = lunes … 6 = domingo). `dias`: lunes a domingo de esta
  semana, 1 = cumplido. Si no tiene hábitos, `"lista": []`: la página le dice cómo elegirlos. Recomiéndale
  3 o 4, no más. Nunca le pongas hábitos que ella no eligió.
- `proyectos`: lo que ella está construyendo, con su fecha, el siguiente paso y sus pasos. La barra de avance
  se calcula sola con los pasos hechos; nunca escribas un porcentaje inventado.
- El menú de la izquierda abre cada página. Un enlace con `#habitos`, `#proyectos`, etc. abre directo esa
  página.

## 5. Pendientes y frases durante el día

- "Mis pendientes son…", "agrega…", "ya hice…", "quita…": actualiza `mis-pendientes.md` (en el chat, entrégale
  el archivo nuevo para que lo cambie en su Proyecto) y vuelve a armar el tablero solo si ella lo pide.
- "Agrega esta frase a mi lista": va a `mis-frases.md`.
- "Anota que…": va a `mis-notas.md`, con la fecha y una etiqueta corta.
- "Mis hábitos son…": van a `mis-habitos.md`. "Hoy cumplí…": marca el día. Al armar el día, la semana
  nueva empieza el lunes en blanco.
- "Mi proyecto es…", "terminé el paso…": van a `mis-proyectos.md`.
- En el tablero ella puede marcar los pendientes con un toque. En Claude Code el navegador lo recuerda hasta
  el día siguiente; para que Claude lo sepa, que te diga "ya hice…".

## 6. Cada mañana sola (opcional, solo donde funciona)

- **En la app de escritorio de Claude (Claude Code o Cowork) con tareas programadas:** ofrécele una tarea
  todos los días a la hora que ella diga (por defecto 7:00 a.m.) que corra esta skill y deje el tablero
  listo. Dile la verdad: la tarea corre si el computador está prendido y la app abierta; si estaban
  cerrados, corre apenas abra la app.
- **En el chat de Claude:** no hay tarea automática. Lo que funciona es escribir **"mi día"** cada mañana: en
  segundos está armado. No prometas que se actualiza solo.

## 7. Lo que nunca hace

- Nunca responde, reenvía, borra ni archiva correos, ni crea o cambia eventos, salvo que ella lo pida con
  esas palabras, y entonces le muestra lo que va a hacer antes de hacerlo.
- Nunca inventa eventos, correos, personas ni números para que el tablero se vea más lleno. Un día vacío se
  muestra vacío ("Día libre").
- Nunca muestra en el tablero contraseñas, códigos de verificación, números de tarjeta ni documentos.

## Formatos

`mis-pendientes.md`:
```markdown
# Mis pendientes
- [ ] Enviar la propuesta a Laura · vence vie 13 · ★
- [ ] Grabar el reel de la semana
- [x] Pagar el internet · hecho 9 mar
```

`mi-agenda.md` (solo si no usa Google Calendar; las fechas que ya pasaron se borran solas al armar el día):
```markdown
# Mi agenda
- dom · 9:00 p.m. · Clase en vivo · todos los domingos
- 2026-03-14 · 7:00 p.m. · Cumpleaños de mi mamá
- 2026-03-20 · todo el día · Entrega del proyecto · ★
```

`mis-notas.md`:
```markdown
# Mis notas
- 2026-03-09 · ideas · Hacer un reel de lo que aprendí con mi primera clienta
```

`mis-habitos.md` (una línea por hábito; la marca es de lunes a domingo, x = cumplido):
```markdown
# Mis hábitos
Semana del 2026-03-09
- Caminar 20 minutos · x.x....
- Leer 10 páginas · xx.....
```

`mis-proyectos.md`:
```markdown
# Mis proyectos
## Lanzamiento de mi curso · 2026-03-20
Siguiente: grabar el video de venta
- [x] Escribir la página
- [ ] Grabar el video de venta
```

`mis-frases.md`:
```markdown
# Mis frases
## Mis frases
- No tienes que hacerlo todo hoy. Solo lo que de verdad te toca.
## Versículos
- "Estad quietos, y conoced que yo soy Dios." — Salmo 46:10
## Ya usadas
- 2026-03-09 · No tienes que hacerlo todo hoy…
```
