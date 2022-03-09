# Training Docker for beginer 

Le but de cet atelier est de déployer une application front et une application backend en local de la même manière qu'elles seraient installées sur un server.

## Pré-requis

Un environnement linux de préférence, je n'ai réalisé cet exercice que sur une vm debian based pour l'instant

- git
- vim
- openssh-client
- python3-pip
- ansible (via `pip install ansible`)

## Atelier:

Récupérer les projets suivants

- Ansible Docker Install (À venir)
- Quote picker api: https://github.com/khantzen/training-docker-backend
- Quote picker front: ou https://github.com/khantzen/training-docker-front-end

> Le code et la configuration des deux applications n'ont pas besoin d'être modifié lors de l'atelier.

> Cet atelier n'a besoin que d'images officielles pour être réalisé.

> Il est préférable de réaliser cet atelier en compagnie d'un animateur ou avec la doc' docker à côté, cet énoncé se concentre surtout sur la pratique et peu sur la théorie.

### Étape de l'atelier

#### Installation de docker

- Installer docker en suivant ces étapes https://docs.docker.com/get-docker/ ou en suivant les instructions du projes "Ansible Docker Install"
- Lancer un conteneur hello-world `docker run hello-world`

#### Build les applications

- A l'aide de docker builder l'application *Quote Picker Api* 
- A l'aide de docker builder l'application *Quote Picker Front*

- Indications
> Vérifier la version de java dans le pom du quote picker api
> La commande pour compiler un projet maven: `mvn clean install`

> Le front est une appli node classique il vous faut lancer `npm install` avant de pouvoir en compiler un livrable avec `npm run build`

> Vous pouvez trouver des images officielles sur https://hub.docker.com/

Aides:
https://docs.docker.com/engine/reference/commandline/run/
https://docs.docker.com/storage/volumes/#start-a-container-with-a-volume

#### Démarrage de l'application

- A l'aide de docker, faites démarrer l'application *Quote Picker Api*
- Accéder à *Quote Picker Api* depuis le navigateur de votre VM

- Indications

> L'api écoute sur le port 4567 

> Pourquoi ne pas avoir un domaine quote-picker-api.local pour accéder à votre api depuis votre machine

- Accéder à quote-picker-api sans avoir à renseigner le port dans l'URL (À l'aide de docker ou nginx) 

#### Votre première image

- Construire une image docker dans le but d'héberger l'application *Quote Picker Api*
- Faire tourner votre conteneur *Quote Picker Api* et accédez y depuis le navigateur de votre VM

Aides
https://docs.docker.com/engine/reference/builder/
https://docs.docker.com/engine/reference/commandline/build/

#### Communication back et front

- Avec Nginx configurez un server http pour que l'application *Quote Picker Front* puisse communiquer avec le conteneur *Quote Picker Api*

https://docs.nginx.com/nginx/admin-guide/web-server/serving-static-content/

#### Votre deuxième conteneur

- Construire une image docker dans le but d'héberger l'application *Quote Picker Front*

#### Communication entre deux conteneurs

- A l'aide de docker-compose, assurez vous que le conteneur de votre application *Quote Picker Front* soit en mesure de communiquer avec le conteneur de *Quote Picker Api*

#### Activer le https

- Avec Lets Encrypt assurez vous que vous accédez de manière sécurisée à l'application en https



