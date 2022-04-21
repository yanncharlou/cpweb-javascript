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

