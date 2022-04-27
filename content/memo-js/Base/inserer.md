---
title: Insérer du javascript dans une page HTML
description : "Comment utiliser JS ?"
weight: 10
---

## Via un fichier javascript externe (conseillé)
C'est le même principe que pour les fichiers CSS mais avec une balise `<script></script>`.


{{% notice note %}}
Bien mettre la balise juste avant `</body>` pour que le script ne soit lancé qu'une fois la page complètement lue par le navigateur.
{{% /notice %}}

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Titre de la page</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>mon titre</h1>
    <img id="image" src="images/image-1.jpg" alt="texte alternatif" width="250px" height="250px">

    <!-- Ici le chargement de mon script JS -->
    <script src="script.js"></script>
</body>
</html>
```

## Directement dans la page

En mettant directement le code javascript dans une balise `<script></script>`.
On peut mettre cette balise dans le `<head></head>` ou dans le `<body></body>`.

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Titre de la page</title>
    <link rel="stylesheet" href="styles.css">

    <!-- directement dans le head -->
    <script>
        console.log("Youpi mon Javascript est dans le head !");
    </script>
</head>
<body>
    <h1 id="titre">mon titre</h1>
    <img id="image" src="images/image-1.jpg" alt="texte alternatif" width="250px" height="250px">

    <!-- directement dans le body -->
    <script>
        console.log("Youpi mon Javascript est dans le body !");
    </script>
</body>
</html>
```