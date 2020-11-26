# Typographie

Vous l'avez peut-être déjà remarqué, certaines propriétés CSS se transmettent du parent vers enfant, d'autres non.

Les propriétés relatives au texte se héritent.

Par exemple, si vous fixez une color et une font-family pour l'élément `body`, tout élément sera mis en forme avec cette même couleur et cette même police, **à moins qu'on lui ait appliqué directement des règles.**

## `font-family`

La propriété `font-family` définit une liste, ordonnée par priorité, de polices à utiliser pour mettre en forme le texte. Les valeur sont séparés par des virgules.  Le navigateur va utiliser la première police qui est soit installée chez l'utilisateur ou qui peut êtré chargé depuis un serveur distant.

```css
body {
  font-family: "Open Sans", Helvetica, Arial, sans-serif;
}
```

Dans l'exemple ci-dessus, le navigateur va essayer d'appliquer la police "Open Sans", ensuite la police Helvetica, si elle n'est pas disponible il essayera Arial. Si ni Open Sans, ni Helvetica ni Arial ne sont disponibles, la police de type générique `sans-serif` sera utilisée. **La famille de police générique doit toujours être inclue** (et bien evidemment sur la dernière position).

### Les principales familles de polices génériques

- `serif` - les caractères ont des empattements
- `sans-serif` - les caractères n'ont pas d'empattement
- `cursive` - les extrémités des caractères peuvent se joindre les uns aux autres
- `fantasy` - des polices décoratives 
- `monospace` - chaque caractère prend la même largeur, (police est à chasse fixe)

https://codepen.io/alyra/pen/eYJOaOO

Dans notre déclaration de `font-family`, juste avant la famille générique, nous listons souvent des polices qui sont installées chez la majorité des utilisateurs. Vous trouverez la liste des polices *safe for the web* avec les statistiques les concernant sur [Web-safe Fonts](https://www.cssfontstack.com/)

## `font-weight`

La propriété `font-weight` permet de définir la graisse utilisée pour le texte. Les niveaux de graisse disponibles dépendent de la police. Il existe des polices disponible avec plusieurs niveaux de graisse, et des possible avec une seule variante.

```
header p {
  font-weight: bold;
}
```

**Les valeurs de `font-weight` :**

- `normal` - équivalent à la valeur  numérique de 400
- `bold` - texte est en gras, équivalent à la valeur numérique de 700
- numérique - selon l'ancien spécification 100, 200, 300, 400, 500, 600, 700, 800 ou 900. Selon la nouvelle spécification une valeur comprise entre 1 et 1000
- `lighter` - on diminue la graisse d'un niveau par rapport à l'élément parent (selon les fontes / graisses disponibles pour la police utilisée)
- `bolder` - on augemente la graisse d'un niveau par rapport à l'élément parent (selon les fontes / graisses disponibles pour la police utilisée)

Si la graisse demandée n'est pas disponible pour la police, le navigateur procède à une conversion. Vous pouvez trouvez les règles de cette conversion ainsi que des détails de mise en place `font-weight: lighter` et `font-weight: bolder` dans [cet article sur MDN](https://developer.mozilla.org/fr/docs/Web/CSS/font-weight)



## `font-style`

La propriété `font-style` définit si la police devrait utiliser la fonte normale (`normal`), italique (`italic`) ou oblique (`oblique`)

```
header p {
  font-style: italic;
}
```

**Les valeurs de `font-style`**
- `normal`
- `italic` - une police qualifiée d'italic, s'il n'y a pas de version italique, une version oblique sera sélectionnée à la place.
- `oblique` - une police qualifiée d'oblique, s'il n'y a pas de version oblique, une version italic sera sélectionnée à la place. 
- `oblique <angle>` - une police qualifiée d'oblique avec un angle pour la pente du texte spécifié  (très rarement utilisée)

Dans chaque de cas, si aucune police oblique n'est disponible, le navigateur synthétisera une police penchée en tournant les caractères d'une fonte normale.

## font-size

La propriété `font-size` définit la taille de fonte utilisée pour le texte. La propriété font-size peut être définie de deux façons :

- (rarement) comme un mot-clé désignant une taille absolue ou une taille relative (`xx-small`, `x-small`, `small`, `medium`, `large`, `x-large`, `xx-large`)
- (parfois) <percentage> - les valeurs exprimées en pourcentages (`%`) sont proportionnelles à la taille de fonte de l'élément parent
  
  ```css
  small {
    font-size: 75%;
  }
  ```
- (très souvent) comme une valeur de type <length>
  
  `px` - souvent utilisé. Pourtant l'utilisation des pixels pour la taille de police n'est pas le meilleur choix, et nous allons abondonner cette approche. Utilisation de pixels ne permet pas aux navigateurs d'appliquer des réglages utilisateur concernant la taille des polices.
  



https://codepen.io/alyra/pen/VweZJzR

#### autres propriétés :

`text-decoration`  
`text-align` - alignement au sein d'un élément block  
`line-height`

- [Wanted Dead or Alive - Google Fonts](https://codesandbox.io/s/police-rxtme?file=/index.html) | [solution](https://codepen.io/alyra/pen/6eba070d53ff9fa1f9b0952d6ace935f)
