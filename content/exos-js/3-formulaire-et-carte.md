+++
title = "Formulaire et carte"
date =  2022-04-19T14:02:22+02:00
weight = 30
pre = "<b>3.</b> "
+++

## Énoncé

Téléchargez les fichiers de départ de l'exercice : [exercice-3-formulaire-et-carte.zip](/exos-js/3-formulaire-et-carte/exercice-3-formulaire-et-carte.zip)

## Affichage d'une carte interactive

Une div `<div class="map" id="mapId"></div>` est déjà présente dans le fichier HTML.

L'objectif est d'afficher une carte interactive à l'intérieur.

Pour cela, aidez-vous de la documentation en ligne suivante : https://www.datavis.fr/maps/leaflet-firstmap

La documentation complète de la librairie est accessible ici : https://leafletjs.com/ mais vous ne devriez pas en avoir besoin pour cet exercice.

1. Affichez une carte à n'importe quelles coordonnées dans la div `<div class="map" id="mapId"></div>`
2. Centrez la carte sur Sud-Management ou n'importe quel endroit de votre choix.
    - Différentes solutions pour obtenir les coordonnées GPS d'un point : 
        - passer par Google Map et faire un clic droit sur la carte.
        - passer par https://www.openstreetmap.org et faire clic droit > afficher l'adresse.
        - https://www.gps-coordinates.net/
3. Ajoutez un pointeur (marker) sur l'adresse que vous avez choisi.

## Validation du formulaire

1. Interceptez l'envoi du formulaire pour pouvoir le valider.
    - par exemple en affichant une alerte ou un console.log
2. Validation du champ nom
    - ne doit pas être vide
    - doit faire au moins trois caractères
    - Si le champ est valide :
        - On met sa bordure en vert
    - Si le champ est invalide :
        - On met sa bordure en rouge
        - On affiche un message d'erreur dans la div `<div id="erreur-name"></div>`
3. Validation du champ mail
    - ne doit pas être vide
    - doit être conforme à la regex `/[a-zA-Z0-9._]*@[a-zA-Z0-9-]*\.[a-z]*/gm`
    - même comportement en cas de validation ou d'erreur que pour le champ name.
3. Validation du champ phone
    - peut être vide.
    - s'il est rempli, il doit être conforme à la regex `/^(?:(?:\+|00)33|0)\s*[1-9](?:[\s.-]*\d{2}){4}$/`
    - s'il est invalide : border rouge + message
    - s'il est vide : bordure lightgrey, pas de message 
    - s'il est valide : bordure verte
4. Validation du champ subject
    - ne doit pas être vide
    - doit faire entre 20 et 255 caractères
    - même comportement en cas de validation ou d'erreur que pour le champ name.

5. Vérifiez que le formulaire n'est pas envoyé si un champ présente une erreur.