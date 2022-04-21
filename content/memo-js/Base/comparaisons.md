+++
title = "Comparaisons et opérateurs logiques"
menuTitle  = "Comparaisons"
date =  2022-04-18T15:23:19+02:00
weight = 70
+++

## Comparer des valeurs

| **Opérateur** | **Description** |
|-------------|-------------|
| `==` | Egal |
| `===` | Egal et de même type |
| `!=` | Non égal |
| `!==` | Non égal ou de type différent |
| `>` | Supérieur |
| `>=` | Supérieur ou égal |
| `<` | Inférieur | 
| `<=` | Inférieur ou égal | 

## Combiner des conditions

| **Opérateur** | **Description** |
|-------------|-------------|
| `&&` | **ET** (les deux conditions doivent être vraies) |
| `\|\|` | **OU** (au moins une des deux conditions doit être vraie) |
| `!` | **NON** (la condition doit être fausse) |

## Exemples

```js

if(prenom == 'didier' && age > 42){
    console.log("Tu t'appelles Didier et tu as plus de 42 ans.");
}

if((prenom == 'didier' || prenom == 'Didier') && age >= 30 && age <= 40){
    console.log("Tu t'appelles Didier et tu as entre 30 et 40 ans.");
}

if((prenom == 'didier' || prenom == 'Didier') && !(age >= 30 && age <= 40) ){
    console.log("Tu t'appelles Didier et tu n'as pas entre 30 et 40 ans.");
}

```