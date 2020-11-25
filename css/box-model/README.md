# Box Model 📦

Du point de vue de CSS chaque élément est un box (boîte). Nous allons apprendre comment ces boîtes fonctionnent afin de pouvoir gérer leurs dimentions leur positionement au sein d'une page HTML.

## Dimensions

Les trois propriétés :

- `width` - la largeur de la boîte, par défaut, sa valeur est `auto`, en lire plus sur [MDN](https://developer.mozilla.org/fr/docs/Web/CSS/width)
- `height`- la hauteur de la boîte, par défaut, sa valeur est `auto`, en lire plus sur [MDN](https://developer.mozilla.org/fr/docs/Web/CSS/height)
- `padding` - raccourcie pour `padding-top` , `padding-right`, `padding-bottom` et `padding-left` - les espacements internes dans l'élément , en lire plus sur [MDN](https://developer.mozilla.org/fr/docs/Web/CSS/padding)

```css
p {
  // top, right, bottom et left à 16px
  padding: 16px;
}
```

```css
p {
  // top et bottom () à 16px et right et left à 24px
  padding: 16px 24px;
}
```

- `border`

agissent directement sur les dimensions d'un élément.

A l'occasion nous allons parler aussi de la propriété `margin`.
Il est important de comprendre la différence entre `margin` et `padding`

https://cdpn.io/alyra/debug/NWRKLWy

### inline & block

`p, div, h1-h6, section, ...`, en fait la majorité des éléments est type `block`  
`span, em, strong, i, b, ins, del ...` - ont le caractère en-ligne `inline`

Le comportement d'un élément peut être modifier avec la propriété `display`

https://codepen.io/alyra/pen/YzwKodK

### margin & padding syntax

```css
div {
  padding: 20px;
  /*
  padding-top: 20px;
  padding-right: 20px;
  padding-bottom: 20px;
  padding-left: 20px;
  */
}
```

```css
div {
  padding: 20px 30px;
  /*
  padding-top: 20px;
  padding-right: 30px;
  padding-bottom: 20px;
  padding-left: 30px;
  */
}
```

```css
div {
  padding: 20px 30px 40px;
  /*
  padding-top: 20px;
  padding-right: 30px;
  padding-bottom: 40px;
  padding-left: 30px;
  */
}
```

```css
div {
  padding: 20px 30px 40px 50px;
  /*
  padding-top: 20px;
  padding-right: 30px;
  padding-bottom: 40px;
  padding-left: 50px;
  */
}
```

https://codepen.io/alyra/pen/XWXWRXJ

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
