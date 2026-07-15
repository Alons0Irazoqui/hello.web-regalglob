# RegalGlob — Brief de Proyecto: Landing Page

Este documento es el **informe de negocio y dirección de diseño** para la creación de la landing page de **RegalGlob**. Sirve como fuente de verdad para vos (desarrollador) y para Claude mientras iteran sobre la plantilla base en HTML.

> **Cómo usar este documento:** ya se envió un prompt inicial a Claude para adaptar la plantilla base a este negocio. A partir de ahí, este README es el contexto de negocio que hay que mantener a mano (pegalo en el proyecto, en un `CLAUDE.md`, o compartilo directo en el chat) para que cada iteración con Claude sea consistente. **Podés y debés seguir iterando con Claude —dándole instrucciones, correcciones y ajustes— todas las veces que haga falta hasta lograr el resultado deseado.** No hay un límite de vueltas; el objetivo es la calidad final, no acertar a la primera.

---

## 1. Sobre el negocio

| Dato | Detalle |
|---|---|
| **Nombre** | RegalGlob |
| **Origen del nombre** | Juego de palabras entre "**Regal**o" (gift) + "**Glob**o" (balloon) — el logo confirma este concepto combinando un regalo con globos. |
| **Rubro (inferido)** | Negocio de **globos y regalos**: arreglos con globos, bouquets de globos, cajas/kits de regalo con globos, decoración de globos para eventos (cumpleaños, baby showers, aniversarios, San Valentín, etc.) |
| **Instagram** | https://www.instagram.com/regalglob |
| **TikTok** | https://www.tiktok.com/@regalglob4 |
| **Teléfono / WhatsApp** | 81 8210 0831 |

> ⚠️ **Nota sobre el teléfono:** el número fue provisto originalmente como `181 8210 0831` (11 dígitos). Se corrigió a `81 8210 0831` (10 dígitos), quitando el "1" inicial que correspondía a una lada de más — "81" ya es la lada de Monterrey/Nuevo León, México. Para el link de WhatsApp (`wa.me`), anteponer el código de país correspondiente (ej. `+52` si es México) antes de los 10 dígitos.

### ⚠️ Importante: no hay ficha de negocio completa del cliente

El cliente **no proporcionó** una descripción escrita del negocio, catálogo, precios, zona de reparto/servicio, horarios, ni testimonios. Todo lo anterior es una **inferencia razonable a partir del logo** (nombre + iconografía de globos y regalo). Por lo tanto:

- **Toda la información real de productos, servicios, fotos de arreglos, precios, zona de cobertura y tono de comunicación debe sacarse directamente de Instagram y TikTok** (posts, reels, bio, historias destacadas). Son la fuente primaria de contenido real del negocio.
- Si algo no se puede confirmar en redes, usar contenido genérico de buen gusto para el rubro (placeholders claramente editables) en vez de inventar datos específicos (precios, direcciones, promesas).
- Cualquier duda de negocio (nombre exacto, slogan, zona de entrega, etc.) resolverla revisando el perfil o preguntando directamente al cliente.

---

## 2. Identidad visual / Branding

### Logo

- Ubicación: [`imagenes/logo.jpeg`](imagenes/logo.jpeg)
- **Tarea obligatoria:** el archivo actual tiene **fondo blanco/sólido**. Hay que **quitarle el fondo** (dejarlo en PNG transparente) antes de usarlo en la web — tanto para el header/navbar como para la pantalla de carga (ver sección 4). Se puede resolver con una herramienta de remoción de fondo (remove.bg, Photoshop, rembg, etc.) y exportar en alta resolución.
- Con el fondo removido, generar también un **favicon** (formatos `.ico` / `.png` en varios tamaños) a partir del logo.

### Paleta de colores

