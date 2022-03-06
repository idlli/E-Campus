## cas d'utilisation
```mermaid
graph LR
    administrateur-l{{administrateur limité}} --- profil & paramètres & notifications & demandes & déconnecter[se déconnecter]
```
## séquence
```mermaid
sequenceDiagram
    actor administrateur_l as administrateur limité
    participant site as site web
    par profil
        administrateur_l ->> site : onclick(profil)
        site ->> site : redirection(profil.php)
    and settings
        administrateur_l ->> site : onclick(paramètres)
        site ->> site : redirection(paramètres.php)
    and notifications
        administrateur_l ->> site : onclick(notifications)
        site ->> site : redirection(notifications.php)
    and requests
        administrateur_l ->> site : onclick(demandes)
        site ->> site : redirection(demandes.php)
    and logout
        administrateur_l ->> site : onclick(se_déconnecter)
        site ->> site : supprimer_cookie(chaîne_de_connexion)
        site ->> site : redirection(connexion.php)
    end
```
