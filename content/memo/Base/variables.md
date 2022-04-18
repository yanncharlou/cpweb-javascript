---
title: Les variables
description : ""
weight: 20
---

## Créer une variable

On crée des variables avec les mots clefs `var`, `let` ou `const`.

```js
var maVariable = "du texte";
let ageDuCapitaine = "42";
const monAutreVariable = "Encore du texte";
```

## Le nom des variables

**Version simple** : Le nom d'une variable ne doit contenir que des caractères basiques ou "_" et ne jamais commencer par un chiffre.

**La règle complète**
- Peut contenir des lettres, nombres, `_` et `$`.
- Ne peut pas commencer par un nombre.
- Est sensible à la casse. (`a` est différent de `A`)
- Elle ne doit pas être un mot réservé. (C'est à dire une commande qui veut dire quelque chose en javascript.)

## var, let, ou const ?

### var (ancienne méthode)
- Ancienne façon de déclarer des variables. (Jusqu'en 2015) 
- La variable est accessible dans toute la fonction où elle se trouve.

### let (nouvelle méthode)
- Nouvelle façon (depuis 2015)
- La variable est accessible dans le bloc `{}` où elle se trouve.

### const : constante = sa valeur ne changera pas.
- Permet de déclarer une variable dont la valeur ne pourra pas changer.
- On l'utilise par exemple pour des options de configuration dans le code.