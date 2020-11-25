# Box Model 📦

Du point de vue de CSS chaque élément est un box (boîte). Nous allons apprendre comment ces boîtes fonctionnent afin de pouvoir gérer leurs dimentions leur positionement au sein d'une page HTML.

## Dimensions

Les quatres  propriétés `width`, `height`, `padding` et `border` agissent directement sur les dimensions d'un élément.

- `width` - la largeur de la boîte, par défaut, sa valeur est `auto`, en lire plus sur [MDN](https://developer.mozilla.org/fr/docs/Web/CSS/width)
- `height`- la hauteur de la boîte, par défaut, sa valeur est `auto`, en lire plus sur [MDN](https://developer.mozilla.org/fr/docs/Web/CSS/height)
- `padding` - raccourcie pour `padding-top` 👆, `padding-right` 👉, `padding-bottom` 👇 et `padding-left` 👈- les espacements internes dans l'élément , en lire plus sur [MDN](https://developer.mozilla.org/fr/docs/Web/CSS/padding)

```css
div {
/* top, right, bottom et left à 16px */
  padding: 16px;
/*
  padding-top: 16px;
  padding-right: 16px;
  padding-bottom: 16px;
  padding-left: 16px;
 */
}
```

```css
div {
/* top et bottom (↕️) à 16px et right et left (↔️) à 24px */
  padding: 16px 24px;
/*
  padding-top: 16px;
  padding-right: 24px;
  padding-bottom: 16px;
  padding-left: 24px;
*/
  
}
```

```css
div {
  /* top à 16px et right et left (↔️) à 24px, bottom à 32px  */
  padding: 16px 24px 32px;
/*
  padding-top: 16px;
  padding-right: 24px;
  padding-bottom: 32px;
  padding-left: 24px;
*/
}
```

```css
div {
/* top à 16px et right à 24px, bottom à 32px et left à 48px 👆👉👇👈 */
  padding: 16px 24px 32px 48px;
/*
  padding-top: 16px;
  padding-right: 24px;
  padding-bottom: 32px;
  padding-left: 48px;
*/
}
```

https://codepen.io/alyra/pen/XWXWRXJ

- `border` - une propriété raccourcie qui permet de définir les propriétés liées à la bordure `border-width`, `border-style` et `border-color`. Il existe aussi `border-top` (`border-top-width`, `border-top-style`, `border-top-color`), `border-right`, `border-bottom` et `border-left`.

```css
div {
  border: 2px solid red;
}
```

```css
div {
  border-bottom: 1px solid;
}
```


A l'occasion nous allons parler aussi de la propriété `margin` - la taille des marges sur les quatre côtés de l'élément, un raccourci pour `margin-top`, `margin-right`, `margin-bottom` et` margin-left`.

```css
div {
/* top, right, bottom et left à 16px */
  margin: 16px;
/*
  margin-top: 16px;
  margin-right: 16px;
  margin-bottom: 16px;
  margin-left: 16px;
 */
}
```

```css
div {
/* top et bottom (↕️) à 16px et right et left (↔️) à 24px */
  margin: 16px 24px;
/*
  margin-top: 16px;
  margin-right: 24px;
  margin-bottom: 16px;
  margin-left: 24px;
*/
  
}
```

```css
div {
  /* top à 16px et right et left (↔️) à 24px, bottom à 32px  */
  margin: 16px 24px 32px;
/*
  margin-top: 16px;
  margin-right: 24px;
  margin-bottom: 32px;
  margin-left: 24px;
*/
}
```

```css
div {
/* top à 16px et right à 24px, bottom à 32px et left à 48px 👆👉👇👈 */
  margin: 16px 24px 32px 48px;
/*
  margin-top: 16px;
  margin-right: 24px;
  margin-bottom: 32px;
  margin-left: 48px;
*/
}
```

Il est important de comprendre la différence entre `margin` et `padding`

https://cdpn.io/alyra/debug/NWRKLWy

### inline & block

`p, div, h1-h6, section, ...`, en fait la majorité des éléments est type `block`  
`span, em, strong, i, b, ins, del ...` - ont le caractère en-ligne `inline`

Le comportement d'un élément peut être modifier avec la propriété `display`

https://codepen.io/alyra/pen/YzwKodK

### Collapsing margins (marges fusionnées)

Les marges top et bottom des blocs sont parfois fusionnées en une seule marge.  
La taille de la marge = la plus grande des deux marges fusionnées. C'est ce qu'on appelle _collapsing margins._

Ceci concerne les situations suivantes:

- des éléments voisins adjacents
- aucun contenu séparant le parent et ses descendants
- bloc vides

https://codepen.io/alyra/pen/QWyWprr

### box-sizing

```css
* {
  box-sizing: border-box;
}
```

```css
html {
  box-sizing: border-box;
}
*,
*:before,
*:after {
  box-sizing: inherit;
}
```

[Playground](https://cdpn.io/alyra/debug/416abba364963b2efce1b467ed776f87)
