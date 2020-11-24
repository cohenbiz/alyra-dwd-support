# Tables

## Structure et HTML tags

Un élément `table` permet de structurer les données tabulaires. Les tableaux sont utiles pour afficher les données de rapport, des plannings, des comparatifs, etc. 
Voici la liste des éléments HTML que nous allons utiliser :

- `table`  
- `thead` - contient ensemble de lignes de la partie en-tête
- `tbody` - contient ensemble de lignes de la partie principale (corps) du tableau
- `tfoot` - contient ensemble de lignes de la partie résumée 
- `tr` - ligne de cellules dans un tableau  
- `th` - cellule de tableau de type "en-tête" 
- `td` - cellule de donnée
- `caption` - la légende du tableau

![](https://wptemplates.pehaa.com/assets/alyra/table.png)

Voici un exemple :

```html
<table>
  <caption>
    Optionnel - description
  </caption>
  <!-- thead est optionnel, imbrique des lignes d'en-tête des colonnes d'un tableau. -->
  <thead>
    <tr>
      <th>titre 1</th>
      <th>titre 2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>el 1</td>
      <td>el 2</td>
    </tr>
    <tr>
      <td colspan="2">el 3</td>
    </tr>
  </tbody>
  <!-- tfoot est optionnel, imbrique des lignes qui résument les colonnes d'un tableau. -->
  <tfoot>
    <tr>
      <td>el 4</td>
      <td>el 5</td>
    </tr>
  </tfoot>
</table>
```

https://codepen.io/alyra/pen/PoPvKEV

https://codepen.io/alyra/pen/dyYQLPE

---

## Exercices

- [Table de multiplication](https://codepen.io/alyra/pen/VwvVoRa) | [solution](https://codepen.io/alyra/pen/0c64510eac62c096c3cb3140d448deb2)
- [Table (Candidat -> Certification)](https://codepen.io/alyra/pen/yLYQrjq) | [solution](https://codepen.io/alyra/pen/73226cb6ba6d469a91a721036a04faea)
- [Tables - ALYRA (Challenge)](https://codepen.io/alyra/pen/LYpMPOx) | [solution](https://codepen.io/alyra/pen/cacca459f15f134825dcc8e51d87f674)
