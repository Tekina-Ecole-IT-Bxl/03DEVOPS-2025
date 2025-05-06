# 🧠 Jour 1 – Setup du pseudo-server & environnement DevOps

## 🎯 Objectifs du jour

- Se connecter à leur "pseudo-server" Docker
- Installer `powerlevel10k`
- Installer et configurer `neovim`
- Comprendre les bases de `vim` et la navigation dans un vrai terminal

---

## ETAPE 0 INSTALL LE SERVER D'ABORD!!!

## ⚙️ Étape 1 – Lancer le pseudo-server (Docker)

**Pré-requis Docker déjà installé sur la machine locale.**

```bash
ssh root@localhost -p 2222
```

---

## 🧪 Étape 2 – Installation de base dans le conteneur

### Mettre à jour les paquets

```bash
apt update && apt upgrade -y
```

### Installer les outils utiles

```bash
apt install -y curl git zsh neovim sudo openssh-server locales
```

---

## 🌈 Étape 3 – Installer powerlevel10k

### 1. Mettre ZSH comme shell par défaut

```bash
chsh -s $(which zsh)
```

Ensuite, relancer le shell ou taper `zsh`.

### 2. Installer oh-my-zsh

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### 3. Installer Powerlevel10k

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
```

Dans `~/.bashrc`, modifie cette ligne :

```bash
ZSH_THEME="powerlevel10k/powerlevel10k"
```

Puis recharge :

```bash
source ~/.bashrc
```

---

## 🧠 Étape 4 – Configurer Neovim

### 1. Créer la structure de config

```bash
mkdir -p ~/.config/nvim
```

### 2. Ajouter le gestionnaire de plugins (vim-plug)

```bash
curl -fLo ~/.local/share/nvim/site/autoload/plug.vim --create-dirs \
     https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

### 3. Installer wget 

```bash
apt install wget
```

### 4. Télécharger la config nvim avec cet command 
```bash
wget -P ~/.config/nvim/ https://raw.githubusercontent.com/Farid212/config-files/refs/heads/master/nvim/init.vim
```

Ensuite, dans Neovim, tape `:PlugInstall` pour installer tous les plugins.

---

## 🛠 Étape 5 – Config minimale Vim (au cas où)

Créer un fichier `.vimrc` si besoin :

```bash
nano ~/.vimrc
```

Colle :

```vim
set number
set cursorline
syntax on
set showmatch

set autoindent
set smartindent
set tabstop=2
set shiftwidth=2
set expandtab
set backspace=indent,eol,start

set mouse=a
set clipboard=unnamedplus
set encoding=UTF-8
set fileformat=unix
set completeopt=menuone,noinsert,noselect

set updatetime=300
set signcolumn=yes
```

---

## ✅ À la fin du jour 1, chaque étudiant devra :

- Pouvoir **se connecter à son conteneur**
- Avoir une interface shell propre avec **powerlevel10k**
- Utiliser **neovim** comme éditeur principal
- Être prêt à travailler sur Docker & les projets à venir
