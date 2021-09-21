# Javascript

## TPs Javascript individuels

TPs constitués par chacun des étudiants de la promotion. Ils servent d'introduction au Javscript.

- [TP1 - Bases syntaxiques de Javascript](js/TP1.ipynb)
- [TP2 - Javascript Orienté Objet](js/TP2.ipynb)

## Configuration de l'espace de travail

*Suivre les [étapes de création d'un environnement](./intro_python.html#creer-un-environnement-virtuel) virtuel Python et d'[installation de jupyter notebook](./intro_python.html#installer-et-lancer-jupyter).*

 ### Installer NodeJS

- Installer NVM pour créer un environnement virtuel NodeJS :
```bash
# Télécharger et installer NVM
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash

# Configurer l'environnement
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # Ceci charge NVM

# Télécharger la dernière version de Node
nvm install node
```

- Installer le kernel Javascript pour Jupyter notebook
```bash
npm install -g ijavascript
# installer
ijsinstall
```
- Lancer ``jupyter notebook``