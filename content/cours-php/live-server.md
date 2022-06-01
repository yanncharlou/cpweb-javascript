+++
title = "Live Server"
date =  2022-06-01T18:02:37+02:00
weight = 10
pre = "<b>Tip.</b> "
+++

## Utiliser Live Server (vscode) avec Xampp, WampServer, etc...

### En utilisant le mode proxy
1. Installer [VS Code](https://code.visualstudio.com/download) si ce n'est pas déjà fait. <sup>(editeur de code)</sup>
2. Installer l'extension vs code [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer).
3. Installer le plugin sur votre navigateur : [Chrome](https://chrome.google.com/webstore/detail/live-server-web-extension/fiegdmejfepffgpnejdinekhfieaogmj/) ou [Firefox](https://addons.mozilla.org/en-US/firefox/addon/live-server-web-extension/).
4. Démarrer votre serveur local (Xampp, WampServer, etc...)
5. Placez-vous dans le dossier PHP (htdocs généralement) ou éventuellement dans un de ses sous-dossiers et ouvrez-le dans vscode.
6. Depuis vscode, créez un fichier de configuration *`.vscode/settings.json`* d'après le modèle ci-dessous :

*`.vscode/settings.json`*
```js
{
    // Mainly for static files
    "liveServer.settings.useWebExt": true,

    // This means that you change your real URL (current PHP url) 
    // to another URL (which Live Sever starts).
    "liveServer.settings.proxy": {
        "enable": true,                             //   i. enabled
        "baseUri": "/",                             //  ii. workspace
        "proxyUri": "http://localhost:80/cpweb" // iii. l'adresse à laquelle vous accédez à votre dossier PHP sans live server.
    },
}

```
7. Ajustez le paramètre `proxyUri` pour qu'il indique l'adresse à laquelle vous vous connectez normalement à votre serveur local.
8. Cliquez sur le bouton `Go Live` dans la barre de statut de VSCode.

{{% notice tip %}}
Pour que cela fonctionne, vous devez rester sur l'url liveserver (ex : `http://127.0.0.1:5500`).
{{% /notice %}}

