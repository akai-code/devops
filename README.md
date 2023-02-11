# Table of contents 


- [1 - Introduction à l'architecture Cloud Native](#1---introduction-à-larchitecture-cloud-native)
  - [1.1 - Definition de cloud native](#11---definition-de-cloud-native)
  - [1.2 - Pourquoi utiliser une architecture cloud native ?](#12---pourquoi-utiliser-une-architecture-cloud-native-)
- [2 - Microservices](#2---microservices)
  - [2.1 - Qu'est-ce qu'un microservice ?](#21---quest-ce-quun-microservice-)
  - [2.2 - Avantages et inconvénients des microservices](#22---avantages-et-inconvénients-des-microservices)
  - [2.3 - Comment constriure une application microservice (cas pratique)](doc_img/microservices.md)
- [3 - Dockerization des microservices](#3---dockerization-des-microservices)
  - [3.1 - Qu'est-ce que Docker ?](#31---quest-ce-que-docker-)
  - [3.2 - Avantages et inconvénients de Docker](#32---avantages-et-inconvénients-de-docker)
  - [3.3 - Comment dockeriser une application (cas pratique)](doc_img/docker.md)
- [4 - Utilisation d'un orchestrateur de conteneurs](#4---utilisation-dun-orchestrateur-de-conteneurs)
  - [4.1 - Qu'est-ce qu'un orchestrateur de conteneurs ?](#41---quest-ce-quun-orchestrateur-de-conteneurs-)
  - [4.2 - Comment choisir un orchestrateur de conteneurs ?](#42---comment-choisir-un-orchestrateur-de-conteneurs-)
  - [4.3 - Comment intégrer l'orchestrateur de conteneurs à l'application (cas pratique)](doc_img/kubernetes.md)
- [5 - Déploiement de l'application](#5---déploiement-de-lapplication)
  - [5.1 - Choix du cloud provider](#51---choix-du-cloud-provider)
  - [5.2 - Comment déployer votre application sur le cloud (cas pratique)](doc_img/deployment.md)
  - [5.3 - Comment gérer les dependances et les ressources de votre application (cas pratique)](doc_img/kustomize.md)
- [6 - Monitoring et opérations](#6---monitoring-et-opérations)
  - [6.1 - Importance du monitoring dans une application cloud native](#61---importance-du-monitoring-dans-une-application-cloud-native)
  - [6.2 - Comment mettre en place un système de monitoring (cas pratique)](doc_img/monitoring.md)
  - [6.3 - Comment opérer et maintenir une architecture Cloud Native (cas pratique)](doc_img/operations.md)
- [7 - Conclusion](#7---conclusion)
  - [7.1 - Résumé de l'imprortance de l'architecture Cloud Native](#71---résumé-de-limprortance-de-larchitecture-cloud-native)
  - [7.2 - Récaptitulation des étapes de la construction d'une application cloud native](#72---récaptitulation-des-étapes-de-la-construction-dune-application-cloud-native)
  - [7.3 - Recommandations pour la suite](#73---recommandations-pour-la-suite)


# 1 - Introduction à l'architecture Cloud Native

## 1.1 - Definition de cloud native

L'architecture cloud native est une approche de conception d'application qui permet de construire et d'exécuter des applications dans un environnement distribué. Elle repose sur les principes suivants :

- Développement et déploiement automatisés
- Infrastructure et plateforme indépendantes
- Mesure de l'activité
- Évolutivité
- Élasticité
- Détection des erreurs
- Isolation des ressources

## 1.2 - Pourquoi utiliser une architecture cloud native ?

L'architecture cloud native permet de construire des applications qui sont :

- **Adaptatives** : elles peuvent s'adapter à l'environnement dans lequel elles sont déployées
- **Évolutives** : elles peuvent être facilement mises à jour
- **Scalables** : elles peuvent être facilement adaptées à la charge de travail
- **Sécurisées** : elles sont conçues pour être sécurisées
- **Fiables** : elles sont conçues pour être fiables
- **Performantes** : elles sont conçues pour être performantes

# 2 - Microservices

## 2.1 - Qu'est-ce qu'un microservice ?

Un microservice est une application qui est conçue pour être autonome et qui peut être déployée et mise à jour de manière indépendante. Il est composé d'une ou plusieurs fonctionnalités métier et il est conçu pour être déployé sur un environnement distribué. Il est également conçu pour être facilement maintenable et évolutif.

## 2.2 - Avantages et inconvénients des microservices

Les microservices ont de nombreux avantages :

- **Scalabilité** : les microservices peuvent être facilement déployés et mis à jour
- **Sécurité** : les microservices peuvent être facilement sécurisés
- **Fonctionnalités** : les microservices peuvent être facilement mis à jour
- **Maintenance** : les microservices peuvent être facilement maintenus
- **Performance** : les microservices peuvent être facilement optimisés

Les microservices ont également quelques inconvénients :

- **Complexité** : les microservices peuvent être complexes à maintenir
- **Dépendances** : les microservices peuvent être complexes à déployer
- **Sécurité** : les microservices peuvent être complexes à sécuriser

## 2.3 - Comment constriure une application microservice (cas pratique)

[doc_img/microservices.md](doc_img/microservices.md)

# 3 - Dockerization des microservices

## 3.1 - Qu'est-ce que Docker ?

Docker est un outil qui permet de créer des conteneurs. Un conteneur est un environnement d'exécution qui permet d'exécuter une application. Il est composé d'un système d'exploitation, d'une bibliothèque et d'une application. Il est conçu pour être isolé des autres conteneurs et pour être facilement déployé et mis à jour.

## 3.2 - Avantages et inconvénients de Docker

Les conteneurs Docker ont de nombreux avantages :

- **Sécurité** : les conteneurs Docker sont isolés les uns des autres
- **Maintenance** : les conteneurs Docker sont faciles à maintenir
- **Déploiement** : les conteneurs Docker sont faciles à déployer
- **Performance** : les conteneurs Docker sont faciles à optimiser

Les conteneurs Docker ont également quelques inconvénients :

- **Complexité** : les conteneurs Docker peuvent être complexes à maintenir
- **Dépendances** : les conteneurs Docker peuvent être complexes à déployer
- **Sécurité** : les conteneurs Docker peuvent être complexes à sécuriser

## 3.3 - Comment dockeriser une application (cas pratique)

[doc_img/docker.md](doc_img/docker.md)

# 4 - Utilisation d'un orchestrateur de conteneurs

## 4.1 - Qu'est-ce qu'un orchestrateur de conteneurs ?

Un orchestrateur de conteneurs est un outil qui permet de gérer et de déployer des conteneurs. Il permet de déployer des applications sur un environnement distribué. Il permet également de gérer les ressources de l'environnement distribué.

## 4.2 - Comment choisir un orchestrateur de conteneurs ?

Il existe plusieurs orchestrateurs de conteneurs. Chaque orchestrateur de conteneurs a ses propres avantages et inconvénients. Il est donc important de choisir l'orchestrateur de conteneurs qui correspond le mieux à vos besoins.

## 4.3 - Comment utiliser un orchestrateur de conteneurs (cas pratique)

[doc_img/orchestration.md](doc_img/orchestration.md)

# 5 - Déploiement de l'application

## 5.1 - Choix du cloud provider

Il existe plusieurs cloud providers. Chaque cloud provider a ses propres avantages et inconvénients. Il est donc important de choisir le cloud provider qui correspond le mieux à vos besoins.

## 5.2 - Comment déployer une application sur un cloud provider (cas pratique)

[doc_img/deployment.md](doc_img/deployment.md)

## 5.3 - Comment gérer les dependances et les ressources de votre application (cas pratique)

[doc_img/dependencies.md](doc_img/dependencies.md)

# 6 - Monitoring et opérations

































