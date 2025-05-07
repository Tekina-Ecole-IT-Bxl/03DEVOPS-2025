# Decouvert de Poetry, init django

## Objectifs de la session

L'objectif de la session était de :

- Installer et configurer Python, PIP, et Poetry,
- Apprendre à créer et gérer un projet Python avec Poetry,
- Installer Django et comprendre le versionning des dépendances,
- Créer un projet Django de base et démarrer le serveur.

## Étapes réalisées

### 1. Installation de Python, PIP et Poetry

d'abord installé Python, PIP et Poetry sur le serveur afin de préparer l'environnement de développement Python.

### 2. Création du dossier de travail

Dans le dossier **sandbox**, créé un dossier **Python**, puis un sous-dossier **TestProject**, qui servira de projet de test pour la session.  
Les commandes utilisées étaient les suivantes :

```bash
cd ~/sandbox
mkdir python
cd python
mkdir testproject
cd testproject
```

3. Initialisation du projet avec Poetry

utilisé Poetry pour initialiser un nouveau projet Python dans le dossier TestProject :

```bash
poetry init
```

le fichier pyproject.toml est généré, qui contient les informations de configuration du projet.

4. Installation de Django avec Poetry

Ensuite, installé Django avec Poetry en utilisant la commande suivante :

```bash
poetry add django
```

Cependant, un problème surviendras lors de l’installation car Django:latest nécessitait une version de Python supérieure à 3.10, mais le serveur était limité à Python 3.9.2 (version LTS de Debian).

5. Résolution du problème de version de Python

Deux solutions possibles pour résoudre ce problème : 1. Télécharger et installer une version plus récente de Python depuis le site officiel de Python. 2. Utiliser une version précédente de Django (par exemple, la version 4.5 ou 4.7), compatible avec Python 3.9.2.

6. Création du projet Django

Une fois Django installé, ont créé un nouveau projet Django avec Poetry en utilisant la commande suivante :

```bash
poetry run django-admin startproject nom_du_projet
```

Cela a créé la structure de base du projet Django.

7. Création de la base de données

Ensuite exécuté la commande pour créer les migrations et la base de données :

```bash
poetry run python manage.py migrate
```

Cela a permis de générer toutes les migrations nécessaires et de configurer la base de données.

8. Lancement du serveur Django

Enfin, démarré le serveur Django pour vérifier que tout fonctionnait correctement avec la commande suivante :

```bash
poetry run python manage.py runserver
```

Si le serveur démarre alors ta bien suivis le tuto sinon recommence tout...
