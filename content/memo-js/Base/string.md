---
title: String
description : "Les chaines de caractère"
weight: 40
---

## Concaténer
```js

let texteA = "Coucou";
let texteB = "les amis";

/* Concaténer (mettre bout à bout) */
let phrase = texteA + " " + texteB;
```

## Accéder à la Nième lettre

```js
let lettre = texteA[0]; //la première
let lettre = texteA[3]; //la 4ème
```

## Chercher une lettre ou un mot

```js
let monTexte = "Lorem ipsum dolor sit amet, consectetur adipiscing elit.";
let motAChercher = "ipsum";
let positionDeLaLettre = monTexte.search(motAChercher); // retourne 6
```
{{% notice note %}}
On peut aussi utiliser cette fonction avec une expression rationnelle (regex).
{{% /notice %}}

## Remplacer une lettre ou un mot

```js
let monTexte = "Lorem ipsum dolor sit amet, consectetur adipiscing elit.";
let nouveauTexte = monTexte.replace('ipsum','truc'); // retourne "Lorem truc dolor sit amet, consectetur adipiscing elit.";
```

## Scinder une chaine de caractères en tableau sur la base d'un caractère de séparation

```js
//un mot dans chaque case du tableau en coupant à chaque espace
let monTexte = "Lorem ipsum dolor sit amet, consectetur adipiscing elit.";
let tableauDesMots = monTexte.split(" ");
console.log(tableauDesMots[1]); //affiche "ipsum"

//un ingrédient dans chaque case en coupant à chaque virgule
let chaineIngredients = "farine,sucre,sel,eau";
let tableauIngredients = chaineIngredients.split(',');
console.log(tableauIngredients[1]); //affiche "sucre"
```
