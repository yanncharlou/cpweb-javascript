+++
title = "Web roulette"
date =  2022-04-19T14:02:22+02:00
weight = 60
pre = "<b>6.</b> "
+++

## Énoncé

### Étape 1
- Créez une page web
- Ajoutez dessus :
    - Un bouton "webroulette"
- Faites en sorte que si on clique sur le bouton le visiteur soit redirigé vers un site web au hasard. 

#### Astuces : 

Stockez la liste des urls des sites dans un tableau javascript.
Tirez au hasard une case de ce tableau et utilisez sa valeur pour rediriger le visiteur.

#### Proposition de liste :

{{% notice warning %}}
Interdiction d'aller sur ces adresses autrement qu'en utilisant le script. Ce sera votre récompense quand vous aurez réussi. ;-)
{{% /notice %}}

```
https://www.youtube.com/watch?v=dQw4w9WgXcQ
https://www.youtube.com/watch?v=LkCEXsIphWY
https://www.youtube.com/watch?v=BuMCZHyGwXw
https://www.youtube.com/watch?v=AfeAhCWaMD0
https://www.youtube.com/watch?v=QEM0r0t88Mg
https://www.youtube.com/watch?v=WHDdCqz5kck
```

{{%expand "Aide ?" %}}

- [Tableaux]({{< ref "memo-js/Base/tableaux.md" >}})
- [Changer de page]({{< ref "memo-js/Browser/page.md" >}})

{{% /expand%}}

### Étape 2

- Ajouter un bouton "+" sur la page.
- Faites en sorte que lorsqu'on clique sur le bouton, une fenêtre s'ouvre pour demander une nouvelle url et que cette url soit ajoutée dans le tableau afin qu'elle puisse être tirée au sort comme les autres.

{{%expand "Aide ?" %}}https://www.w3schools.com/jsref/met_win_prompt.asp{{% /expand%}}