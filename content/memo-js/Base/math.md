+++
title = "Math"
date =  2022-04-18T19:08:17+02:00
weight = 120
+++

## Opérations simples

| **Opérateur** | **Description** |
|-------------------------|-----------------|
| `y = a + b` | addition |
| `y = a - b` | soustraction |
| `y = a * b` | multiplication |
| `y = a / b` | division |
| `y = a % b` | modulo (reste de la division entière) |
| `y++` | incrementer (équivalent à `y = y + 1` ) |
| `y--` | décrémenter (équivalent à `y = y - 1` ) |

## Classe Math

| **Fonction** |  **Description** |
|--------------|------------------|
| Math.random() | Retourne un chiffre au hasard entre 0 (inclus) et 1 (exclus) |
| Math.floor(*nombre*) | Retourne la partie entière du nombre. |
| Math.round(*nombre*) | Retourne le nombre arrondi |

[Liste complète des fonctions](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Math)

### Tirer au hasard un nombre entier

```js
// nombre entier entre 0 et 10 inclus :
let nombreEntierAuPif = Math.floor(Math.random() * 11);

// nombre entier entre 30 et 40
let nombreEntierEntre30et40 = Math.floor(Math.random() * 11) + 30;
```

