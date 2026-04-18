# CLAUDE.md — Fortuna Miel Artesanal

## Qué es este proyecto

Landing page estática para **Fortuna**, marca de miel artesanal multifloral de Puente Nacional, Santander (Colombia). Vende por domicilio en Mosquera, Funza y Madrid (Sabana Occidente).

Archivo único: `index.html` con CSS y JS embebidos. Sin framework, sin build step.

## Imágenes disponibles (`img/`)

| Archivo | Contenido |
|---|---|
| `frascos.jpg` | Frascos de miel — hero principal |
| `apiario.jpg` | Vista del apiario |
| `colmena.jpg` | Colmena |
| `cosecha.jpg` | Proceso de cosecha |
| `flora.jpg` | Flora del entorno |
| `abejas.jpg`, `abejas2.jpg` | Abejas en panal |
| `apicultoras.jpg` | Equipo / apicultoras |
| `panal.jpg` | Panal de miel |
| `logo.png`, `logo.jpg` | Logo de la marca |

## Paleta de colores

```css
--cream:  #F5F0E8   /* fondo principal */
--brown:  #2C1A0E   /* texto y fondos oscuros */
--amber:  #C8860A   /* acento principal */
--terra:  #8B4513   /* acento secundario */
--light:  #FAF7F2   /* fondo secciones claras */
--muted:  #7A6550   /* texto secundario */
--green:  #3D7A4A   /* badge disponible */
```

## Tipografías

- **Cormorant Garamond** (serif) — títulos y precios
- **DM Sans** (sans-serif) — cuerpo y UI

## Secciones de la página

1. `nav` — navegación fija con hamburger mobile
2. `#hero` — hero 2 columnas: contenido + imagen
3. `.band` — banda de datos (colmenas, altitud, etc.)
4. `#productos` — grid 2 columnas de producto cards con carrito
5. `#proceso` — proceso de producción
6. `#nosotros` — historia / equipo
7. `#contacto` — zona de entrega + WhatsApp
8. `footer`

## Funcionalidad JS embebida

- Carrito flotante (`.cart-bar`) — suma cantidades por producto
- Modal de pedido con formulario (nombre, barrio, pago)
- Envío por WhatsApp con mensaje pre-armado
- Animaciones scroll (`IntersectionObserver` + clase `.reveal`)
- Nav shrink al hacer scroll
- Contador animado en `.band-number[data-count]`

## Pendientes visuales

- [ ] Fotos reales en cards de producto (actualmente placeholder)
- [ ] Reemplazar `og:image` placeholder con imagen real
- [ ] Sección nosotros con `apicultoras.jpg`
- [ ] Optimizar imágenes (WebP, tamaños)

## Convenciones

- No usar frameworks — mantener HTML/CSS/JS puro
- Responsive con media queries embebidas al final del `<style>`
- Imágenes con `loading="lazy"` excepto hero (`eager`)
- WhatsApp link: `https://wa.me/57XXXXXXXXXX` — reemplazar con número real
