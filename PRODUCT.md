# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users
Público general y prensa que exploran solos el estado de la universidad peruana, y decisores/analistas de política educativa que necesitan cifras claras y citables. El modo Presentar también sirve para proyectar las cifras clave ante una audiencia en vivo.

## Product Purpose
Hacer explorable «La universidad en cifras» (2.ª edición, Minedu — Digesu, Dipoda, noviembre 2026): una visualización interactiva y no oficial del informe sobre la educación universitaria en el Perú. Éxito: que alguien entienda quiénes estudian y enseñan, cuántos acceden y cómo es la oferta, sin leer el PDF.

## Positioning
Mismas cifras que el informe oficial, pero cada cuadro es un grupo de personas que se reacomoda según lo que se cuenta (idea «Land vs People» aplicada a la universidad), con exploración libre, interacciones tipo «adivina» y un modo Presentar para contarlo en charla. Los tres usos (explorar, adivinar, presentar) pesan igual.

## Operating Context
Se consulta en navegador (también móvil) o se proyecta en charlas con el modo Presentar. Fuente de datos: informe PDF y su texto extraído (`fuente/informe.pdf`, `fuente/informe.txt`); `fuente/build.py` genera datos/estructura a partir de él.

## Capabilities and Constraints
- Un solo `index.html` estático, sin frameworks ni dependencias externas (en el estado actual; se mantiene salvo decisión contraria).
- Cifras en español peruano: espacio como separador de millares y coma decimal (1 525 560; 12,3 %).
- No inventar, recalcular ni redondear datos fuera del informe; cada gráfico cita su fuente (SIRIES, Sunedu, ENAHO, SISFOH, Renacyt, Scopus).
- Debe permanecer visible que es una visualización no oficial.

## Brand Commitments
Crédito «by Liz Riveros · Crafter Research». Estilo de cuadros dinámicos inspirado en Land vs People (decisión ya tomada en el diseño actual).

## Evidence on Hand
Informe completo del Minedu en `fuente/informe.pdf` y `fuente/informe.txt`. No hay testimonios, métricas de uso ni validación con usuarios; no deben inventarse.

## Product Principles
1. La fidelidad a la cifra y su fuente va antes que el efecto visual.
2. Cada cuadro representa personas o instituciones reales; la interacción debe revelar proporciones, no decorar.
3. Funciona igual de bien leído a solas que proyectado en una sala.
4. Transparencia sobre el origen: es una versión no oficial del informe del Minedu.

## Accessibility & Inclusion
Legible en proyección y en móvil; texto mínimo de 12 px (criterio ya adoptado). Sin otro estándar formal confirmado.