Extraída algorítmicamente de los píxeles del logo (valores promedio de cada clúster de color). Son un **punto de partida fiel a la marca**, no valores oficiales del cliente — está bien que Claude/el desarrollador los ajuste levemente (tints/shades) para lograr contraste y accesibilidad (AA) en botones, textos y fondos.

| Color | Hex aprox. | Uso sugerido |
|---|---|---|
| 🎀 Rosa / Magenta (marca) | `#D0407A` | Color primario — texto "Regal", acentos, CTAs, detalles |
| 💜 Púrpura / Violeta (marca) | `#7752A4` | Color secundario — texto "Glob", globos, fondos de sección, hovers |
| 🌸 Rosa pastel claro | `#F2DCEB` | Fondos suaves, tarjetas, separadores de sección |
| 🤍 Blanco | `#FFFFFF` | Fondo base, espacios en blanco (estilo minimal) |
| ⚫ Negro / Gris oscuro | `#1A1A1A` – `#2B2B2B` | Tipografía principal sobre fondo claro, footer oscuro |

**Sugerencia de aplicación:** usar rosa y púrpura como pareja de marca (pueden combinarse en un **degradado diagonal rosa → púrpura** para títulos, botones o fondos hero), apoyados sobre mucho blanco/espacio negativo para mantener el look minimal-premium.

### Tipografía sugerida

- Encabezados: una tipografía moderna, elegante, con algo de personalidad (ej. *Playfair Display*, *Cormorant*, *Fraunces* o similar serif premium) **o** una sans-serif geométrica de alto contraste (ej. *Poppins*, *Sora*, *General Sans*) según el look final que se busque — priorizar algo que se sienta "high-end", no infantil, aunque el rubro sea festivo.
- Cuerpo de texto: sans-serif limpia y legible (ej. *Inter*, *Manrope*, *Plus Jakarta Sans*).
- Evitar tipografías tipo "comic"/infantiles pese a que el producto sean globos — el mandato de estilo es **premium y corporativo**, no lúdico-casero.

### Tono de marca

Festivo pero elegante: la comunicación debe transmitir que son **arreglos de regalo/globos de alta gama**, no una tienda genérica de piñatería. Fotografía cuidada, composición limpia, mensajes cortos y aspiracionales.

---

## 3. Dirección de diseño (obligatorio)

El estilo visual de la landing debe sentirse:

- **Premium / Enterprise / Corporativo** — como una marca establecida, no un negocio casero.
- **High-tech y elegante** — transiciones suaves, tipografía cuidada, jerarquía visual clara.
- **Minimalista** — mucho espacio en blanco, pocos elementos por pantalla, sin saturar de color ni texto.

En la práctica esto significa: layouts con "aire" (whitespace generoso), grillas alineadas, imágenes grandes y bien recortadas, paleta controlada (no usar más colores que los de la sección 2), microinteracciones sutiles (no efectos exagerados ni "ruidosos"), y consistencia total de espaciados/tamaños tipográficos en todo el sitio.

---

## 4. Efectos visuales y animaciones (obligatorio)

Estos elementos son requerimiento explícito del cliente, no opcionales:

1. **Pantalla de carga (loading screen)**
   - Debe mostrarse al cargar la página, con un **spinner/loader animado junto al logo del negocio** (logo ya sin fondo, ver sección 2).
   - Debe desvanecerse (fade-out) suavemente hacia el contenido una vez que la página terminó de cargar.

2. **Animaciones al hacer scroll**
   - Los elementos de cada sección deben **revelarse/animarse a medida que entran en el viewport** (fade-in + slight translate, por ejemplo), no aparecer todos de golpe.
   - Mantenerlas sutiles y consistentes (misma curva de animación/duración en todo el sitio) para que se sientan "premium" y no cargadas.

3. **Título del Hero (sección principal)** — dos efectos combinados sobre el texto principal:
   - **Efecto máquina de escribir (typewriter):** el título se escribe letra por letra al cargar la sección.
   - **Letras que cambian de color:** además del efecto de tipeo, las letras del título deben tener una animación de color (ya sea cambio cíclico, degradado animado entre los colores de marca —rosa/púrpura—, o efecto de "shimmer"). Ambos efectos deben verse elegantes y no infantiles, coherentes con el estilo premium/minimal del punto 3.

