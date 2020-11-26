# Typographie

Vous l'avez peut-être déjà remarqué, certaines propriétés CSS se transmettent du parent vers enfant, d'autres non.

Les propriétés relatives au texte se héritent.

Par exemple, si vous fixez une color et une font-family pour l'élément `body`, tout élément sera mis en forme avec cette même couleur et cette même police, **à moins qu'on lui ait appliqué directement des règles.**

### `font-family`

La propriété `font-family` définit une liste, ordonnée par priorité, de polices à utiliser pour mettre en forme le texte. Les valeur sont séparés par des virgules.

```css
body {
  font-family: "Open Sans", Helvetica, Arial, sans-serif;
}
```

Dans l'exemple ci-dessus, le navigateur va essayer d'appliquer la police "Open Sans", ensuite la police Helvetica, si elle n'est pas disponible il essayera Arial. Si ni Open Sans, ni Helvetica ni Arial ne sont disponibles, la police de type `sans-serif` sera utilisée.

#### Generic font-faces :

- serif
- sans-serif
- cursive
- fantasy
- monospace

https://codepen.io/alyra/pen/eYJOaOO

[Web-safe Fonts](https://www.cssfontstack.com/)

### font-weight

100 - 200 - 300 - ... - 900  
normal (400) - défaut pour body  
bold (700)

```
header p {
  font-weight: bold;
}
```

#### font-style

italic, normal

```
header p {
  font-style: italic;
}
```

#### font-size

`px`, `em`, `rem`

https://codepen.io/alyra/pen/VweZJzR

#### autres propriétés :

`text-decoration`  
`text-align` - alignement au sein d'un élément block  
`line-height`

- [Wanted Dead or Alive - Google Fonts](https://codesandbox.io/s/police-rxtme?file=/index.html) | [solution](https://codepen.io/alyra/pen/6eba070d53ff9fa1f9b0952d6ace935f)
