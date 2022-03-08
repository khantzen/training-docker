# Training Docker for beginer 

Slides: https://docs.google.com/presentation/d/177G9D130jxb59elNG4qItYKd6ikAwTENpRZMYFNjnuQ/edit?usp=sharing

Le but de cette première journée est de déployer une application front et une application backend en local de la même manière qu'elles seront installés sur un server.

## Pré-requis

Une vm linux debian based en ayant installé

- git
- vim
- openssh-client
- python3-pip
- ansible (via `pip install ansible`)

## Atelier:

Sur le gitlab arolla, récupérer les projets suivants

- GuildeDevops / Ansible Docker Install
- GuildeDevops / Arollacademy Quote picker api
- GuildeDevops / Arollacademy Quote picker front


### Étape de l'atelier

#### Installation de docker

- Suivez les instructions pour installer docker à l'aide du projet "Ansible Docker Install"

#### Build les applications

- A l'aide de docker builder l'application *Quote Picker Api* 
- A l'aide de docker builder l'application *Quote Picker Front*

#### Démarrage de l'application

- A l'aide de docker, faites démarrer l'application *Quote Picker Api*
- Accéder à *Quote Picker Api* depuis le navigateur de votre VM

#### Votre première image

- Construire une image docker dans le but d'héberger l'application *Quote Picker Api*
- Faire tourner votre conteneur *Quote Picker Api* et accédez y depuis le navigateur de votre VM

#### Communication back et front

- Avec Nginx configurez un server http pour que l'application *Quote Picker Front* puisse communiquer avec le conteneur *Quote Picker Api*

#### Votre deuxième conteneur

- Construire une image docker dans le but d'héberger l'application *Quote Picker Front*

#### Communication entre deux conteneurs

- A l'aide de docker-compose, assurez vous que le conteneur de votre application *Quote Picker Front* soit en mesure de communiquer avec le conteneur de *Quote Picker Api*

#### Activer le https

- Avec Lets Encrypt assurez vous que vous accédez de manière sécurisée à l'application en https



