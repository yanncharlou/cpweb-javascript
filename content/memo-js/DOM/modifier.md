+++
title = "Modifier un élément"
date =  2022-04-18T20:09:31+02:00
weight = 30
+++

Javascript peut modifier comme il veut le contenu HTML de la page.

{{% notice tip %}}
Besoin d'une explication détaillée parce que vous n'avez rien compris ?
<a href="https://openclassrooms.com/fr/courses/5543061-ecrivez-du-javascript-pour-le-web/5577491-modifiez-le-dom" target="_blank">ICI</a>
{{% /notice %}}

## Modifier les styles CSS

```js
let monBouton = document.getElementById("mon-bouton");
monBouton.style.backgroundColor  = "red";
```
Attention, le nom de l'attribut CSS est en camelCase .
Par exemple : background-color devient backgroundColor .

## Modifier un attribut

```js
let monImage = document.getElementById("mon-image");
monImage.src  = "./images/image1.jpg"; //va charger une autre image à la place.
```

## Modifier le contenu HTML d'un élément

```js
let maDiv = document.getElementById("ma-div");
maDiv.innerHTML  = "<p>Ici du <strong>GROS</strong> contenu.</p>"; 
```
