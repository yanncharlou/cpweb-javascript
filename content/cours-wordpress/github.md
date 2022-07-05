+++
title = "Github"
date =  2022-07-05T12:03:12+02:00
weight = 20
+++

Github permet de travailler chacun de son côté sur des fichiers puis de mélanger les modifications de chacun.

{{% notice warning %}}
ATTENTION : Cette technique est assez avancée. Elle ne vous fera gagner du temps que si vous comprenez bien comment l'utiliser. A votre niveau, s'il n'y a pas trop de fichiers à modifier, il reste plus simple de se les échanger "à la main" via mail, etc...
{{% /notice %}}


Utiliser Git pour partager les modifications sur les fichiers :


## A faire par le "responsable" du projet. (il en faut bien un)

- Importer le site de départ sur chaque poste de travail.
- S'inscrire sur github (https://github.com)
- Créer un nouveau repository 
	- `+` (en haut à droite) > New Repository
	- Indiquer un nom (ex : projet-cpweb)
	- Choisir public ou private (selon si vous voulez ou non que n'importe qui puisse consulter le code source.)
	- Laissez les autres champs tels quels.

![Créer un dépôt](/cours-wordpress/git/git-new-repo.png);

- Sur l'écran suivant, vous trouverez les commandes pour configurer le repository sur votre ordinateur. (Ne fermez pas cet écran)
![Créer un dépôt](/cours-wordpress/git/git-add-repo-commands.png);

- Rendez-vous sur vscode (dans le dossier de votre site)
- Créez un fichier `.gitignore` dans la racine de votre dossier.
Ce fichier sert à indiquer les fichiers qui ne doivent pas être suivis par git.
Pensez à indiquer le bon dossier de votre theme.

```
/*
!.gitignore
!wp-content
wp-content/*

!wp-content/uploads

!wp-content/themes
wp-content/themes/*
!wp-content/themes/woocommerce-theme
```

- Allez sur Terminal > Nouveau terminal
- Executez la commande suivante : 
	git init

Vous devriez pouvoir voir la liste des fichiers modifiés dans l'onglet GIT de vscode.
Vérifiez qu'il ne manque pas de fichier devant être partagé et qu'il n'y en a pas en trop. Sinon corrigez le fichier .gitignore.

 - Utilisez le bouton "+" en haut de la liste pour ajouter toutes les modifications que vous voulez enregistrer.
 - Indiquez un commentaire pour décrire l'objet des modifications. (ex : premier commit)
 - Puis validez avec la coche.	
	
 - copier-coller la commande de la case "…or push an existing repository from the command line" de github dans le terminal.
 
 Github va normalement vous demander un Access Token, vous devez en créer un depuis Github via : Profil > Settings > Developper Settings > Personal access token

Normalement, vscode devrait alors envoyer vos fichiers modifiés sur le dépôt github. Vous devriez pouvoir les voir en vous rendant sur la page de votre repository dans github.

Une fois que tout est bon, il ne reste qu'à autoriser les autres membres du projet à accéder au repository.
Depuis github : Profil > Your repositories > Le projet > Settings > collaborators


## A faire par chacun des collaborateurs du projet

- Importer le site de départ sur chaque poste de travail.
- S'inscrire sur github (https://github.com)
- Vous devriez recevoir un invitation par mail du responsable du projet. (accepter l'invitation, etc...)

- Allez sur le dossier sur la page github du repository, dans l'onglet vert "Code" > HTTPS : copier l'adresse du dépôt.

- Allez sur Terminal > Nouveau terminal et collez les commandes suivantes (en reprenant l'url du dossier)
```
git remote add origin https://github.com/yanncharlou/projet-cpweb.git
git branch -M main
git pull
```
La commande devrait vous demander votre personnal token. Si vous ne le connaissez pas, vous pouvez en créer un nouveau dans Profil > Settings > Developper Settings > Personal access token

## Récupérer les modifications du dépôt principal
Onglet git > ... > Pull 

## Envoyer vos modifications sur de dépôt principal
- Onglet git
    - Utiliser le bouton "+" pour ajouter les modifications à envoyer.
    - Indiquer un commentaire dans la case "Message" et validez avec la coche.
    - puis ... push