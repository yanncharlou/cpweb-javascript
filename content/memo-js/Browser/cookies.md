+++
title = "Cookies"
date =  2022-04-18T21:11:58+02:00
weight = 10
+++

Un cookie est une donnée stockée dans un petit fichier texte qu'un site peut laisser dans le navigateur du visiteur.
Lors d'une prochaine visite, le site pourra accéder aux données sauvegardées dans le cookie.

## Ecrire un cookie

```js
// document.cookie ajoute un cookie dans le fichier texte.
document.cookie= "name=Sylvain;";
document.cookie= "work=helper; expires=Thu, 05 Oct2021 12:00:00 UTC; path=/;";

// retourne tous les cookies dans une chaîne de caracteres. (Le fichier texte complet)
console.log(document.cookie);
```

## Lire un cookie

Comme `document.cookie` contient toutes les valeurs bout à bout, on préfère passer par une fonction spéciale qui permet de récupérer une seule valeur :

```js
function getCookie(cname) {
  let name = cname + "=";
  let decodedCookie = decodeURIComponent(document.cookie);
  let ca = decodedCookie.split(';');
  for(let i = 0; i <ca.length; i++) {
    let c = ca[i];
    while (c.charAt(0) == ' ') {
      c = c.substring(1);
    }
    if (c.indexOf(name) == 0) {
      return c.substring(name.length, c.length);
    }
  }
  return "";
}

let name = getCookie("name"); //name contiendra "Sylvain"

```