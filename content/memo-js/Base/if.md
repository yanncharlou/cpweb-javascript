+++
title = "Si, sinon"
date =  2022-04-18T15:23:19+02:00
weight = 60
+++

{{% notice tip %}}
Besoin d'une explication détaillée parce que vous n'avez rien compris ?
<a href="https://openclassrooms.com/fr/courses/6175841-apprenez-a-programmer-avec-javascript/6278948-choisissez-la-condition-appropriee-pour-controler-le-deroulement-de-votre-programme-if-else-switch" target="_blank">ICI</a>
{{% /notice %}}

## Si 
```js
let prenom = prompt("Quel est ton prénom ?");
if(prenom == "Didier" || prenom == "didier"){
    alert("Bonjour didier");
}
```

## Si, sinon
```js
let prenom = prompt("Quel est ton prénom ?");
if(prenom == "Didier" || prenom == "didier"){
    alert("Bonjour Didier");
}else{
    alert("Je ne sais pas qui vous êtes.");
}
```

```js
if(condition1){
    //code qui s'execute si la condition est bonne
}else if(condition2){
    //code qui s'execute si cette deuxième condition est bonne
}else{
    //code qui s'execute si les conditions ne sont pas bonnes
}
```