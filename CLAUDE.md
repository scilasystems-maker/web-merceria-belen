# Mercería Belén — web

Web de **Mercería Belén**, mercería de barrio en La Viña (Lorca, Murcia). Cliente de **ScilaAI**.

- Repo: `scilasystems-maker/web-merceria-belen` (rama `main`)
- Publicada con GitHub Pages: https://scilasystems-maker.github.io/web-merceria-belen/
- Todo lo que hay en el repo se publica en Pages salvo lo excluido en `_config.yml` (hoy: `CLAUDE.md`). Ojo: el repo es público, así que en GitHub todo se puede leer igualmente.
- **Mientras esté en GitHub Pages es una demo**: `noindex, nofollow`, sin `canonical` ni `og:url`. **Revertir cuando haya dominio propio**: volver a `index, follow`, añadir `<link rel="canonical">` y `og:url` con el dominio, y cambiar el `url` del JSON-LD (hoy `https://scilasystems-maker.github.io/web-merceria-belen/`) por el dominio.

## Forma de trabajar

- Paso a paso: se propone el cambio, el cliente/ScilaAI decide, y solo entonces se toca el código.
- **No inventar datos del negocio.** Lo que no se sepa se marca como pendiente (`<!-- EDITAR: ... -->` en el HTML o `<span class="pendiente">` en los textos legales).
- Al terminar cada cambio: commit y push a `main`.
- Sin frameworks ni build: un único `index.html` con HTML, CSS y JS en línea (más las tipografías en `fuentes/`). Mantenerlo así salvo decisión explícita.
- **Nunca escribir `</script>` dentro del JS en línea, ni siquiera en un comentario**: el navegador cierra ahí el bloque y todo el JS deja de funcionar.
- Idioma de la web y del código (clases, variables, comentarios): español.

## Datos reales del negocio (confirmados)

| Dato | Valor |
|---|---|
| Nombre | Mercería Belén |
| Dirección | Ctra. de Granada, 19 Bajo, 30800 Lorca (Murcia). Área Comercial La Viña |
| Teléfono | 690 70 38 62 (`tel:+34690703862`) |
| Horario | L–V 10:00–13:30 y 17:00–20:00 · Sábado 10:00–13:30 |
| Qué venden | Mercería · lencería y corsetería · moda de mujer y de hombre · ropa de bebé y niño |
| Especialidad | Tallas grandes de mujer |

## Datos de la ficha discoverinmurcia

**Fuente: ficha discoverinmurcia, pendiente de confirmar con la clienta.** Se mantienen en la web:

- «Trato cercano».
- «Principales marcas» / «Primeras marcas».
- «Precios muy competitivos» / «Buenos precios».
- «Complementos».
- Email `belenpadilla39@gmail.com` (pie de página).
- Coordenadas 37.66462, -1.70387 (JSON-LD y enlace a Google Maps).
- Nombre «Mercería Lencería Belén» (`alternateName` del JSON-LD).
- Texto del bloque de tallas grandes: «Somos especialistas en tallas grandes de mujer. Prendas selectas de las principales marcas, con excelente calidad, y un trato cercano para ayudarte a elegir. Ven a probártelas o pregúntanos antes por tu talla.» («prendas selectas», «principales marcas», «excelente calidad» y «trato cercano» salen de la ficha).

## Pendientes de confirmar con la clienta

- **WhatsApp en el 690 70 38 62**: lo confirma ScilaAI con la clienta. El formulario y el botón flotante dependen de ello. No tocar mientras tanto.
- **Domingo cerrado** (se deduce del horario, pero no está dicho).
- **Festivos y horario de verano.**
- **Datos legales**: titular, NIF y email de contacto. En la web aparece «Datos del titular pendientes de publicar» (`.pendiente`, estilo discreto en gris cursiva).
- **Dominio propio**: no hay. `merceriabelen.es` era una suposición y ya no aparece en la web.
- Redes sociales (no hay ninguna en la web).
- Enlace de créditos `https://www.scilaai.com`.

## Retirados de la web hasta que la clienta los confirme

No tienen fuente. No volver a ponerlos sin confirmación:

