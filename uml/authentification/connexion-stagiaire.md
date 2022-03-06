## cas d'utilisation
```mermaid
graph LR
    utilisateur{{utilisateur}} --- connexion[se connecter] & passe-o[mot de passe oublié]
    connexion --> |include| e-mail[e-mail ou nom d'utilisateur] & passe[mot de passe]
    restez[restez connecté] -.-> |extend| connexion
    
    %% liens
    click passe-o "https://github.com/idlli/projet-de-stage/blob/main/uml/authentification/mot-de-passe-oublié.md" _blank
```
## séquence
```mermaid
sequenceDiagram
    actor stagiaire
    participant site as site web
    participant serveur as serveur web
    alt se connecter
        stagiaire ->>+ site : onclick(se_connecter)
        site ->> site : validation du formulaire
        note right of site : e-mail et mot de passe
        alt formulaire valide
            site ->>+ serveur : trouver(stagiaire)
            serveur ->> serveur : trouver le stagiaire
            serveur -->>- site : répondre
            alt stagiaire existe
                alt restez connecté
                    site ->> site : produire(chaîne_de_connexion)
                    site ->>+ serveur : insérer(chaîne_de_connexion)
                    serveur ->> serveur : insérer la chaîne de connexion
                    serveur -->>- site : répondre
                    site ->> site : cookie(chaîne_de_connexion)
                end
                site ->> site : redirection(tableau-de-bord.php)
            end
        end
        site -->>- stagiaire : message()
    else mot de passe oublié
        stagiaire ->> site : onclick(mot_de_passe_oublié)
        site ->> site : redirection(mot-de-passe-oublié.php)
    end
```
