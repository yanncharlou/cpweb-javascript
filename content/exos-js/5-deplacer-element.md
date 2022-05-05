+++
title = "Déplacer un élément"
date =  2022-04-19T14:02:22+02:00
weight = 50
pre = "<b>5.</b> "
+++

## Énoncé

- Créez une page web
- Ajoutez dessus :
    - Un paragraphe contenant n'importe quel texte.
    - Un bouton "Déplacer vers la gauche"
    - Un bouton "Déplacer vers la droite"
- Faites en sorte que :
    - Si on clique sur le bouton "Déplacer vers la gauche", le paragraphe se déplace vers la gauche.
    - Si on clique sur le bouton "Déplacer vers la droite", le paragraphe se déplace vers la droite.

{{%expand "Aide ?" %}}L'astuce consiste à modifier les css du paragraphe à chaque clic pour qu'il se déplace. Vous pouvez par exemple mettre l'élément en `position:relative` puis modifier sa directive `left` en css.
{{% /expand%}}
