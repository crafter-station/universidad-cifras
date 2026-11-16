---
name: La universidad en cifras
description: Visualización editorial no oficial del informe del Minedu, hecha de cuadros que son personas.
colors:
  paper-green: "#EEF4EC"
  forest-ink: "#0E1F18"
  moss-mute: "#4F6B5D"
  sage-line: "#C9D7CB"
  card-paper: "#F6FAF4"
  soft-sage: "#DCE7DB"
  public-terracotta: "#C2492B"
  private-forest: "#173F31"
  third-sage: "#5F8F75"
  neutral-grey: "#A8B2A6"
  highlight-ochre: "#B07A12"
  teal-ramp-dark: "#1D5560"
  teal-ramp-mid: "#3C8791"
  teal-ramp-light: "#9CCBD0"
  night-bg: "#07100D"
  night-ink: "#EEF4EC"
  night-mute: "#8FB09E"
  night-line: "#1F3329"
  night-card: "#0D1A14"
  night-public: "#E8704F"
  night-private: "#CFE7D2"
typography:
  display:
    fontFamily: "Instrument Serif, Georgia, serif"
    fontSize: "clamp(52px, 10vw, 120px)"
    fontWeight: 400
    lineHeight: 0.94
    letterSpacing: "-0.03em"
  headline:
    fontFamily: "Instrument Serif, Georgia, serif"
    fontSize: "clamp(34px, 6vw, 60px)"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: "-0.025em"
  title:
    fontFamily: "Instrument Serif, Georgia, serif"
    fontSize: "clamp(21px, 2.5vw, 25px)"
    fontWeight: 400
    lineHeight: 1.15
    letterSpacing: "-0.015em"
  body:
    fontFamily: "Geist, Inter, ui-sans-serif, system-ui, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: "Geist Mono, ui-monospace, Menlo, monospace"
    fontSize: "12px"
    fontWeight: 400
    letterSpacing: "0.02em"
rounded:
  sm: "2px"
  md: "4px"
  pill: "99px"
spacing:
  sm: "8px"
  md: "16px"
  lg: "28px"
  xl: "64px"
components:
  button-pill:
    backgroundColor: "transparent"
    textColor: "{colors.forest-ink}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "5px 12px"
  button-pill-hover:
    backgroundColor: "{colors.forest-ink}"
    textColor: "{colors.paper-green}"
  segment-selected:
    backgroundColor: "{colors.forest-ink}"
    textColor: "{colors.paper-green}"
    rounded: "{rounded.pill}"
    padding: "6px 13px"
  guess-panel:
    backgroundColor: "{colors.forest-ink}"
    textColor: "{colors.paper-green}"
    rounded: "{rounded.md}"
    padding: "22px"
  search-field:
    backgroundColor: "{colors.card-paper}"
    textColor: "{colors.forest-ink}"
    rounded: "{rounded.md}"
    padding: "9px 12px"
---

# Design System: La universidad en cifras

## Overview

**Creative North Star: "El cuaderno verde de cifras"** *(propuesto a partir del código; por confirmar)*

Una pieza editorial que se lee como un informe bien compuesto, no como un panel de control. Fondo verde papel, tinta verde casi negra, una sola voz cálida (terracota) para lo público. Los números grandes en serif llevan la jerarquía; el resto es monoespaciado y discreto. Los gráficos son cuadros que representan personas y se reacomodan, en la línea de Land vs People.

Densidad media, mucho aire entre secciones, líneas finas en lugar de cajas. La estructura se marca con filetes de 1 px, no con sombras. La interfaz se retira: el dato manda.

**Key Characteristics:**
- Serif de gran tamaño para cifras y titulares; mono para etiquetas y fuentes.
- Paleta verde-salvia con acento terracota; modo oscuro verde noche.
- Cuadros (2 px de radio) como unidad visual de todos los gráficos.
- Plano: sin sombras, profundidad por filetes y tono.
- Movimiento solo para reacomodar datos y revelar secciones.

## Colors

Paleta tonal verde con un único acento cálido; el acento significa «pública» y se usa con moderación.

