# Docker

Docker est un système de conteneurisation permettant de faire tourner des applications et services assez et rapidement. À travers des fichiers de configuration, il est possible de déployer facilement des *containers* qui peuvent tourner ensuite dans des environnements de production. Docker permet aussi aux développeurs de travailler sur un même environnement de développement, avec les mêmes dépendances et versions de frameworks.

## Créer une image Docker (Dockerfile)

Chaque conteneur Docker doit reposer sur une image. De nombreuses images populaires prêtes à l'emploi sont disponibles sur [DockerHub](https://hub.docker.com/search?type=image). Dans notre cas, nous allons créer nous même notre image à partir d'une existante.

**Le fichier [Dockerfile](https://docs.docker.com/engine/reference/builder/) permet de construire une image.**

Dans le TD *hero-api*, voici à quoi peut ressembler le Dockerfile :

```dockerfile
# Image de base, Alpine: distro Linux très légère (5 MB)
FROM python:3.9.6-alpine

# Dossier de travail dans l'image
WORKDIR usr/src/app

# Installation des dépendances
RUN apk update \
&& apk add postgresql-dev gcc python3-dev musl-dev

COPY requirements.txt /usr/src/app/requirements.txt

# Installation des requirements
RUN pip install -r requirements.txt

RUN apk update \
    && apk add postgresql-dev gcc python3-dev musl-dev
```

Après, il faut construire l'image avec la commande : `docker build -t <nom de l'image>`

- `docker images` liste les images créées
- `docker image rm <nom de l'image>` supprime une image

## Lancer un conteneur

Pour lancer l'image précédement créé, nous utilisons : `docker run -p 8080:8000 -it <nom de l'image>`. On mappe avec l'option `-p` les ports du container à un de la machine. L'argument `-it` permet de lancer le container en mode intérctif, on entre dedans.

Si l'image du container n'est pas trouvée localement, Docker va directement chercher une image publique sur le Docker Hub. Exemple avec `docker run -it --rm busybox`.

## Docker-compose

## Liens utiles
- [Docker cheat sheet - commandes Docker](https://www.docker.com/sites/default/files/d8/2019-09/docker-cheat-sheet.pdf)
- [Docker Hub](https://hub.docker.com/)


Auteurs : **Reymond Arsène** ([@p0lycarpio](https://github.com/p0lycarpio)),  **Demart Erwan** ([@edemart](https://github.com/edemart))