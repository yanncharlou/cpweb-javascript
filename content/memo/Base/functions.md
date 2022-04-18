+++
title = "Fonctions"
date =  2022-04-18T16:12:44+02:00
weight = 100
+++

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