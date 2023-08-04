# Installation d'Ansible dans un environnement virtuel Python3

1. Assurez-vous que Python3 est installé sur votre machine.
2. Installez virtualenv avec la commande `pip install virtualenv`.
3. Créez un environnement virtuel avec `virtualenv -p python3 venv`.
4. Activez l'environnement avec `source venv/bin/activate`.
5. Installez Ansible dans l'environnement virtuel avec `pip install -r requirements.txt`.
6. Verifiez l'installation avec `ansible --version`.
