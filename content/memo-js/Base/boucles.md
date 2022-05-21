+++
title = "Boucles"
date =  2022-04-18T16:02:17+02:00
weight = 80
+++

{{% notice tip %}}
Besoin d'une explication détaillée parce que vous n'avez rien compris ?
<a href="https://openclassrooms.com/fr/courses/6175841-apprenez-a-programmer-avec-javascript/6279104-utilisez-la-bonne-boucle-pour-repeter-les-taches-for-while" target="_blank">ICI</a>
{{% /notice %}}

## For
Compte de x à y
```js
for(let i =0; i <= 5; i++){
    //execute code sur chaque itération
}
```

## Foreach
Fait un tour avec chaque élément de la liste ou du tableau
```js
let tableau = ["A", "B", "C"];
tableau.forEach((element, index) => {
    //execute code on element
})
```

## While
Tourne tant qu'une condition est vraie

```js
let boucle = 0;
while(boucle < 5){
    boucle++;
    console.log(boucle);
}
```