- Pijamas, fajas y canastilla.
- `priceRange: "€€"` del JSON-LD.
- «Aquí te conocen, te escuchan y, si no lo tenemos, te decimos dónde encontrarlo» (párrafo de Por qué Belén). Queda solo «Formamos parte del Área Comercial de La Viña.».
- «de señora y caballero» en la tarjeta de lencería (queda «Sujetadores, braguitas y ropa interior.»).
- «para caballero» y «de buena calidad» en la tarjeta de moda hombre (queda «Ropa, complementos y ropa interior para el día a día.»).
- Texto anterior del bloque de tallas grandes: «Prendas con buen patrón, tejidos agradables y estilo actual, para que elegir sea por gusto y no por lo que queda en la percha. Ven, pruébate y te asesoramos con calma.» (sustituido por el de la ficha discoverinmurcia).

## Pendientes `<!-- EDITAR -->` en index.html

1. Demo en GitHub Pages: `noindex` y sin canonical/og:url; revertir con dominio propio — `<head>`.
2. `og:image` 1200×630 con foto real del escaparate — `<head>`.
3. Confirmar horario actual, festivos y si cambia en verano — sección Visítanos.
4. Confirmar que el 690 70 38 62 tiene WhatsApp — antes del formulario.
5. Confirmar email y redes sociales — pie de página.
6. Sustituir los textos `.pendiente` de los modales legales por titular, NIF y email reales, revisar con asesoría y actualizar «Última actualización».
7. Foto real de prendas de tallas grandes — bloque Tallas grandes (ver «Bloque de tallas grandes»).

## Identidad visual

Concepto: costurero / mercería de toda la vida con un acabado editorial moderno. Motivos recurrentes: botones, carrete de hilo, aguja, cinta métrica, pespuntes (bordes discontinuos) y una textura de tela muy sutil en el fondo.

### Paleta (variables en `:root`)

| Variable | Color | Uso |
|---|---|---|
| `--lino` | `#F5EEE3` | Fondo general |
| `--lino-2` | `#EDE3D3` | Fondo secundario, hover del menú, tarjeta hombre |
| `--papel` | `#FBF7F1` | Tarjetas, paneles, formulario |
| `--tinta` | `#241226` | Texto principal, bloques oscuros, `theme-color` |
| `--tinta-2` | `#4A3048` | Texto secundario |
| `--gris` | `#6E5F6B` | Texto terciario, etiquetas |
| `--coral` | `#E0485A` | Color de marca: botones, logo, acentos, sección tallas |
| `--coral-osc` | `#B8323F` | Hover del coral, etiquetas y rótulos de sección («01 — La tienda»…) sobre fondo claro (5,1:1) |
| `--coral-fuerte` | `#DC3045` | **Fondos con texto blanco**: botones coral y bloque de tallas grandes (blanco 4,6:1). Mismo tono que `--coral`, 5,4 puntos más oscuro |
| `--mostaza-clara` | `#F3CF90` | Títulos grandes sobre `--coral-fuerte` (3,1:1) |
| `--borde-campo` | `#9D8F9C` | Bordes de campos, opciones e interruptores (3:1 sobre blanco) |
| `--mostaza` | `#E9A93A` | Cinta métrica, subrayados, acentos sobre fondo oscuro |
| `--salvia` | `#8FA88A` | Botón ilustrado |
| `--rosa` | `#F3C9C4` | Tarjeta lencería, disco de la portada |

Otros fijos: `#DCE5D6` (tarjeta bebé), `#E7DCCB` (mapa), `#2FA36B` (punto «abierto»), `#25D366` (icono de WhatsApp sobre fondo oscuro, en la barra móvil), `#1DA851` (fondo del botón flotante de WhatsApp: el icono blanco necesita 3:1; con `#25D366` daba 1,98:1).

Otros tokens: `--radio: 22px`, `--sombra`, `--ancho: 1180px`.

### Tipografías (servidas desde la propia web, sin Google Fonts)