### Primary
- **Terracota Pública** (#C2492B; en oscuro #E8704F): universidades públicas, cursiva del título, barra de progreso, marcador «tú» y acentos clave.
- **Verde Bosque Privada** (#173F31; en oscuro #CFE7D2): universidades privadas, logotipo, rangos de ingreso.

### Secondary
- **Salvia Tercera** (#5F8F75) y **Gris Salvia** (#A8B2A6): tercera categoría (por ejemplo, licenciadas sin clasificar) y datos sin categoría.
- Serie categórica `--c0…--c10` para gráficos con varias categorías (turquesa, malva, oliva, ocre, etc.), con variante clara para el modo oscuro.

### Semantic data colors
- **Terracota** (`--pub`) y **Verde Bosque** (`--pri`) significan solo gestión pública/privada.
- **Malva** (`--c7`) mujeres, **Turquesa** (`--c4`) varones; **Marrón** (`--c6`) Lima, **Salvia** (`--c2`) resto del país; **Verde-azul** (`--c9`) ordinarios, **Oliva** (`--c8`) contratados.
- **Rampa verde-azulada** (`--s1…--s3`) para datos ordinales: dedicación, pobreza, empleo, edad.
- **Ocre** (#B07A12; oscuro #E3B24A, `--hi`): énfasis puntual (Perú, «tú», desempleo). Nunca significa gestión.

### Neutral
- **Papel Verde** (#EEF4EC): fondo de página. **Tarjeta Papel** (#F6FAF4): campos y superficies. **Salvia Suave** (#DCE7DB): pistas de barras, cabeceras sticky.
- **Tinta Bosque** (#0E1F18): texto y paneles invertidos. **Musgo Apagado** (#4F6B5D): texto secundario. **Filete Salvia** (#C9D7CB): líneas.
- Modo oscuro: **Noche** (#07100D) con tinta #EEF4EC; sigue `prefers-color-scheme` y `data-theme`.

### Named Rules
**The One Meaning Rule.** Cada color significa una sola cosa en todo el sitio: terracota = pública; el énfasis puntual usa ocre. Las etiquetas sobre rellenos eligen tinta clara u oscura según contraste.
**The Tonal Dark Rule.** El modo oscuro reasigna los mismos roles, no invierte a ciegas; cada categoría conserva su identidad.

## Typography

**Display Font:** Instrument Serif (con Georgia)
**Body Font:** Geist (con Inter, system-ui)
**Label/Mono Font:** Geist Mono (con ui-monospace)

**Character:** Serif editorial de contraste suave para las cifras, sans neutra para leer, mono para lo técnico: fuentes, etiquetas, leyendas. Las fuentes se cargan desde Google Fonts.

### Hierarchy
- **Display** (400, clamp 52–120 px, 0.94): título H1; el número grande usa clamp 60–150 px y en modo Presentar hasta 260 px.
- **Headline** (400, clamp 34–60 px, 1): título de sección H2.
- **Title** (serif 400, clamp 21–25 px, 1.15): título de cada gráfico; enuncia la conclusión, no el tema.
- **Body** (400, 16–17 px, 1.55): introducciones y texto corrido; máximo ~600 px de ancho.
- **Label** (400, 12–12.5 px, mono, +0.02em): navegación, controles, fuentes (`.src`), leyendas. Mínimo absoluto de 12 px.

### Named Rules
**The Number Is the Headline Rule.** La cifra clave va en serif grande; la explicación, en sans pequeña debajo.
**The 12px Floor Rule.** Ningún texto baja de 12 px.

## Layout

Columna única centrada de 1080 px máx. con 16 px de gutter. Secciones con 64 px de padding vertical separadas por filetes. Rejillas de 2 y 3 columnas con 28 px de hueco que colapsan a una columna bajo 760 px. La navegación es sticky de 52 px con enlaces desplazables y botones Presentar y Tema fijos a la derecha. El contador vivo de los cuadros queda fijo bajo la navegación al desplazar.

## Elevation & Depth

Plano por defecto. La profundidad se logra con filetes de 1 px, cambios de tono (`soft`, `card`) y un desenfoque de fondo (10 px) solo en la navegación y el contador fijo. No hay sombras en reposo; el hover usa contorno de 2 px o brillo.

### Named Rules
**The Hairline Rule.** Se separa con un filete de 1 px, no con cajas ni sombras.

## Shapes

Geometría casi recta: cuadros y barras con 2 px de radio, campos y paneles con 4 px, y píldoras completas (99 px) solo para controles y enlaces de navegación. El cuadrado es la unidad de la visualización.

## Components

### Buttons
- **Shape:** píldora (99 px).
- **Primary / default:** transparente, filete 1 px, texto mono 12 px, padding 5×12 px.
- **Hover:** se invierte a tinta sobre papel.
- **Segmented control:** contenedor píldora con filete; opción activa rellena de tinta con texto de fondo (`aria-pressed`).

### Chips / Legend
- Botones de texto con un cuadrito de color de 9 px; al desactivar bajan a 35 % de opacidad y se tachan.

### Cards / Containers
- Sin caja: un filete superior y 16 px de padding. Título 15 px, subtítulo 13.5 px en musgo.

### Inputs / Fields
- Fondo tarjeta, filete 1 px, radio 4 px, 14 px de texto, padding 9×12 px. Lista de resultados con cabeceras sticky en mono mayúscula.

### Navigation
- Sticky, translúcida con blur; enlaces mono 12 px en píldora, el activo se invierte; barra de progreso de 2 px en terracota.

### Cuadros dinámicos (signature)
- Cada cuadro es una persona o universidad; se posiciona absoluto y se reacomoda con transición de 0.9 s al cambiar universo o métrica. Hover con contorno de tinta. Un número vivo y una frase narrativa en serif acompañan el cambio.

### Panel de adivinar
- Bloque invertido (tinta con texto claro), pregunta en serif, deslizador con acento terracota, resultado que se revela.

### Modo Presentar
- Pantalla completa con cifra enorme, texto de apoyo de 20–34 px, fuente y barra de progreso; navegable por teclado.

## Do's and Don'ts

### Do:
- **Do** usar un cuadro por unidad real y reacomodarlo en lugar de crear/borrar elementos.
- **Do** citar la fuente en mono 12 px bajo cada gráfico.
- **Do** formatear cifras en español peruano: 1 525 560; 12,3 %.
- **Do** respetar `prefers-reduced-motion` y los dos modos de color.
- **Do** mantener visible el aviso de visualización no oficial.

### Don't:
- **Don't** usar sombras, degradados decorativos ni tarjetas con caja.
- **Don't** bajar de 12 px de texto.
- **Don't** usar terracota fuera de lo público o del énfasis clave.
- **Don't** redondear o recalcular cifras del informe por razones estéticas.
