+++
title = "Evenements"
date =  2022-04-18T19:43:22+02:00
weight = 20
+++

Les événements se produisent lorsqu'il se passe quelque chose sur la page.

Ex : la page vient de finir de se charger, l'utilisateur vient de cliquer sur quelque chose,...

## Ecouter un événement en javascript pur (conseillé)
```html
<button id="mon-bouton">Mon bouton</button>
```

```js

// j'écoute le clic sur le bouton
let monBouton = document.getElementById("mon-bouton");
monBouton.addEventListener('click', function(e) {
    console.log("Clic sur le bouton");
    monBouton.style.backgroundColor  = "red";
})

// j'écoute l'appui sur une lettre du clavier
//keypress marche avec les touches lettrées, keydown détecte toutes les touches du clavier.
document.addEventListener("keydown", function (e) {
    console.log(e['key']); // affiche la touche dans la console.
    if (e['key'] == 'c') {
        alert("Vous avez appuyé sur la touche c.");
    }
})
```

Astuce, on peut utiliser la commande `e.preventDefault()` pour empêcher que les d'autres fonctions qui écoutent le même évenement ne s'executent après la notre. Très utile si on veut valider un formulaire et qu'on ne veut pas qu'il soit envoyé ou qu'on a pas envie qu'un lien s'execute. 

### Quelques événements courants

| **événement** | **description** |
|--------------|-----------------|
| change | L'élément à changé |
| click | L'utilisateur a cliqué sur l'élément |
| blur | L'élément vient de perdre le focus |
| mouseover | La souris vient de passer au-dessus de l'élément |
| mouseout | La souris vient de quitter l'élément |
| keydown | L'utilisateur a appuyé sur une touche du clavier (inclus CTRL, etc...) |
| keypress | L'utilisateur a appuyé sur une touche de lettre ou chiffre du clavier |
| load | Le navigateur a fini de charger la page |

## Écouter un événement via un attribut HTML

### directement dans le html
**html**
```html
<button onclick="clicSurBouton()">Mon bouton</button>
```
**javascript**
```js
function clicSurBouton(){
    console.log("clic sur bouton !");
}
```

### via javascript
```html
<button id="mon-bouton">Mon bouton</button>
```
**javascript**
```js
let monBouton = document.getElementById("mon-bouton");
monBouton.onclick = function(){
    console.log("clic sur bouton !");
}
```

### Quelques attributs courants

| **attribut** | **description** |
|--------------|-----------------|
| onchange | L'élément à changé |
| onclick | L'utilisateur a cliqué sur l'élément |
| onblur | L'élément vient de perdre le focus |
| onmouseover | La souris vient de passer au-dessus de l'élément |
| onmouseout | La souris vient de quitter l'élément |
| onkeydown | L'utilisateur a appuyé sur une touche du clavier |
| onload | Le navigateur a fini de charger la page |
