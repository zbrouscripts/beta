# Personnalisation

## Presets

Chacun des 3 slots enregistre toute sa configuration. Le joueur peut utiliser un slot fixe ou le mode aléatoire.

Each slot stores:

- Phrase text.
- Text color.
- Glow color and intensity.
- Font and text size.
- Position.
- Animation and speed.
- Killer-line visibility, color, font, size and alignment.
- Whether the slot participates in random mode.

## Fonts

FraseKill includes **100 fonts**. Saved profiles reference font keys, so avoid renaming existing keys after launch.

## Animations

Includes 25 animation styles plus `none`, including pop, slides, zoom, bounce, glitch, typewriter and per-letter effects.

## Menu colors

Les couleurs du menu sont regroupées à la fin de `web/styles.css` dans `ZBROU FRASEKILL THEME`. Aucun JavaScript à modifier.

```css
/* ZBROU FRASEKILL THEME */
:root {
    --accent: #0E58D8;
}
```

## Preview

The preview supports 16:9, 16:10, 4:3, 5:4 and 21:9 and uses its own virtual canvas so text scale is represented consistently inside each ratio.