- **Fraunces** (`--serif`), variable con ejes `opsz`, `wght` 300–800 y `SOFT` (se usa `SOFT 100`). Títulos, cifras, cursivas en coral.
- **Manrope** (`--sans`) 400–700 (un solo archivo variable). Texto, botones, etiquetas.
- Archivos en `fuentes/`: un `.woff2` por familia/estilo y juego de caracteres (`latin` y `latin-ext`), descargados de Google Fonts con la misma petición que usaba la web. Los `@font-face` están al principio del `<style>`, con `unicode-range`: el navegador solo baja `latin-ext` si hace falta (en español basta con `latin`).
- Se precargan (`<link rel="preload">`) los tres `latin`: Fraunces normal, Fraunces cursiva y Manrope.
- Licencia SIL Open Font License 1.1: `fuentes/OFL-Fraunces.txt` y `fuentes/OFL-Manrope.txt`. Hay que mantenerlas junto a las fuentes.
- Solo cubren los caracteres de esos juegos: por ejemplo, la flecha «→» no está y saldría en otra fuente (se usa «›»).

## Estructura de la página

| # | Sección | id / clase | Contenido |
|---|---|---|---|
| — | Saltar al contenido | `.saltar` | Primer elemento del `<body>`. Solo se ve al llegar con el tabulador; lleva a `<main id="contenido">` |
| — | Cabecera fija tipo píldora | `#cabecera` | Logo botón + menú + botón llamar (oculto ≤ 640px) + hamburguesa |
| — | Hilo cosido | `.hilo` | SVG que se «cose» al hacer scroll. Escritorio: zigzag de lado a lado. < 700px: pespunte fino pegado al borde izquierdo (x 2–10px), fuera del texto |
| — | Portada | `#inicio` | H1 «Del botón al conjunto perfecto» (se cose al cargar), estado abierto/cerrado, escena ilustrada con parallax, botón principal con pespunte |
| — | Cinta métrica | `.cinta` | Marquesina con las categorías |
| 01 | La tienda | `#tienda` | Bento: Mercería, Lencería y corsetería, Bebé y niño, Moda mujer, Moda hombre |
| 02 | Tallas grandes | `#tallas` | Bloque coral con dos cintas métricas que se desenrollan con el scroll + hueco para foto |
| 03 | Por qué Belén | `#porque` | 4 motivos |
| 04 | Visítanos | `#visitanos` | Horario (resalta hoy) + mapa ilustrado + Google Maps |
| 05 | Pregúntanos | `#pregunta` | Formulario que abre WhatsApp con el mensaje (no guarda datos) |
| 06 | Preguntas frecuentes | `#faq` | `<details>` |
| — | Pie | `.pie` | Lema grande, datos, enlaces legales (+ «Configurar cookies»), créditos ScilaAI |
| — | WhatsApp flotante | `#wa-flotante` | Solo > 640px |
| — | Barra de contacto móvil | `#barra-movil` | Solo ≤ 640px: Llamar / WhatsApp / Cómo llegar, fija abajo. `body` lleva `padding-bottom` para que no tape el pie |
| — | Aviso de cookies | `#aviso-cookies` | Primera visita, abajo. Escritorio: a la izquierda del botón de WhatsApp. Móvil: encima de la barra de contacto |
| — | Modales | `dialog#modal-*` | Aviso legal, privacidad, cookies y `modal-config-cookies` (Configurar cookies) |

## JavaScript (en línea, al final)

- Año automático en el pie.
- Menú móvil.
- Abierto/cerrado con hora de Madrid: objeto `HORARIO` en minutos (si cambia el horario, cambiarlo aquí, en la lista `#horario`, en el FAQ y en el JSON-LD).
- Festivos y vacaciones: lista `FESTIVOS` (ver «Cómo añadir festivos y vacaciones»). Si hoy está en la lista, el indicador dice «Hoy cerrado por festivo / por vacaciones · abrimos …» y la tabla marca esa fila.
- Aparición al hacer scroll (`.aparece` + IntersectionObserver).
- Hilo que se cose con el scroll (dos trazados: escritorio y móvil < 700px; se recalcula al redimensionar o girar).
- La barra móvil se oculta (`.oculta`) mientras se escribe en el formulario, para que no tape el campo con el teclado abierto.
- Parallax de la escena con el ratón.
- Cintas métricas de tallas grandes ligadas al scroll (variables `--p1` y `--p2` en `#metro`).
- Formulario → `wa.me` con texto prellenado, trampa antispam `.trampa`.
- Modales con `<dialog>` (función `abreModal`): solo uno abierto a la vez; se cierran con la X, con Esc y tocando fuera; mientras hay uno abierto la página de detrás no se desplaza. Necesitan `margin:auto` en su CSS: el reset `*{margin:0}` quita el centrado que pone el navegador. Cualquier `<dialog>` nuevo usa la misma regla.
- Cookies: aviso, panel de configuración y consentimiento (ver «Cookies y textos legales»).
- Respeta `prefers-reduced-motion`.

