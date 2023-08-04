# Agence Déploiement Express

## Introduction

Bienvenue dans le référentiel d'Agence Déploiement Express, où vous trouverez tout ce dont vous avez besoin pour configurer et déployer rapidement votre site web ou application. Ce projet est conçu pour vous rendre autonome, vous permettant de saisir pleinement la fonctionnalité, de l'adapter à vos besoins et de réussir de manière indépendante.

## Table des matières

- [Prérequis](#prérequis)
- [Installation](#installation)
  - [Configuration de l'environnement virtuel](#configuration-de-lenvironnement-virtuel)
  - [Clés SSH](#clés-ssh)
- [Déploiement](#déploiement)
- [Support](#support)

## Prérequis

- Python 3.x
- Ansible
- Accès SSH à vos serveurs

## Installation

### Configuration de l'environnement virtuel

1. Installez `virtualenv` si vous ne l'avez pas déjà :

   ```bash
   pip3 install virtualenv
   ```
2. Création du virtualenv nommé venv :
   ```bash
   virtualenv -p python3 venv
   ```
3. On source le virtualenv pour l'utiliser :

   ```bash
   source venv/bin/activate
   ```
4. On installe les prérequis de déploiement (ansible et ses modules) :

   ```bash
   pip install -r requirements.txt
   ```

## Clés SSH

1. Assurez-vous de suivre la procédure de gestion des clés SSH (doc/ssh_guide.md) et d'être dans le dossier de déploiement.

## Déploiement

Chaque playbook à un objectif précis, voici comment lancer un playbook

1. Modifiez l'inventaire (inventory.ini) pour correspondre à votre configuration de serveur.
2. Exécutez le playbook pour déployer votre site ou application :
```bash
ansible-playbook playbooks/nom_du_playbook.yml
```

## Support

Si vous rencontrez des problèmes ou avez des questions concernant le déploiement, n'hésitez pas à contacter notre équipe de support technique. Vous pouvez nous joindre par :

- **Email** : contact@linux-man.fr

Nous nous engageons à répondre à vos demandes dans les plus brefs délais et à vous fournir l'assistance nécessaire pour une mise en place réussie.
