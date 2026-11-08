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
- Sin frameworks ni build: un único `index.html` con HTML, CSS y JS en línea. Mantenerlo así salvo decisión explícita.
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

## Pendientes `<!-- EDITAR -->` en index.html

1. Demo en GitHub Pages: `noindex` y sin canonical/og:url; revertir con dominio propio — `<head>`.
2. `og:image` 1200×630 con foto real del escaparate — `<head>`.
3. Confirmar horario actual, festivos y si cambia en verano — sección Visítanos.
4. Confirmar que el 690 70 38 62 tiene WhatsApp — antes del formulario.
5. Confirmar email y redes sociales — pie de página.
6. Sustituir los textos `.pendiente` de los modales legales por titular, NIF y email reales, y revisar con asesoría.

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
| `--coral-osc` | `#B8323F` | Hover del coral, etiquetas |
| `--mostaza` | `#E9A93A` | Cinta métrica, subrayados, acentos sobre fondo oscuro |
| `--salvia` | `#8FA88A` | Botón ilustrado |
| `--rosa` | `#F3C9C4` | Tarjeta lencería, disco de la portada |

Otros fijos: `#DCE5D6` (tarjeta bebé), `#E7DCCB` (mapa), `#2FA36B` (punto «abierto»), `#25D366` (WhatsApp).

Otros tokens: `--radio: 22px`, `--sombra`, `--ancho: 1180px`.

### Tipografías (Google Fonts)

- **Fraunces** (`--serif`), variable con ejes `opsz`, `wght` 300–800 y `SOFT` (se usa `SOFT 100`). Títulos, cifras, cursivas en coral.
- **Manrope** (`--sans`) 400/500/600/700. Texto, botones, etiquetas.

## Estructura de la página

| # | Sección | id / clase | Contenido |
|---|---|---|---|
| — | Cabecera fija tipo píldora | `#cabecera` | Logo botón + menú + botón llamar (oculto ≤ 640px) + hamburguesa |
| — | Hilo cosido | `.hilo` | SVG que se «cose» al hacer scroll. Escritorio: zigzag de lado a lado. < 700px: pespunte fino pegado al borde izquierdo (x 2–10px), fuera del texto |
| — | Portada | `#inicio` | H1 «Del botón al conjunto perfecto» (se cose al cargar), estado abierto/cerrado, escena ilustrada con parallax, botón principal con pespunte |
| — | Cinta métrica | `.cinta` | Marquesina con las categorías |
| 01 | La tienda | `#tienda` | Bento: Mercería, Lencería y corsetería, Bebé y niño, Moda mujer, Moda hombre |
| 02 | Tallas grandes | `#tallas` | Bloque coral con cintas métricas |
| 03 | Por qué Belén | `#porque` | 4 motivos |
| 04 | Visítanos | `#visitanos` | Horario (resalta hoy) + mapa ilustrado + Google Maps |
| 05 | Pregúntanos | `#pregunta` | Formulario que abre WhatsApp con el mensaje (no guarda datos) |
| 06 | Preguntas frecuentes | `#faq` | `<details>` |
| — | Pie | `.pie` | Lema grande, datos, enlaces legales, créditos ScilaAI |
| — | WhatsApp flotante | `#wa-flotante` | Solo > 640px |
| — | Barra de contacto móvil | `#barra-movil` | Solo ≤ 640px: Llamar / WhatsApp / Cómo llegar, fija abajo. `body` lleva `padding-bottom` para que no tape el pie |
| — | Modales legales | `dialog#modal-*` | Aviso legal, privacidad, cookies |

## JavaScript (en línea, al final)

- Año automático en el pie.
- Menú móvil.
- Abierto/cerrado con hora de Madrid: objeto `HORARIO` en minutos (si cambia el horario, cambiarlo aquí, en la lista `#horario`, en el FAQ y en el JSON-LD).
- Festivos y vacaciones: lista `FESTIVOS` (ver «Cómo añadir festivos y vacaciones»). Si hoy está en la lista, el indicador dice «Hoy cerrado por festivo / por vacaciones · abrimos …» y la tabla marca esa fila.
- Aparición al hacer scroll (`.aparece` + IntersectionObserver).
- Hilo que se cose con el scroll (dos trazados: escritorio y móvil < 700px; se recalcula al redimensionar o girar).
- La barra móvil se oculta (`.oculta`) mientras se escribe en el formulario, para que no tape el campo con el teclado abierto.
- Parallax de la escena con el ratón.
- Formulario → `wa.me` con texto prellenado, trampa antispam `.trampa`.
- Modales legales con `<dialog>`.
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

## Sin cookies

No hay analítica ni mapas embebidos. Solo Google Fonts como recurso de terceros (está declarado en la política de cookies). Si se añade algo de terceros, actualizar la política.

## Pruebas

Antes de publicar cambios de maquetación, revisar a 390px (móvil) y 1280px (escritorio): sin scroll horizontal, la barra móvil no tapa el formulario ni el pie, y sin errores de JS.