## Animación de la portada

Una sola vez al cargar, ~2,3 s en escritorio y ~1,5 s en móvil. No se repite.

1. **Título cosido**: el H1 está partido en tres `.linea`. Una aguja (`.aguja-titulo`, creada por JS) recorre cada línea mientras se destapa con `clip-path` y deja un pespunte coral (`.puntada`) que luego se desvanece. Al terminar la línea de «conjunto» se dibuja el subrayado mostaza.
2. **Hilo del carrete al botón** (solo escritorio, con el carrete a la derecha y el botón visible en pantalla): un SVG temporal (`.hilo-portada`) sale del extremo del hilo del carrete, pasa por el hueco entre el texto y los botones y llega por arriba al botón «¿Lo tenéis? Pregunta». Luego se desvanece y se borra.
3. **Pespunte del botón** (`.boton-cosido::after`): un contorno discontinuo coral se «cose» alrededor del botón principal y **se queda**. En móvil es lo único que hace el botón. Si el botón no se ve al cargar, se cose cuando aparece en pantalla.

Detalles:

- `<html class="anima-portada">` se pone en el `<head>` antes de pintar, solo si el usuario **no** tiene `prefers-reduced-motion`. Sin esa clase todo se ve quieto y completo (título visible, pespunte del botón ya dibujado).
- Si el JS fallara, a los 5 s el CSS muestra el título y el pespunte igualmente.
- Espera a la tipografía (máx. 700 ms) para medir bien las líneas.
- En pantallas bajas (p. ej. 1280×800) el título encoge un poco (`min(8.2vw, 12svh)`) y el margen superior de la portada baja, para que el botón principal se vea sin hacer scroll.
- Si se cambia el texto del H1, mantener una `<span class="linea">` por línea.

## Bloque de tallas grandes

- **Cintas** (`#metro`, `aria-hidden`): la 1.ª (mostaza, 1–10) sale de una caja de metro; la 2.ª (papel, 11–20) se desenrolla de un rollo que gira. Los números son una cinta métrica genérica: **no son tallas** y no hay que convertirlos en rangos de tallas sin datos de la clienta.
- **Ligadas al scroll**, también hacia atrás: el JS pone `--p1` y `--p2` (0 a 1) según dónde está la cinta en pantalla (empieza cuando asoma al 95 % de la altura y termina al 40 %). La 2.ª va un poco por detrás de la 1.ª.
- Solo escucha el scroll mientras el bloque está cerca de la pantalla (IntersectionObserver).
- **Sin JS o con `prefers-reduced-motion`**: las variables valen 1 y las cintas se ven extendidas y quietas.
- La frase «Que la ropa se adapte a ti, y no al revés» ya **no** está dentro del `aria-hidden` (antes la ocultaba a lectores de pantalla).

### Hueco para la foto (pendiente)

En el HTML, dentro de `.tallas-visual`, hay un `<!-- EDITAR -->` con la etiqueta `<figure class="tallas-foto">` comentada. Para activarla:

1. Guardar la foto en `fotos/tallas-grandes.jpg` (vertical 4:5, mínimo 800×1000 px, optimizada).
2. Quitar el comentario dejando solo la etiqueta `figure`.
3. Poner en `alt` una descripción real de la foto.

Sale como una foto con pespunte, un poco girada, y las cintas pasan por delante de su parte de abajo, como tomando medidas. Mientras no haya foto, el bloque se ve completo sin ella. Probado con una imagen de prueba a 390 y 1280 px.

## Cómo añadir festivos y vacaciones

La lista está en `index.html`, en el `<script>` del final. Buscar `var FESTIVOS`. **Hoy está vacía**: solo se añaden fechas que confirme la clienta.

```js
var FESTIVOS = [
  // EDITAR: añadir aquí los festivos y vacaciones que confirme la clienta
  '2026-12-08',                  // un día suelto
  '2026-12-25',
  ['2027-08-09', '2027-08-21'],  // un periodo: del 9 al 21 de agosto, los dos incluidos
];
```

Reglas:

