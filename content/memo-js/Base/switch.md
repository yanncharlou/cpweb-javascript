+++
title = "Switch"
date =  2022-04-18T16:08:42+02:00
weight = 90
+++

Pratique si on veut utiliser une chose différente entre plusieurs valeurs possibles d'une variable.

{{% notice tip %}}
Besoin d'une explication détaillée parce que vous n'avez rien compris ?
<a href="https://openclassrooms.com/fr/courses/6175841-apprenez-a-programmer-avec-javascript/6278948-choisissez-la-condition-appropriee-pour-controler-le-deroulement-de-votre-programme-if-else-switch" target="_blank">ICI</a>
{{% /notice %}}

```js
switch (prenom) {
    case "didier":
        //code à executer
        break;
    case "julien":
        //code à executer
        break;
    default:
        //code à executer par défaut
}
```
Ne pas oublier le `break` à la fin de chaque condition.