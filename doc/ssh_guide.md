# Gestion des Clés SSH

## Génération de la clé

1. Assurez-vous d'être dans le répertoire de déploiement.
2. Utilisez la commande `ssh-keygen -t ed25519 -a 100 -f ./deploy_key -N ""` pour générer une clé puissante.
3. Votre clé privée et publique seront dans le répertoire actuel.

## Ajouter la clé sur le serveur

1. Afficher la clé publique sur votre machine locale.
    ```bash
    cat deploy_key.pub
    ```
2. Copiez la sortie (c'est la clé publique) dans votre presse-papiers.
3. Connectez-vous au serveur distant.
4. Créez le répertoire .ssh dans votre répertoire personnel si ce n'est pas déjà fait.
    ```bash
    mkdir -p ~/.ssh
    ```
5. Ouvrez ou créez le fichier ~/.ssh/authorized_keys en utilisant un éditeur comme nano ou vi.
    ```bash
    nano ~/.ssh/authorized_keys
    ```
6. Collez la clé publique (que vous avez copiée à l'étape 2) à la fin du fichier.
7. Sauvegardez et fermez le fichier.
8. Changez les permissions du fichier pour le sécuriser.
    ```bash
    chmod 600 ~/.ssh/authorized_keys
    ```
9. Retournez sur le terminal de votre ordinateur (pas le serveur) puis aller dans le repertoire de kit-deploiement
10. Vérifiez la connexion avec la clé privée.
    ```bash
    ssh -i deploy_key.pub <user>@<host>
    ```
