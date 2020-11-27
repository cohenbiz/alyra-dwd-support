# Sélecteurs CSS

Bien sélectionner les éléments pour changer leurs propriétés CSS est une partie importante de notre apprentissage.

## Différents type de sélecteurs et comment les combiner ?

Pour commencer, ce matin, on vous offre un petit déjeuner, [commandez tout ce qui vous plaît.](https://css-cantine.netlify.app/)

[![css cantine](https://wptemplates.pehaa.com/assets/alyra/css-cantine.png)](https://css-cantine.netlify.app/)

Nous allons aussi utiliser le pen ci-dessous pour jouer avec des sélecteurs :

https://codepen.io/alyra/pen/OJMyLoz

ainsi que [ce site qui traduit un sélecteur entrée par l'utilisateur en anglais.](https://hugogiraudel.github.io/selectors-explained/)

## Type Selector

`E {}`

En français _sélecteur de type._ Les _sélecteurs de type_ ciblent des éléments en fonction du nom de leur balise (`tag`) HTML ou XML, comme `div`, `p`, `ul`, `assiette` etc. C'est un sélecteur simple.

```css
img {
  max-width: 100%;
  height: auto;
}
```

```css
body {
  background: lavender;
}
```

---

## Class Selector

`.class {}`

En français _sélecteur de classe._ Le symbole `.` suivi (sans espace) par le nom de la classe permet de cibler tous les éléments qui ont cette classe. C'est un sélecteur simple.

```css
.mini {
  font-size: 0.875rem;
}
```

---

## ID Selector

`#jolie`

En français _sélecteur d'identifiant._ Avec le symbole `#` suivi (sans espace) par le nom d'identifiant on peut cibler un élément par son attribut `id.` C'est un sélecteur simple.

```css
#top {
  position: fixed;
  top: 0;
}
```

---

## The Universal Selector

`* {}`

En français - sélecteur universel. Il correspond à un élément de n'importe quel type. C'est un sélecteur simple.

```css
* {
  box-sizing: border-box;
}
```

---

{
doThis: "Je vais prendre des 'french toasts'.",
selector: "[lang='fr']",

## Attribute selector

`[attr] {}`,  
`[attr=value] {}`,  
`[attr*=value] {}`,  
`[attr^=value] {}`,  
`[attr$=value] {}`,  
`[attr~=value] {}`

En français _sélecteur d'attribut._ C'est un sélecteur simple.

<dl>
 <dt><code>[<em>attr</em>]</code></dt>
 <dd>Cible des éléments avec l'attribut <code>attr</code>.</dd>
 <dt><code>[<em>attr</em>=<em>value</em>]</code></dt>
 <dd>Cible  des éléments avec l'attribut <code>attr</code> dont la valeur est exactement <code>value</code>.</dd>
 <dt><code>[<em>attr</em>~=<em>value</em>]</code></dt>
 <dd>Cible des éléments avec l'attribut <code>attr</code> dont la valeur contient <code>value</code> séparée par des espaces.
 <dt><code>[<em>attr</em>|=<em>value</em>]</code></dt>
 <dd>Cible des éléments avec l'attribut <code>attr</code> dont la valeur est exactement <code>value</code> ou dont la valeur commence par <code>value</code> suivi&nbsp;immédiatement d'un tiret (U+002D). Souvent utilisé avec des codes de langues.</dd>
 <dt><code>[<em>attr</em>^=<em>value</em>]</code></dt>
 <dd>Cible des éléments avec l'attribut <code>attr</code> dont la valeur commence par <code>value</code>.</dd>
 <dt><code>[<em>attr</em>$=<em>value</em>]</code></dt>
 <dd>Cible des éléments avec l'attribut <code>attr</code> dont la valeur se termine par <code>value</code>.</dd>
 <dt><code>[<em>attr</em>*=<em>value</em>]</code></dt>
 <dd>Cible des éléments avec l'attribut <code>attr</code> et dont la valeur contient au moins une occurrence de&nbsp;<code>value</code>.</dd>
</dl>

```css
[lang="en"] {
  font-family: italic;
}

a[href^="#"] {
  background-color: gold;
}

a[href$="alyra.fr"] {
  background-color: blue;
  color: white;
}
```

---

## Descendant Combinator

`A B {}`

En français : le combinateur de descendance. Permet de combiner deux sélecteurs sous la forme `A B`.
`A B` cible des éléments qui correspondent au sélecteur `B` uniquement si ceux-ci ont un élément ancêtre qui correspond au premier sélecteur (`A`).
Attention à l'espace entre deux éléments.

```css
header p {
  font-weight: bold;
}
```

---

## Selector list (,)

`A, B {}`

Cibler en même temps les éléments `A` et `B`. On peut ainsi combiner plusieurs types de sélecteurs et en avoir plus de deux.

```css
h1,
h2,
h3,
.heading {
  font-family: Montserrat, sans-serif;
  font-weight: 900;
}
```

---

## Child Selector

`A > B {}`

Permet de combiner des sélecteurs. Cible les éléments `B` qui sont des enfants directs des éléments `A`.

```css
header > div {
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
```

---

## Adjacent Sibling Selector

`A + B {}`

Permet de combiner des sélecteurs. `A + B` cible tous les éléments `B` qui suivent directement les `A`.

```css
h2 + p {
  font-size: 0.875rem;
  text-transform: uppercase;
  letter-spacing: 0.125rem;
}
```

---

## General sibling combinator"

`A ~ B {}`

Permet de combiner des sélecteurs. A ~ B cible tous les éléments `B` qui suivent les `A`.

---

## First Child Pseudo-class

`:first-child {}`

Cible les éléments qui sont les premiers enfants de son élément parent.

```css
li:first-child {
  font-weight: bold;
}
```

---

## nth Child Pseudo-class

`:nth-child(..) {}`

Cible les éléments qui sont les enfants numéro .. de son élément parent.

```css
li:nth-child(2n + 1) {
  background: pink;
}
/*
li:nth-child(1) {
  background: pink;
}
li:nth-child(3) {
  background: pink;
}
li:nth-child(5) {
  background: pink;
}
...
*/
```

---

## Last Child Pseudo-class

`:last-child {}`

Cible les éléments qui sont les derniers enfants de son élément parent.

```css
section p:last-child {
  margin-bottom: 0;
}
```

## First-of-type Pseudo-class

{
selectorName: "en anglais : First of type Pseudo-selector",
helpTitle: "Cible l'élément qui est le premier enfant de son type",
doThis: "Donnez moi la première assiette, svp.",
selector: "assiette:first-of-type",
syntax: ":first-of-type",
examples: [
"<strong>:first-of-type</strong> cible tous les éléments qui sont les premiers enfants de leur type.",
"<strong>p:first-of-type</strong> cible tous les premiers paragraphes.",
"<strong>div p:first-of-type</strong> cible tous les premiers paragraphes qui sont dans un <tag>div</tag>.",
],
boardMarkup: `<boite /> <assiette /> <assiette /> <assiette />`,
},

{
doThis: "Moi, je vais prendre des mini donuts, svp.",
selector: "donut.mini",
helpTitle: "Combinons les sélecteurs!",
syntax: "A.classname",
help:
"A.classname veut dire un élément <strong>A</stron> avec la classe <strong>classname</strong> - en collant des sélecteurs ensemble (sans espace) on ajoute des restrictions. </br></br><strong>assiette.mini</strong> et <strong>assiette&nbsp;&nbsp;.mini</strong> sont deux sélecteurs complétement différents : le premier cible des petites assiettes, le deuxième les petits éléments dans les assiettes.",
examples: [
'<strong>ul.important</strong> cible tous éléments <tag>ul</tag> qui ont la classe <strong>class="important"</strong>',
'<strong>#big.wide</strong> cible un élément avec l\'identifiant <strong>id="big"</strong> qui a aussi la classe <strong>class="wide"</strong>',
],
boardMarkup: ` <toast/> <toast class="mini"/> <boite> <donut class="mini"/> </boite> <assiette> <donut/> </assiette> <assiette> <donut class="mini"/> </assiette>`,
},

{
selectorName: "en anglais : nth Child Pseudo-selector",
helpTitle:
"Cible l'élément qui est l'enfant numéro ... de son élément parent",
doThis: "Je prendrai bien la 3e assiette, svp.",
selector: "assiette:nth-child(3)",
syntax: ":nth-child(..)",
examples: [
"<strong>:nth-child(2)</strong> cible tous les éléments qui sont les 2e enfants de leur parent.",
"<strong>p:nth-child(2)</strong> cible tous les paragraphes qui sont les 2e enfants de leur parent.",
"<strong>div p:nth-child(2)</strong> cible tous les paragraphes qui sont les 2e enfants d'un <tag>div</tag>.",
"<strong>:nth-child(2n)</strong> cible tous les éléments qui sont les enfants pairs de leur parent.",
"<strong>:nth-child(2n+1)</strong> cible tous les éléments qui sont les enfants impairs de leur parent.",
"<strong>:nth-child(3n+1)</strong> cible tous les éléments qui sont les enfants numéro 1, 4, 7, 10, 13, ... de leur parent.",
],
boardMarkup: `<assiette /> <assiette /> <assiette /> <assiette /> <assiette />`,
},

{
selectorName: "en anglais : First of type Pseudo-selector",
helpTitle: "Cible l'élément qui est le premier enfant de son type",
doThis: "Donnez moi la première assiette, svp.",
selector: "assiette:first-of-type",
syntax: ":first-of-type",
examples: [
"<strong>:first-of-type</strong> cible tous les éléments qui sont les premiers enfants de leur type.",
"<strong>p:first-of-type</strong> cible tous les premiers paragraphes.",
"<strong>div p:first-of-type</strong> cible tous les premiers paragraphes qui sont dans un <tag>div</tag>.",
],
boardMarkup: `<boite /> <assiette /> <assiette /> <assiette />`,
},
{
selectorName: "en anglais : First of type Pseudo-selector",
helpTitle: "Cible l'élément qui est le premier enfant de son type",
doThis: "Donnez moi la première assiette et la première boite, svp.",
selector: ":first-of-type",
syntax: ":first-of-type",
examples: [
"<strong>:first-of-type</strong> cible tous les éléments qui sont les premiers enfants de leur type.",
"<strong>p:first-of-type</strong> cible tous les premiers paragraphes.",
"<strong>div p:first-of-type</strong> cible tous les premiers paragraphes qui sont dans un <tag>div</tag>.",
],
boardMarkup: `<boite /> <boite /> <assiette /> <assiette /> <boite /> <assiette />`,
},
{
doThis: "Donuts, mais pas les petits, svp...",
selector: "donut:not(.mini)",
selectorName: "en anglais : Negation pseudo-class",
helpTitle: "Utilise la negation pour cibler les élément",
syntax: ":not(..)",
examples: [
"<strong>:not(p)</strong> cible tous les éléments qui ne sont pas des paragraphes.",
"<strong>p:not(.subtitle)</strong> cible tous les paragraphes qui n'ont pas de classe <i>subtitile</i>.",
"<strong>li:not(:first-child)</strong> cible tous les li qui ne sont les premiers enfants.",
],
//help : 'You can combine the class selector with other selectors, like the type selector.',
boardMarkup: ` <donut/> <donut class="mini"/> <donut/> <boite> <donut class="mini"/> </boite> <assiette> <donut/> </assiette> <assiette> <donut/> </assiette>`,
},
{
doThis: "Je prends tout, sauf le cupcake, svp...",
selector: ":not(cupcake)",
selectorName: "en anglais : Negation pseudo-class",
helpTitle: "Utilise la negation pour cibler les élément",
syntax: ":not(..)",
examples: [
"<strong>:not(p)</strong> cible tous les éléments qui ne sont pas des paragraphes.",
"<strong>p:not(.subtitle)</strong> cible tous les paragraphes qui n'ont pas de classe <i>subtitile</i>.",
"<strong>li:not(:first-child)</strong> cible tous les li qui ne sont les premiers enfants.",
],
//help : 'You can combine the class selector with other selectors, like the type selector.',
boardMarkup: ` <donut/> <donut class="mini"/> <boite/> <donut class="mini"/> <cupcake/> <assiette/> <donut/>`,
},
{
doThis: "Je prends tout, sauf le petit cupcake, svp...",
selector: ":not(cupcake.mini)",
selectorName: "en anglais : Negation pseudo-class",
helpTitle: "Utilise la negation pour cibler les élément",
syntax: ":not(..)",
examples: [
"<strong>:not(p)</strong> cible tous les éléments qui ne sont pas des paragraphes.",
"<strong>p:not(.subtitle)</strong> cible tous les paragraphes qui n'ont pas de classe <i>subtitile</i>.",
"<strong>li:not(:first-child)</strong> cible tous les li qui ne sont les premiers enfants.",
],
//help : 'You can combine the class selector with other selectors, like the type selector.',
boardMarkup: ` <donut/> <donut class="mini"/> <donut/> <donut class="mini"/> <cupcake class="mini"/> <cupcake/> <donut/> <donut/>`,
},

]

<ul class="columns fragment fade visible current-fragment" data-fragment-index="0">
  <li class="done"><code>E F { }</code></li>
  <li class="done"><code>E &gt; F { }</code></li>
  <li class="done"><code>E + F { }</code></li>
  <li><code>:hover { }</code></li>
  <li><code>:focus { }</code></li>
  <li><code>:link { }</code></li>
  <li><code>:visited { }</code></li>
  <li><code>E[attribute] { }</code></li>
  <li><code>E[attribute=value] { }</code></li>
  <li><code>E[attribute^=value] { }</code></li>
  <li><code>E[attribute$=value] { }</code></li>
  <li><code>E[attribute*=value] { }</code></li>
  <li class="done"><code>:first-child { }</code></li>
  <li><code>:lang() { }</code></li>
  <li><code>:before { }</code></li>
  <li><code>::selection { }</code></li>
  <li><code>:after { }</code></li>
  <li><code>:first-letter { }</code></li>
  <li><code>:first-line { }</code></li>
  <li><code>E ~ F { }</code></li>
  <li><code>:root { }</code></li>
  <li class="done"><code>:last-child { }</code></li>
  <li><code>:only-child { }</code></li>
  <li><code>:nth-child() { }</code></li>
  <li><code>:nth-last-child() { }</code></li>
  <li><code>:first-of-type { }</code></li>
  <li><code>:last-of-type { }</code></li>
  <li><code>:only-of-type { }</code></li>
  <li><code>:nth-of-type() { }</code></li>
  <li><code>:nth-last-of-type() { }</code></li>
  <li><code>:empty { }</code></li>
  <li><code>:not() { }</code></li>
  <li><code>:target { }</code></li>
  <li><code>:enabled { }</code></li>
  <li><code>:disabled { }</code></li>
  <li><code>:checked { }</code></li>
  <li><code>:default { }</code></li>
  <li><code>:valid { }</code></li>
  <li><code>:invalid { }</code></li>
  <li><code>:in-range { }</code></li>
  <li><code>:out-of-range { }</code></li>
  <li><code>:required { }</code></li>
  <li><code>:optional { }</code></li>
  <li><code>:read-only { }</code></li>
  <li><code>:read-write { }</code></li>
  <li><code>:right { }</code></li>
  <li><code>:left { }</code></li>
  <li style="color:orange">...et ce toujours pas tout...</li>
</ul>

https://codepen.io/alyra/pen/RwrrpBO

[Quiz](https://cdpn.io/alyra/debug/6f79149941afdce6945473428e1395ac)

```html
<ul class="personnages">
  <li class="list-item">Stormtrooper</li>
  <li class="list-item">Boba Fett</li>
  <li class="list-item">Dark Vador</li>
  <li class="list-item">Empereur Palpatine</li>
</ul>
```

```css
.personnages li {
  color: red;
}
.list-item {
  color: green;
}
ul > li {
  color: blue;
}
```

<dl style="font-size:20px">
						<dt>Puissance "0"</dt>
						<dd>Sélecteurs universels <em>universal selector</em> <code>*</code></dd>
						<dt>Puissance "1"</dt>
						<dd><em>type selectors</em> (html, body, div, ... ) et pseudo-elements (:before, ...)</dd>
						<dt>Puissance "10"</dt>
						<dd>classes (.title), attributs([class], [id], [title], [href],...), pseudo-classes (:hover, :first-child, :lang(), :focus, ...)</dd>
						<dt>Puissance "100"</dt>
						<dd>ids (#top, #contact, ...)</dd>
						<dt>Puissance "1000"</dt>
						<dd> style="font-weight:bold"</dd>
						<dt>Puissance "10000"</dt>
						<dd>{color: red!important;}</dd>
					</dl>

[Support .pdf](https://assets.codepen.io/4515922/Tableau_de_cartes%402x.pdf)

[Specificity calculator](https://specificity.keegan.st/)

![""](https://assets.codepen.io/4515922/Screenshot+2020-06-09+08.45.00.png)

    				<blockquote style="background: #bac8a6;
    color: black;
    border-left-color: black;

}">Des sur-spécificités, tu te méfieras… Plus efficaces les sélecteurs de base sont, pour qui sait les manipuler… Plus séducteur est le côté obscur, plus facile… N’en crois rien.

</blockquote>

### Ex. 1

https://codepen.io/alyra/pen/MWKaXjG

### Ex. 2

https://codepen.io/alyra/pen/NWxGzbv

[Quizzzzz](https://cdpn.io/alyra/debug/d341e5aba9eb51c6b9b0f517b45cf812)

[et l'afrontement final](https://codepen.io/pehaa/pen/dEpvXN)

## Exercices

- [Selectors - Statistiques](https://codepen.io/alyra/pen/JjGdeLy) | [solution](https://codepen.io/alyra/pen/351f134590b49036c87d4411ab114932)
- [Selectors - sac a dos](https://codepen.io/alyra/pen/RwrPqYe) | [solution](https://codepen.io/alyra/pen/f44b1d8384c5545652d8eb65e4b84a99)
- [Selectors - damier](https://codepen.io/alyra/pen/MWKwzZe) | [solution](https://codepen.io/alyra/pen/097d079ae3beab1186f3564fdbc2fe1b)
- [Selectors - lorem](https://codepen.io/alyra/pen/gOPpQVJ) | [solution](https://codepen.io/alyra/pen/819a084e0ce8c33dbd8dca7aa1d60370)
- [Selectors - cards](https://codepen.io/alyra/pen/xxZZqVL) | [solution](https://codepen.io/alyra/pen/05daf99332451394a1b1cd41acd71022)
