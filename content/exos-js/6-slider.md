+++
title = "Slider"
date =  2022-04-19T14:02:22+02:00
weight = 60
pre = "<b>6.</b> "
+++

## Énoncé

### Étape 1

- Téléchargez les fichiers de départ : [exercice-6-slider.zip](/exos-js/6-slider/exercice-6-slider.zip)

- Créez une fonction `display(n)`. A la fin de l'exercice, cette fonction aura pour objectif d'afficher l'image de rang `n` et de masquer les autres.

- Au départ, on appellera directement la fonction avec une valeur arbitraire pour tester.

```js
var slideEnCours = 1;
display(slideEnCours);

function display(n) {
    // Affiche le slide n
}
```

Dans la fonction :

- Récupérer la liste des images dans une variable.
- Masquer toutes les images sauf celle qui porte le rang n

{{%expand "Aide ?" %}}Pour afficher ou masquer une image on peut utiliser la directive css opacity . L'image est transparente quand elle vaut 0, et opaque quand elle vaut 1. {{% /expand%}}

### Étape 2

Afficher la bonne image quand on clique sur un des boutons `class="indicator"`.

### Étape 3

Afficher l'image suivante ou précédente quand on clique sur les flèches.

{{%expand "Aide ?" %}}
Le principe consiste à ajouter ou soustraire 1 à la variable `slideEnCours` puis à rappeler la fonction display(slideEnCours); 
Attention de prévoir le cas où slideEnCours devient supérieur au dernier slide ou inférieur à 0.
{{% /expand%}}

### Étape 4

Changer la couleur de l'indicateur `class="indicator"` dont le slide correspondant est actif.

{{%expand "Aide ?" %}}
Le plus simple sera de le faire directement dans la fonction `display(n)`.
{{% /expand%}}
