# Gestion des Clés SSH

## Génération de la clé

1. Assurez-vous d'être dans le répertoire de déploiement.
2. Utilisez la commande `ssh-keygen -t ed25519 -a 100 -f ./deploy_key` pour générer une clé puissante.
3. Votre clé privée et publique seront dans le répertoire actuel.

## Ajouter la clé sur le serveur

1. Utilisez `ssh-copy-id -i <votre-clé-publique> <user>@<host>` pour copier la clé publique sur le serveur.
2. Vérifiez la connexion avec `ssh <user>@<host>`.
