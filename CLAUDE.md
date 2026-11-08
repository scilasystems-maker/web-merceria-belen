# Mercería Belén — web

Web de **Mercería Belén**, mercería de barrio en La Viña (Lorca, Murcia). Cliente de **ScilaAI**.

- Repo: `scilasystems-maker/web-merceria-belen` (rama `main`)
- Publicada con GitHub Pages: https://scilasystems-maker.github.io/web-merceria-belen/
- Todo lo que hay en el repo se publica: cualquier archivo que se suba (incluido este) es accesible por URL.

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

## Datos que aparecen en la web y NO están confirmados

Revisar con el cliente antes de darlos por buenos:

- **Domingo cerrado** (se deduce del horario, pero no está dicho).
- **WhatsApp en el 690 70 38 62**: todo el formulario y el botón flotante dependen de esto.
- **Email** `belenpadilla39@gmail.com` (pie de página).
- **Dominio** `www.merceriabelen.es` (canonical, og:url, JSON-LD). Hoy no es la URL real de la web.
- **Coordenadas** 37.66462, -1.70387 (JSON-LD y enlace a Google Maps).
- `alternateName: "Mercería Lencería Belén"` y `priceRange: "€€"` en el JSON-LD.
- Textos comerciales: «principales marcas del sector», «precios muy competitivos», «Primeras marcas», «Buenos precios», «si no lo tenemos, te decimos dónde encontrarlo».
- Productos concretos que no están en los datos: pijamas, fajas, complementos, canastilla, ropa interior de caballero.
- Festivos y horario de verano.
- Redes sociales (no hay ninguna en la web).
- Enlace de créditos `https://www.scilaai.com`.

## Pendientes `<!-- EDITAR -->` en index.html

1. Dominio definitivo (canonical) — línea ~10.
2. `og:image` 1200×630 con foto real del escaparate — línea ~17.
3. Confirmar horario actual, festivos y si cambia en verano — sección Visítanos.
4. Confirmar que el 690 70 38 62 tiene WhatsApp — antes del formulario.
5. Confirmar email y redes sociales — pie de página.
6. Completar los datos legales (en amarillo) y revisar con asesoría — modales legales:
   - Titular (nombre y apellidos / razón social)
   - NIF
   - Email de contacto (aviso legal y privacidad)

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
| — | Cabecera fija tipo píldora | `#cabecera` | Logo botón + menú + botón llamar + hamburguesa |
| — | Hilo cosido | `.hilo` | SVG que se «cose» al hacer scroll (oculto < 700px) |
| — | Portada | `#inicio` | H1 «Del botón al conjunto perfecto», estado abierto/cerrado, escena ilustrada con parallax |
| — | Cinta métrica | `.cinta` | Marquesina con las categorías |
| 01 | La tienda | `#tienda` | Bento: Mercería, Lencería y corsetería, Bebé y niño, Moda mujer, Moda hombre |
| 02 | Tallas grandes | `#tallas` | Bloque coral con cintas métricas |
| 03 | Por qué Belén | `#porque` | 4 motivos |
| 04 | Visítanos | `#visitanos` | Horario (resalta hoy) + mapa ilustrado + Google Maps |
| 05 | Pregúntanos | `#pregunta` | Formulario que abre WhatsApp con el mensaje (no guarda datos) |
| 06 | Preguntas frecuentes | `#faq` | `<details>` |
| — | Pie | `.pie` | Lema grande, datos, enlaces legales, créditos ScilaAI |
| — | WhatsApp flotante | `#wa-flotante` | |
| — | Modales legales | `dialog#modal-*` | Aviso legal, privacidad, cookies |

## JavaScript (en línea, al final)

- Año automático en el pie.
- Menú móvil.
- Abierto/cerrado con hora de Madrid: objeto `HORARIO` en minutos (si cambia el horario, cambiarlo aquí, en la lista `#horario`, en el FAQ y en el JSON-LD).
- Aparición al hacer scroll (`.aparece` + IntersectionObserver).
- Hilo que se cose con el scroll.
- Parallax de la escena con el ratón.
- Formulario → `wa.me` con texto prellenado, trampa antispam `.trampa`.
- Modales legales con `<dialog>`.
- Respeta `prefers-reduced-motion`.

## Sin cookies

No hay analítica ni mapas embebidos. Solo Google Fonts como recurso de terceros (está declarado en la política de cookies). Si se añade algo de terceros, actualizar la política.