- Formato siempre `'AAAA-MM-DD'`, entre comillas simples y con coma al final de cada línea.
- Día suelto → la fecha. Periodo (vacaciones) → `['inicio', 'fin']`, ambos días incluidos.
- Una fecha mal escrita se ignora (sale un aviso en la consola del navegador) y no rompe la web.
- Las fechas pasadas no molestan, pero conviene limpiar la lista de vez en cuando.
- Se usa la fecha de Madrid, esté donde esté quien visita la web.

Qué hace la web:

- **Día suelto = festivo. Periodo = vacaciones.** Si un día suelto cae dentro de un periodo, manda «festivo».
- **Indicador** (portada y Visítanos): si hoy está en la lista, dice «Hoy cerrado por festivo» o «Hoy cerrado por vacaciones», seguido de «· abrimos mañana / el miércoles / el lunes 24 de agosto a las 10:00». El «abrimos…» se salta los festivos y vacaciones aunque caigan otro día.
- **Tabla de horario**: cada fila es el próximo día de esa semana (hoy y los 6 siguientes). Si cae en la lista, en lugar de las horas pone «Cerrado · festivo 8 dic» o «Cerrado · vacaciones», en rosa y cursiva.
- **Los días que ya cierran siempre (domingo) no se marcan**: en la tabla siguen diciendo solo «Cerrado» y el indicador dice lo de un domingo normal («Cerrado · abrimos mañana…»). La regla es por día completo: un sábado festivo sí se marca, porque normalmente abre por la mañana.

## Accesibilidad (WCAG 2.2 AA)

Auditado con axe-core (0 incumplimientos A/AA y de buenas prácticas, en la página, con el aviso de cookies, con cada pop-up y con el menú móvil abierto) y revisando a mano los contrastes que axe no puede medir por la textura del fondo.

**Reglas para no romperlo:**

- **Contraste.** Texto normal ≥ 4,5:1 y texto grande (≥ 24 px, o ≥ 18,66 px en negrita) ≥ 3:1. Elementos gráficos y bordes de controles ≥ 3:1.
  - Texto blanco sobre coral: siempre sobre `--coral-fuerte`, nunca sobre `--coral` (4:1, no llega).
  - Coral sobre lino solo para títulos grandes (3,5:1). Para texto normal, `--coral-osc`.
  - Mostaza sobre coral no llega ni en títulos: usar `--mostaza-clara`.
  - Bordes de campos y opciones: `--borde-campo`.
- **Foco visible**: `:focus-visible` con contorno coral de 3 px. Sobre fondo coral (bloque de tallas) el contorno es blanco. Los campos del formulario usan un doble borde coral. No quitar el `outline` sin poner otro indicador.
- **Orden del tabulador** = orden del HTML: saltar al contenido → cabecera → portada → … → pie → WhatsApp/barra móvil. El aviso de cookies, cuando está visible, va justo después de «Saltar al contenido».
- **El foco no se esconde** bajo la cabecera fija ni bajo la barra móvil: `scroll-padding-top:100px` y, en móvil, `scroll-padding-bottom:96px`.
- **Menú móvil**: al abrirlo, el foco pasa al primer enlace (en el HTML los enlaces van antes que el botón). Esc lo cierra y devuelve el foco al botón.
- **Pop-ups**: `<dialog>` modal (la página de detrás queda bloqueada). El botón de cerrar se llama «Cerrar: <título>» (lo pone el JS).
- **Nombres**: los enlaces de teléfono se anuncian como «Llamar al 690 70 38 62». Los que abren otra pestaña o WhatsApp llevan un texto oculto `<span class="sr">(se abre en otra pestaña)</span>`. Los iconos decorativos llevan `aria-hidden="true"`.
- **Títulos en orden**: los del pie son `h2` con aspecto de etiqueta (`.pie-cols h2`).
- El botón flotante de WhatsApp está dentro de `<aside aria-label="WhatsApp">`, para que no quede fuera de las zonas de la página.

## Icono de la pantalla de inicio (manifest)

