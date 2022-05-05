+++
title = "Tableaux"
date =  2022-04-18T15:23:19+02:00
weight = 50
+++


## Créer et accéder aux données

```js
//Tableau simple
var sports = ['basket', 'volley', 'foot', 'natation', 'tennis', 'course'];
console.log(sports);
console.log(sports[0]); //affiche basket
console.log(sports[1]); //affiche volley

//Tableau contenant un autre tableau
var tableau2D= ['arbre', 795, [12, 88, 512, 42]];
console.log(tableau2D.length); //affiche 3
console.log(tableau2D[2][2].length); //affiche 4
console.log(tableau2D[2][3].length); //affiche 512
```
{{% notice note %}}
La première case d'un tableau porte le numéro 0.
{{% /notice %}}

## Modifier un tableau

| *fonction* | *description* |
|----|----|
| tableau[i] = valeur | mets une valeur dans une case |
| tableau.push(valeur) | ajoute une valeur à la fin |
| tableau.pop() | enlève le dernier élément et le retourne |
| tableau.shift() | enlève le premier élément et le retourne |

```js
let array = ['0','1','2','3'];
array[1] = '4'; //met '4' à la place de '1'
array.push('5'); //ajoute '5' à la fin du tableau
let removeLast = array.pop() //enlève le dernier élément et le retourne.
let removeFirst = array.shift() //enlève le premier élément et le retourne.
console.log(array) // [ "4", "2", "3" ]
console.log(removeLast) // 5
console.log(removeFirst) // 0
```

## Tirer au hasard une case de tableau

```js
let messages = ['coucou', 'machin', 'truc'];
//je tire au hasard un nombre entier entre 0 et la longueur du tableau.
let indiceRandom = Math.floor(Math.random() * messages.length);
alert(messages[indiceRandom]);
```

Autre exemple sur la page [Objects]({{< ref "memo-js/Base/objects.md" >}}).