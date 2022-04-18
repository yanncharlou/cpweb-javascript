+++
title = "Boucles"
date =  2022-04-18T16:02:17+02:00
weight = 80
+++

## For
Compte de x à y
```js
for(let i =0; i <= 5; i++){
    //execute code sur chaque itération
}
```

## Foreach
Fait un tour avec chaque élément de la liste ou du tableau
```js
let tableau = ["A", "B", "C"];
tableau.forEach((element, index) => {
    //execute code on element
})
```

## While
Tourne tant qu'une condition est vraie

```js
let boucle = 0;
while(boucle < 5){
    boucle++;
    console.log(boucle);
}
```