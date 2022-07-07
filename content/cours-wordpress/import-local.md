+++
title = "Export et Import d'un site dans Local WP"
date =  2022-07-07T13:55:20+02:00
weight = 5
+++

## Export d'un site depuis local wp
- Dans la liste des sites sur local wp, clic droit > export
- Local va générer un fichier .zip que l'on pourra utiliser pour importer le site sur un autre ordinateur.

## Import d'un site dans local wp
- Dans local wp : Menu burger > Import site
- Choisir le fichier .zip précédemment généré lors de l'export.

Attention, si vous personnalisez le nom de domaine lors de l'import. Vous devez indiquer le nom de domaine **sans** le `.local`à la fin. (Sinon le site ne fonctionnera pas et affichera une erreur 404. Dans ce cas, voir la manip plus bas pour corriger ce problème.)

## Erreur 404 car j'ai mis `.local` à la fin du nom de mon site lors de l'importation

On peut voir si c'est le cas en regardant la colonne de gauche de wp local. Normalement le nom du site ne doit **pas** contenir `.local`. Si c'est le cas, c'est que le `.local` est en trop.

### Méthode 1 : la plus simple
1. Exporter le site qui pose problème.
2. Supprimer le site depuis local.
3. Le réimporter dans local en corrigeant le nom.

Il pourra être utile de redémarrer l'ordinateur si le problème n'est pas immédiatement résolu.

### Méthode 2 : si la première n'a pas fonctionné.

Sur local WP, dans l'onglet Overview, à la ligne `Site Domain` cliquez sur le bouton `Change` pour corriger le nom de domaine.

Si cela ne suffit pas à corriger le problème, il est possible qu'il faille aussi corriger cette information dans la base de données.
Sur la page du site dans Wp local, aller dans l'onglet "Database" et cliquer sur `Open Adminer`.
Rendez-vous dans la table `wp_options` sur l'onglet `Afficher les données`.
Corriger l'url du site sur les lignes `siteurl` et `home`.