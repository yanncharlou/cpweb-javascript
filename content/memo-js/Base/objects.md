+++
title = "Objets"
date =  2022-04-18T18:48:14+02:00
weight = 55
+++

Les objets sont des structures, comme les tableaux, qui peuvent contenir des attributs et des fonctions.

{{% notice tip %}}
Besoin d'une explication détaillée parce que vous n'avez rien compris ?
<a href="https://openclassrooms.com/fr/courses/6175841-apprenez-a-programmer-avec-javascript/6278564-definissez-des-objets-et-leurs-attributs-avec-des-classes" target="_blank">ICI</a>
{{% /notice %}}

```js
var marin = {
    nom: "Haddock",
    age: 54,
    insultes: [
        "Bachi-bouzouk !",
        "Tonnerre de Brest !",
        "Mille Milliard de Mille Sabords !",
        "Moule à Gaufres !", 
        "Nyctalope !"
    ],
    insulter(){
        let indiceRandom = Math.floor(Math.random() * this.insultes.length);
        alert(this.insultes[indiceRandom]);
    }
}

marin.insultes.push("Bougre de crème d’emplâtre à la graisse de hérisson !");
marin.insulter();
```