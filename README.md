# Le Comptoir des Frères — versions publiées

Ce dépôt ne contient **que les versions publiées** de l'outil de gestion (paquets de mise à jour signés).
Le code source est dans un dépôt privé.

Chaque version (onglet *Releases*) contient trois fichiers :

| Fichier | Rôle |
|---|---|
| `comptoir-des-freres-mise-a-jour-X.Y.Z.zip` | Le programme (sans aucune donnée d'établissement) |
| `mise-a-jour.json` | Version, taille et empreinte SHA-256 du paquet |
| `mise-a-jour.json.sig` | Signature Ed25519 de `mise-a-jour.json` |

L'outil installé lit la dernière version publiée ici, vérifie la signature avec la clé publique qu'il contient,
puis l'empreinte du paquet. Un paquet dont la signature ne correspond pas est refusé.
