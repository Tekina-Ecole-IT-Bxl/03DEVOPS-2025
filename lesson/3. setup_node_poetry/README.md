# Installation Nodejs et Poetry

## Objectifs de la session

L'objectif principal de cette session était d'apprendre à :

- Installer Node.js sur le serveur,
- Créer un projet Node.js dans un dossier dédié,
- Utiliser Neovim comme éditeur de texte pour leur code,
- Se familiariser avec les commandes de base de Neovim pour améliorer leur productivité.

## Étapes réalisées

### 1. Installation de Node.js

D'abord **accédé au serveur** puis **installé Node.js, npm, yarn**. L'installation permet de préparer l'environnement pour le projet Node.js à venir.

### 2. Création du dossier de travail

Ensuite **accéder au dossier sandbox** créé lors de la session précédente et à y créer un **dossier node**. Ce dossier servira de répertoire de travail pour toute les projets Node.js.

- **Commandes utilisées :**
  ```bash
  cd sandbox
  mkdir dode
  cd Node
  ```

### 3. Initialisation d'un projet Node.js

Dans le dossier **Node**, créé un dossier **Scraper**, à l'intérieur duquel ils ont initialisé un projet Node.js avec la commande suivante :

- **Commande utilisée :**
  ```bash
  mkdir Scraper
  cd Scraper
  yarn init -y
  ```

Ensuite répliqué le projet de **Scraping** que vous avaiez réalisé lors de la session précédente, en recopiant le même script.

### 4. Familiarisation avec Neovim

L'objectif de la session était aussi de **s'habituer à utiliser Neovim**. Vu/a voir :

- Ouvrir, éditer et sauvegarder des fichiers avec Neovim,
- Utiliser l'autocomplétion pour accélérer le développement,
- Utiliser des commandes basiques comme `:w` pour sauvegarder, `:q` pour quitter, et `:wq` pour sauvegarder et quitter,
- Manipuler du texte avec des commandes comme `y` pour copier, `p` pour coller, et `d` pour supprimer.
