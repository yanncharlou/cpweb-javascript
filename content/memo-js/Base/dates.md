+++
title = "Dates"
date =  2022-04-18T19:22:40+02:00
weight = 130
+++

La classe Date permet de manipuler facilement des dates en javascript.

## Créer une date

```js
var date1 = new Date('December17, 1995 03:24:00');// Sun Dec17 1995 03:24:00 GMT...
var date2 = new Date('1995-12-17T03:24:00');// Sun Dec17 1995 03:24:00 GMT...

//attention on ne peut pas comparer dates :
console.log(date1 === date2);// false;
console.log(date1 == date2);// false;
console.log(date1 - date2); // retourne la différence en milliseconde
```

## Afficher une date
```js
var uneDate = new Date('1995-12-17T03:24:00');

//afficher la date dans la langue de l'utilisateur
console.log( uneDate.toLocaleString() );

//afficher dans une langue spécifique
console.log( uneDate.toLocaleString('fr-FR') );

```

## Modifier une date

```js
var date1 = new Date('1995-12-17T03:24:00');
//On modifie la date avec set...
date1.setDate(31);
date1.setMonth(2);
date1.setFullYear(2018);
date1.setHours(10);
date1.getUTCHours();
date1.setMinutes(0);
date1.setSeconds(0);
date1.setMilliseconds(0);

//On récupère les valeurs avec get...

console.log(
    "Nous sommes le " + date1.getDate() + " du mois " + date1.getMonth() + " de l'an de grâce " + date1.getFullYear()
);

```