# Sélecteurs CSS

Bien sélectionner les éléments pour changer leurs propriétés CSS est une partie importante de notre apprentissage. 


## Différents type de sélecteurs et comment les combiner ?

Pour commencer, ce matin, on vous offre un petit déjeuner, [commandez tout ce qui vous plaît.](https://css-cantine.netlify.app/)

[![css cantine](https://wptemplates.pehaa.com/assets/alyra/css-cantine.png)](https://css-cantine.netlify.app/)

Nous allons aussi utiliser le pen ci-dessous pour jouer avec des sélecteurs :

https://codepen.io/alyra/pen/OJMyLoz

ainsi que [ce site qui traduit un sélecteur entrée par l'utilisateur en anglais.](https://hugogiraudel.github.io/selectors-explained/)

<ul class="columns fragment fade visible current-fragment" data-fragment-index="0">
  <li class="done"><code>* { }</code></li>
  <li class="done"><code>E { }</code></li>
  <li class="done"><code>.class { }</code></li>
  <li class="done"><code>#id { }</code></li>
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