- `manifest.webmanifest`: nombre «Mercería Belén», nombre corto «M. Belén», `theme_color` `#241226` (= `<meta name="theme-color">`), `background_color` `#F5EEE3`, `display: standalone`, `start_url` y `scope` relativos (`./`) para que funcione en GitHub Pages y con dominio propio.
- `iconos/`: mismo dibujo que el favicon (botón coral con pespunte y 4 agujeros).
  - `icono-192.png`, `icono-512.png`: fondo transparente (`purpose: any`).
  - `icono-maskable-192.png`, `icono-maskable-512.png`: fondo lino y el botón al 80 %, dentro de la zona segura de los iconos adaptables de Android (`purpose: maskable`).
  - `apple-touch-icon.png` (180×180): igual que el maskable, porque iPhone no admite transparencia.
  - `icono.svg` e `icono-con-fondo.svg`: originales para regenerar los PNG si cambia el dibujo.
- **Sin service worker ni modo offline** (decisión explícita). Si no hay conexión, la web no abre.

## Cookies y textos legales

**Hoy la web no usa cookies de terceros ni analíticas, y no carga nada de terceros al visitarla** (ni fuentes, ni mapas, ni scripts). Lo único que guarda es la elección de cookies.

### Cómo funciona el consentimiento

- **Aviso** (`#aviso-cookies`): sale en la primera visita, después de la animación de portada (al momento si hay `prefers-reduced-motion`). Botones «Rechazar» y «Aceptar» con el mismo estilo y tamaño (guía AEPD) y «Configurar».
- **Panel** (`#modal-config-cookies`): técnicas (siempre activas) y analíticas (desactivadas por defecto).
- **Se guarda** en `localStorage`, clave `mb-cookies`: `{version, fecha, tecnicas, analiticas}`.
- **Vuelve a preguntar** pasados 12 meses (`COOKIES.dias`) o si cambia `COOKIES.version`.
- **Si cambia la política** (nuevas cookies, otra finalidad…): actualizar el texto y la tabla de la política, la fecha de «Última actualización» y subir `COOKIES.version` en el JS (por ejemplo, a la fecha del cambio). Así se vuelve a preguntar a todo el mundo.
- **Cambiar la elección**: enlace «Configurar cookies» del pie, o el botón dentro de la política de cookies.
- Si se retira un permiso ya dado, la página se recarga para que no siga funcionando nada de esa categoría.
- Si el navegador bloquea `localStorage`, la web funciona igual; simplemente volverá a preguntar en cada visita.

### Cuando se añada analítica (u otra categoría)

1. Poner el script bloqueado, sin que se ejecute: `type="text/plain"` y `data-cookies="analiticas"` (sirve con `src` o con código dentro). El JS lo activa solo si la persona acepta las analíticas.
2. Otra opción desde JS: `window.cookiesMB.permitido('analiticas')` o escuchar el evento `cookies:eleccion` en `document`.
3. Añadir cada cookie a la tabla de la política (nombre, finalidad, duración, tipo y si es de terceros), revisar privacidad (destinatarios y transferencias) y subir `COOKIES.version`.
4. Si al retirar el consentimiento quedan cookies de ese proveedor, borrarlas o explicarlo en la política.

### Textos legales (modales)

- **Aviso legal** (LSSI-CE): titular, objeto, condiciones de uso, propiedad intelectual (incluye la licencia OFL de las fuentes), responsabilidad, enlaces, legislación y jurisdicción.
- **Privacidad** (RGPD y LOPDGDD): responsable, datos y finalidades (WhatsApp, llamadas, datos técnicos del alojamiento), base legal, conservación, destinatarios (WhatsApp/Meta y **GitHub Pages**), transferencias internacionales, derechos, reclamación ante la AEPD.
- **Cookies**: qué son, tabla, cómo cambiar la elección y cómo borrarlas en cada navegador.
- Titular, NIF y email: «pendiente de publicar». **No inventar.**
- Cada texto termina con «Última actualización: 8 de noviembre de 2026». Actualizarla cuando cambie el texto.
- **Al pasar a dominio propio**: si cambia el alojamiento, revisar «Destinatarios» y «Transferencias internacionales» en privacidad (hoy nombran GitHub Pages).
- Revisión pendiente con asesoría antes de dar la web por definitiva.

## Pruebas

Antes de publicar cambios de maquetación, revisar a 390px (móvil) y 1280px (escritorio): sin scroll horizontal, la barra móvil no tapa el formulario ni el pie, y sin errores de JS.

Probar con un servidor local (`python -m http.server`), no abriendo el archivo: con `file://` Chrome no carga las fuentes locales.
