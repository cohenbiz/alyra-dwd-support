# Couleurs 🌈

CSS nous permet de colorier nos pages, en particulier avec des propriétés :  
- `background-color`
- `color`
- `border`
- `box-shadow`
- `text-shadow`

Il y a plusieurs possibilités pour décrire une couleur. Voici quelques exemples pour de décrire la même nuance du rouge:

- `red`  
- `#ff0000` 
- `#f00`  
- `rgb(255, 0, 0)`  
- `rgba(255, 0, 0, 0)`  
- `rgb(100%, 0, 0)`  
- `hsl(0, 100%, 50%)`

Nous allons maintenant déchiffrer tout cela.

## Couleurs par mot-clé

La première possibilité est d'utiliser le nom de la couleur [keyword](https://developer.mozilla.org/fr/docs/Web/CSS/Type_color#Les_mots-cl%C3%A9s) (mot-clé) : `red`, `black`, `tomato`, `cornflowerblue`, ...., `transparent` et `currentColor`.

De cette façon nous pouvons décrire **147** couleurs différentes, sans compter `transparent` et `currentColor`. Voici un autre [site que les présente](http://www.colors.commutercreative.com/)).

De cette façon, nous sommes capables de référencer une minime partie des couleurs qui peuvent être affichées sur l'écran. Et si nous voulons aller au-déla ?

## Anatomie de la couleur

Chaque pixel sur l'écran est composé de trois petits points appelés luminophores entourés d'un masque noir. Les trois luminophores distincts produisent respectivement de la lumière <span style="color:red;">rouge</span>, <span style="color:lime">verte</span> et <span style="color:blue;">bleue.</span>

Pour contrôler la couleur de chaque pixel sur l'écran, le système d'exploitation consacre une quantité de mémoire à chaque pixel.

Sur les premiers écrans en noir et blanc, pixel est allumé (1) ou éteint (0), un seul morceau de mémoire est affecté à chaque pixel - un bit de memoire.

Sur les écrans modernes 8 bits de mémoire sont affectés pour chaque couleurs (rouge, verte et bleue). Cela donne 2<sup>8</sup> = **256** valueurs possibles pour la couleur rouge, **256** pour la couleur verte et **256** pour la bleue, donc:

256 x 256 x 256 = **16 777 216** couleurs

## Format `rgb` et `rgba`

**rgb, rgba**  décrit des intensités du rouge (r), vert (g) et b (bleu) + opacité a (alpha)

[Playground - Couleurs RGB expliquées](https://cdpn.io/alyra/debug/b2c543699a8868342fb23ac6c9f6f73d)

```
p {
  color: rgb(255, 0, 0);
  background: rgb(255, 0, 0, 0.1);
}
```

## Format hexadecimal (#)

Le format **hexadecimal** fonctionne comme le format `rgb`, il regroupe des intensités du rouge, vert et bleu mais representés en système hexadécimal.

Vous pouvez en lire davantage dans [cet article sur smashingmagazine.](https://www.smashingmagazine.com/2012/10/the-code-side-of-color/)

![""](https://wptemplates.pehaa.com/assets/alyra/rgbtohex.png)

[![Le fameux Quiz du Professeur Hervé B.\*](https://wptemplates.pehaa.com/assets/alyra/quizz-rvb.png)](https://cdpn.io/alyra/debug/616e97467780239fc8927073fe284ec5)

## Format `hsl` et `hsla` 

Le format couleur HSL, répresente une couleur pas ses : 
- teinte `h` (hue)
- saturation `s`
- clarté `l` (lightness)

[HSL Color Picker par Marton Borbely](https://codepen.io/HunorMarton/full/dvXVvQ)

Le format `hsl` est particulierement pratique pour gérér :

- les nuances et ombres (**juste le 3e paramètre change**):

```
/* Teinte de base */
background-color: hsl(14, 76%, 55%);

/* Plus foncée */
background-color: hsl(14, 76%, 75%);

/* Plus claire */
background-color: hsl(14, 76%, 35%);
```

- couleurs complémentaires (ajoter 180 - demi-tour au 1e paramètre):

```
/* Teinte de base */
color: hsl(14, 76%, 55%);

/* Couleur complémentaire */
color: hsl(194, 76%, 55%);
```

- couleurs complémentaires adjacentes (+/-120 au 1e paramètre):

```
/* Teinte de base */
color: hsl(14, 76%, 55%);

/* Couleur complémentaire adj. 1 */
color: hsl(134, 76%, 55%);

/* Couleur complémentaire adj. 1 */
color: hsl(254, 76%, 55%);
```

- couleurs similaires (analogous) (+/-30 au 1e paramètre):

```
/* Teinte de base */
color: hsl(14, 76%, 55%);

/* Couleur complémentaire adj. 1 */
color: hsl(44, 76%, 55%);

/* Couleur complémentaire adj. 1 */
color: hsl(74, 76%, 55%);
```

https://codepen.io/alyra/pen/RwrPBxB

[HSL en action](https://cdpn.io/alyra/debug/LYpoYPY)

## Nouvelles format coleurs

Des nouvelles couleurs arrivent - pour l'instant uniquement dans le navigateur Safari [CodePen](https://codepen.io/cssgrid/pen/KKpLBom)
Nous allons pas les utiliser mais vous pouvez [en lire ici](https://webkit.org/blog/10042/wide-gamut-color-in-css-with-display-p3/)

## Contrast checker - Web Accessibility in Mind

Vous savez maintenant comment référencer les couleurs. Par contre pas toutes les couleurs fonctionnent bien ensemble. Le problème principale ici est le contraste entre la couleur du fond (`background-color`) et la couleur du texte (`color`). Le contraste trop bas rend notre contenu illisible. 

Il existe des normes qui définissent les valeur correctes pour le contraste, ainsi que des outils qui calcule et valide le contaste. 

[Contrast checker](https://webaim.org/resources/contrastchecker/)

## Background

[Playground - size/repeat/position](https://codepen.io/alyra/debug/ExPxpyw)
[Playground - linear-gradient](https://codepen.io/alyra/debug/bGEdmMM)

## Exercices

- [hsl colors](https://codepen.io/alyra/pen/JjGdBwM) | [solution](https://codepen.io/alyra/pen/24600deab70bf2bd797c1e39fbedec24)
