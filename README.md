# Raíz Coffee — Ejercicio de recreación visual en CSS

Recreación visual de la web de [Blank Street Coffee](https://www.blankstreet.com) realizada como ejercicio de CSS. La estructura HTML, el layout y todos los estilos son de elaboración propia; el contenido de texto ha sido reemplazado íntegramente por una marca ficticia (**Raíz Coffee**) para no reproducir el copy original.

> **Nota:** Este proyecto es un ejercicio educativo sin fines comerciales. No tiene ninguna afiliación con Blank Street Coffee.

---

## Vista general

Una landing page minimalista de una cafetería ficticia con identidad de specialty coffee. El diseño es mobile-first, con un único breakpoint para desktop a `1024px`.

---

## Secciones

| Sección | Descripción |
|---|---|
| **Navbar** | Fija, transparente al inicio. Al hacer scroll invierte colores y aparece borde inferior animado. |
| **Hero** | Pantalla completa con imagen de fondo, título de temporada y descripción de bebidas. |
| **Rewards** | Texto + imagen de producto. Presenta el programa de puntos de la marca. |
| **Shop** | Sección con imagen de fondo, acceso a la tienda de merchandise. |
| **More** | Dos tarjetas: app móvil y sobre la marca. Grid de 2 columnas en desktop. |
| **Footer** | Copyright, redes sociales, horarios y contacto. |

---

## Stack

- **HTML5** semántico
- **CSS3** — sin frameworks ni preprocesadores
- **JavaScript** vanilla — únicamente para el estado de scroll del navbar

---

## Técnicas de CSS aplicadas

- Custom properties (`--color-*`, `--font-size-*`, `--spacing-*`)
- Mobile-first con un solo breakpoint (`min-width: 1024px`)
- **Flexbox** para navbar, hero, rewards, shop y footer
- **CSS Grid** para la sección "More" (1 columna → 2 columnas) y el footer en desktop
- `background-image` con `cover` y `center` para las secciones hero y shop
- Animaciones de estado con `transition` y `cubic-bezier` en navbar (color, borde, sombra)
- `position: fixed` con cambio de estilo reactivo vía JS + clase CSS

---

## Comportamiento del navbar

El navbar parte transparente sobre la imagen del hero. Al superar `100px` de scroll, JavaScript añade la clase `.scrolled` que activa mediante transición CSS:

- Fondo `--color-bg` (crema)
- Inversión de color en logo, links y botón
- `box-shadow` sutil en el `.navbar`
- `border-bottom` en el `.navbar__container` con el mismo color que el footer

---

## Tipografía

Ambas fuentes están auto-alojadas en `assets/fonts/`.

| Variable | Fuente | Uso |
|---|---|---|
| `--font-style-title` | Switzer | Títulos y logo |
| `--font-style-base` | Satoshi | Cuerpo, links y botones |

---

## Estructura de archivos

```
BlankStreetClone/
├── index.html
├── css/
│   ├── styles.css        # Todos los estilos del proyecto
│   └── fonts.css         # @font-face para Satoshi y Switzer
├── js/
│   └── components.js     # Scroll listener para el navbar
└── assets/
    ├── fonts/            # Satoshi y Switzer (OTF, TTF, WOFF)
    └── img/              # Imágenes de las secciones
```

---

## Contenido ficticio — Raíz Coffee

El copy, la marca y todos los datos del sitio son inventados:

- **Nombre:** Raíz Coffee
- **Ubicación:** Brooklyn, NY
- **Temporada actual:** Summer 2026
- **Bebidas destacadas:** Mango Cardamom Latte, Hibiscus Cold Brew, Coconut Horchata Matcha
- **Redes:** @raizcoffee
- **Horario:** Lun–Dom, 7am–9pm

---

## Referencia

Layout visualmente inspirado en **[Blank Street Coffee](https://www.blankstreet.com)**.
