+++
title = "Fonctions"
date =  2022-04-18T16:12:44+02:00
weight = 100
+++

{{% notice tip %}}
Besoin d'une explication détaillée parce que vous n'avez rien compris ?
<a href="https://openclassrooms.com/fr/courses/6175841-apprenez-a-programmer-avec-javascript/6279223-travaillez-sur-les-fonctions" target="_blank">ICI</a>
{{% /notice %}}

```js
//Déclarer la fonction
function nom_de_la_fonction(parametreA, parametreB,...){
    //code à executer
}

//Appeler la fonction
nom_de_la_fonction(parametreA, parametreB,...);
```

**Exemple**

```js
function surfaceRectangle(hauteur, largeur){
    let surface = hauteur * largeur;
    return surface;
}

let surface = surfaceRectangle(18, 42);
```