+++
title = "Objets"
date =  2022-04-18T18:48:14+02:00
weight = 55
+++

Les objets sont des structures, comme les tableaux, qui peuvent contenir des attributs et des fonctions.

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