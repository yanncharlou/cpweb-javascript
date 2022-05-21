---
title: Accéder à l'HTML
description : ""
weight: 10
---

{{% notice tip %}}
Besoin d'une explication détaillée parce que vous n'avez rien compris ?
<a href="https://openclassrooms.com/fr/courses/5543061-ecrivez-du-javascript-pour-le-web/5577476-accedez-aux-elements-du-dom" target="_blank">ICI</a>
{{% /notice %}}

## Comment récupérer un élement HTML

### Par son ID

**html**
```html
<div id="idDeMonElement"></div>
```
**js**
```js
let monElement = document.getElementById('idDeMonElement');
```

### Avec un sélecteur CSS

**html**
```html
<div id="idDeMonElement">A</div>
<div class="element">B</div>
```

**js**
```js
let monElementA = document.querySelector("#idDeMonElement");
let monElementB = document.querySelector(".element");
```


## Comment récupérer plusieurs élements HTML d'un seul coup

```javascript
var elements = document.getElementsByClassName('toto'); // class="toto"
var elements = document.getElementsByName('toto'); // name="toto"
var elements = document.getElementsByTagName('h1'); // <h1>...</h1>
```
Ces commandes retournent une liste d'éléments. On utilisera souvent ensuite une boucle pour faire des modifications dessus.