4. **Microinteracciones generales:** hover states suaves en botones/tarjetas/links, transiciones consistentes (200–400ms, easing suave), sin saltos bruscos.

> Nota para quien itere con Claude: si un efecto queda "cargado" o poco elegante, pedirle explícitamente a Claude que lo simplifique — el criterio de aceptación es que se vea premium y minimal, no que tenga la mayor cantidad de efectos posible.

---

## 5. Estructura sugerida de la landing page

Como no hay catálogo/copy oficial del cliente, esta es una estructura de referencia a validar/completar con contenido real de Instagram y TikTok:

1. **Loading screen** (ver sección 4)
2. **Header / Navbar** — logo, navegación, CTA de contacto (WhatsApp)
3. **Hero** — título con efectos (sección 4), subtítulo/propuesta de valor, CTA principal, imagen/fondo con globos
4. **Sobre nosotros** — breve historia/propuesta de valor de RegalGlob
5. **Productos / Servicios** — categorías de arreglos (cumpleaños, aniversarios, baby shower, corporativo, etc.) con imágenes reales sacadas de redes sociales
6. **Galería** — grid de fotos de arreglos reales (Instagram/TikTok)
7. **Cómo funciona / Proceso de compra** — pasos simples (elegir, pedir por WhatsApp, entrega)
8. **Testimonios** (si se encuentran en redes; si no, dejar sección lista para completar)
9. **Contacto / CTA final** — teléfono, WhatsApp flotante, redes sociales
10. **Footer** — logo, redes, datos de contacto, copyright

---

## 6. Assets disponibles

- [`imagenes/`](imagenes/) — carpeta con los archivos entregados por el cliente. **Actualmente solo contiene el logo** (`logo.jpeg`). Cualquier otra imagen (fotos de productos, arreglos, eventos) debe sacarse directamente de Instagram (@regalglob) y TikTok (@regalglob4).

---

## 7. Checklist técnico

- [ ] Quitar el fondo del logo y exportar en PNG transparente (alta resolución)
- [ ] Generar favicon a partir del logo sin fondo
- [ ] Implementar pantalla de carga con spinner + logo
- [ ] Implementar animaciones de scroll (reveal on scroll) en todas las secciones
- [ ] Implementar efecto typewriter + cambio de color en el título del Hero
- [ ] Aplicar paleta de colores de marca (sección 2) de forma consistente
- [ ] Sitio 100% responsive (mobile-first, ya que gran parte del tráfico vendrá de Instagram/TikTok)
- [ ] Botón flotante de WhatsApp con el número de contacto (confirmar formato correcto antes de linkear)
- [ ] Enlaces a Instagram y TikTok visibles (header y/o footer)
- [ ] Optimización de imágenes y performance (lazy loading, compresión)
- [ ] Revisión de contraste/accesibilidad de la paleta rosa/púrpura sobre blanco y sobre fondos oscuros

---

## 8. Flujo de trabajo con Claude

- Ya existe una plantilla base en HTML y un prompt inicial enviado a Claude para adaptarla a RegalGlob.
- A partir de acá, el trabajo es **iterativo**: dale instrucciones puntuales a Claude (ajustes de copy, diseño, animaciones, responsive, bugs, etc.) tantas veces como sea necesario hasta llegar al resultado esperado. No hay que resolver todo en una sola iteración.
- Usá este README como contexto de negocio en cada sesión para que las respuestas de Claude sean consistentes con la marca, la paleta y el estilo definidos acá.
- Si encontrás contenido real (fotos, textos, precios) en Instagram/TikTok que contradiga los supuestos de este documento, priorizá siempre la información real de redes sociales.
