+++
title = "Tips en vrac"
date =  2022-07-05T15:17:45+02:00
weight = 30
+++

## Un sous menu bootstrap "du pauvre"

{{% notice warning %}}
Cette méthode est juste "pour dépanner". L'idéal étant d'utiliser un walker bootstrap pour générer un menu bootstrap complet.
{{% /notice %}}

En supposant que votre navigation principale est codée "en dur" et que cela serait plus pratique d'avoir quelques menus déroulants modifiables depuis l'administration.

### Déclarer un nouveau menu
Dans functions.php 

A adapter en fonction de vos besoins.
```php
function add_theme_submenus() {
  register_nav_menu('sous-menu-1',__( 'Sous menu 1' ));

}
add_action( 'init', 'add_theme_submenus' );
```

### Afficher le sous menu dans le menu principal bootstrap.

Dans le fichier qui affiche le menu principal bootstrap 4 (par exemple `template-parts/main-nav.php`).

```html
    <li class="nav-item dropdown">
        <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-expanded="false">
            Sous menu 1
        </a>
            <?php wp_nav_menu([
                'theme_location' => 'sous-menu-1',
                'container'            => 'div',
                'container_class'      => 'dropdown-menu',
                'container_id'         => 'navbarDropdown',
            ]); 
            ?>
    </li>
```

Il ne restera plus qu'à ajouter éventuellement un peu de css pour masquer les puces.