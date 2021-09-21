# Python

## TPs Python individuels

TPs constitués par chacun des étudiants de la promotion. Ils servent d'introduction au Python.

- [TP1 - Bases syntaxiques de Python](python/TP1.ipynb)
- [TP2 - Python Orienté Objet](python/TP2.ipynb)


## Configuration de l'espace de travail

> Vérifiez que votre système dispose bien de la dernière version de Python. Si ce n'est pas le cas, [téléchargez-le](https://www.python.org/downloads/). L'utilisation d'un système Linux est recommandée.

 ### Créer un environnement virtuel

Dans le dossier du projet :
```bash
# version de Python par défaut
python3 -m venv venv
# en précisant la version de Python
virtualenv --python=/usr/bin/python3.8 venv 
# activation du venv
source venv/bin/activate
```
***NB:** Sur Windows, le dossier ``bin`` s'appelle ``Scripts``. Le script est ensuite éxecutable avec [PowerShell ou  cmd.exe](https://docs.python.org/fr/3/library/venv.html#creating-virtual-environments)*

### Installer et lancer jupyter
```bash
pip install jupyter notebook
jupyter notebook
```