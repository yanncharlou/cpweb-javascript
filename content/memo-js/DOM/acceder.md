---
title: Accéder à l'HTML
description : ""
weight: 10
---

## Comment récupérer un élement HTML

**html**
```html
<div id="idDeMonElement"></div>
```
**js**
```js
let monElement = document.getElementById('idDeMonElement');
```

## Comment récupérer plusieurs élements HTML d'un seul coup

```javascript
var elements = document.getElementsByClassName('toto'); // class="toto"
var elements = document.getElementsByName('toto'); // name="toto"
var elements = document.getElementsByTagName('h1'); // <h1>...</h1>
```
Ces commandes retournent une liste d'éléments. On utilisera souvent ensuite une boucle pour faire des modifications dessus.