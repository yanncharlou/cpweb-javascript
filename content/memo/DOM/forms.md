+++
title = "Formulaires"
date =  2022-04-18T20:18:49+02:00
weight = 40
+++

## Récupérer un formulaire et ses champs

On peut récupérer le formulaire comme les autres éléments avec `document.getElementById()`;

```js
let champ = document.getElementById("mon-champ");
let valeurChamp = champ.value;
let valeurChamp = document.getElementById("mon-champ").value;
```

On peut aussi utiliser `document.forms` qui contient la liste de tous les formulaires de la page.
On pourra même récupérer un champ spécifique d'un formulaire de cette manière :

```js
let champ = document.forms['id_du_formulaire'].elements['name_du_champ'];
let valeurChamp = document.forms['id_du_formulaire'].elements['name_du_champ'].value;
```

## Valider un formulaire

### Avec un événement

```js
let formulaire = document.getElementById("formulaire");
formulaire.addEventListener('submit', function(e) {
    let valid = true;

    //ici on vérifie les champs
    //on met valid à false en cas d'erreur
    //on affiche des messages d'erreur

    //si valid = false, alors on empêche l'envoi du formulaire.
    //formulaire.checkValidity() sert à vérifier le formulaire avec la validation HTML5 (les champs type=email etc...)
    if(!valid || !formulaire.checkValidity()){
        e.preventDefault();
    }
})
```

### Avec l'attribut onSubmit
```js
let formulaire = document.getElementById("formulaire");
formulaire.onsubmit = function(e) {
    let valid = true;

    //ici on vérifie les champs
    //on met valid à false en cas d'erreur
    //on affiche des messages d'erreur

    //si valid = false, alors on empêche l'envoi du formulaire.
    //formulaire.checkValidity() sert à vérifier le formulaire avec la validation HTML5 (les champs type=email etc...)
    if(!valid || !formulaire.checkValidity()){
        return false;
    }
    return true;
}
```

NOTE : On préfèrera souvent valider directement les champs du formulaire sur "change" ou "blur" pour ne pas avoir à attendre que le visiteur clique sur "Envoyer" pour lui afficher les erreurs.

## Vérifier les valeurs des champs

```js
    let nom = document.getElementById("name"); //mon champ à vérifier
    let erreurName = document.getElementById("erreur-name"); //une div à côté du champ dans laquelle je mettrait le message d'erreur.

    if(nom.value === "") {
        nom.style.borderColor = 'red'
        erreurNom.style.color = 'red'
        erreurNom.innerHTML = 'Ce champ est requis.'
        valid = false
    }else if(nom.value.length < 3){
        nom.style.borderColor = 'red'
        erreurNom.style.color = 'red'
        erreurNom.innerHTML = 'Ce champ doit être rempli avec au moins trois caractères.'
        valid = false
    }else{
        nom.style.borderColor = 'green'
        erreurNom.innerHTML = ''
    }

```
### Validation avec Regex

Les Regex (Expressions Régulières) sont un langage qui permet de décrire le format que doit avoir un texte.
On s'en sert souvent pour valider les adresses e-mail ou les numéros de téléphone.

Vous trouverez souvent sur le net des regex toutes prêtes.

```js
    let phoneRegex = /^(?:(?:\+|00)33|0)\s*[1-9](?:[\s.-]*\d{2}){4}$/
    let emailRegex = /[a-zA-Z0-9._]*@[a-zA-Z0-9-]*\.[a-z]*/gm

    let email = document.getElementById("email");

    if(emailRegex.test(email.value) === false){
        console.log("Mail invalide");
    }
```

**Astuce** : Vous pouvez tester une regex en live sur https://regex101.com/ .
Vous y trouverez aussi une librairie de regex toutes prêtes.
