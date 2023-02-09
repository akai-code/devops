# Table of contents 


- [1 - Introduction à la conception d'une application cloud native](#1---introduction-a-la-conception-d-une-application-cloud-native)
  - [1.1 - Présentation des microservices et leur rôle dans une application cloud native](#11---presentation-des-microservices-et-leur-role-dans-une-application-cloud-native)
  - [1.2 - Objectifs de la mise en place de l'application](#12---objectifs-de-la-mise-en-place-de-l-application)
- [2 - Planification des microservices](#2---planification-des-microservices)
  - [2.1 - Analyse de la fonctionnalité requise pour chaque microservice](#21---analyse-de-la-fonctionnalite-requise-pour-chaque-microservice)
  - [2.2 - Détermination des dépendances entre les microservices](#22---determination-des-dependances-entre-les-microservices)
  - [2.3 - Planification de la répartition des responsabilités entre les microservices](#23---planification-de-la-repartition-des-responsabilites-entre-les-microservices)
- [3 - Mise en place des microservices](#3---mise-en-place-des-microservices)
  - [3.1 - Développement des microservices en utilisant les technologies appropriées](#31---developpement-des-microservices-en-utilisant-les-technologies-appropriees)
  - [3.2 - Tests unitaires et de bout en bout pour les microservices](#32---tests-unitaires-et-de-bout-en-bout-pour-les-microservices)
  - [3.3 - Déploiement des microservices en utilisant des conteneurs](#33---deploiement-des-microservices-en-utilisant-des-conteneurs)
- [4 - Orchestration avec Kubernetes](#4---orchestration-avec-Kubernetes)
  - [4.1 - Présentation de Kubernetes et ses fonctionnalités](#41---presentation-de-Kubernetes-et-ses-fonctionnalites)
  - [4.2 - Configuration des objets Kubernetes pour gérer les microservices](#42---configuration-des-objets-Kubernetes-pour-gerer-les-microservices)
  - [4.3 - Mise en place de la mise à l'échelle et de la fiabilité en utilisant les fonctionnalités de Kubernetes](#43---mise-en-place-de-la-mise-a-l-echelle-et-de-la-fiabilite-en-utilisant-les-fonctionnalites-de-Kubernetes)
- [5 - Surveillance et tests](#5---surveillance-et-tests)
  - [5.1 - Mise en place de l'outil de surveillance pour surveiller les microservices](#51---mise-en-place-de-l-outil-de-surveillance-pour-surveiller-les-microservices)
  - [5.2 - Écriture de tests pour vérifier la qualité et la disponibilité des microservices](#52---ecriture-de-tests-pour-verifier-la-qualite-et-la-disponibilite-des-microservices)
  - [5.3 - Configuration de l'outil de test pour s'exécuter automatiquement en cas de modification du code](#53---configuration-de-l-outil-de-test-pour-s-exécuter-automatiquement-en-cas-de-modification-du-code)
- [6 - Déploiement et mise à l'échelle](#6---deploiement-et-mise-a-l-echelle)
  - [6.1 - Préparation du déploiement dans le cloud](#61---preparation-du-deploiement-dans-le-cloud)
  - [6.2 - Déploiement des microservices sur le cloud en utilisant des outils tels que Terraform ou CloudFormation](#62---deploiement-des-microservices-sur-le-cloud-en-utilisant-des-outils-tels-que-Terraform-ou-CloudFormation)
  - [6.3 - Mise à l'échelle des microservices en fonction des besoins en utilisant les fonctionnalités de Kubernetes](#63---mise-a-l-echelle-des-microservices-en-fonction-des-besoins-en-utilisant-les-fonctionnalites-de-Kubernetes)
- [7 - Conclusion](#7---conclusion)
  - [7.1 - Résumé de la mise en place de l'application cloud native basée sur des microservices](#71---resume-de-la-mise-en-place-de-l-application-cloud-native-basee-sur-des-microservices)
  - [7.2 - Discussion sur les avantages et les limites de cette approche](#72---discussion-sur-les-avantages-et-les-limites-de-cette-approche)
  - [7.3 - Directions futures pour le développement de l'application](#73---directions-futures-pour-le-developpement-de-l-application)

  <br/>

# 1 - Introduction à la conception d'une application cloud native

## 1.1 - Présentation des microservices et leur rôle dans une application cloud native

Les microservices sont une architecture de développement logiciel qui permet de décomposer une application en petits modules indépendants qui peuvent être développés, testés et déployés de manière indépendante. Ce paradigme de développement est de plus en plus populaire pour les applications cloud native en raison de sa flexibilité et de sa capacité à gérer la complexité croissante des applications modernes.

Les microservices sont particulièrement importants pour les applications cloud native car ils permettent d'adopter une approche DevOps pour le développement, le test et le déploiement. Les équipes de développement peuvent travailler sur le développement d'un microservice indépendant sans perturber les autres microservices, ce qui permet une amélioration rapide de l'application. De plus, les microservices peuvent être déployés de manière dynamique et mise à l'échelle en fonction des besoins, ce qui permet d'optimiser les ressources et les coûts.

En utilisant les microservices, les équipes peuvent également utiliser différents outils et technologies pour chaque microservice en fonction de leurs besoins spécifiques, ce qui les aide à maximiser leur efficacité et leur qualité. Enfin, les microservices peuvent être facilement maintenus et mis à jour sans impacter l'ensemble de l'application, ce qui garantit la stabilité et la disponibilité de l'application à long terme.

## 1.2 - Objectifs de la mise en place de l'application cloud native

Les objectifs de la mise en place de l'application sont les suivants :

  - Extraire les données de différentes sources de manière efficace et en temps réel.
  - Stocker les données de manière sécurisée et scalable.
  - Transformer les données en un format utilisable pour les analyses.
  - Visualiser les données de manière claire et intuitive pour permettre une meilleure compréhension.
  - Automatiser les processus de collecte, de transformation et de visualisation des données pour une utilisation efficace.
  - Utiliser les principes DevOps pour améliorer la rapidité et la qualité du développement, du déploiement et de la maintenance de l'application.
  - Tirer pleinement parti des avantages offerts par le cloud pour garantir une disponibilité - élevée, une évolutivité et une rentabilité à long terme.


# 2 - Planification de des microservices

## 2.1 - Analyse de la fonctionnalité requise pour chaque microservice

Dans cette section, nous allons examiner les fonctionnalités requises pour chaque microservice de notre application de data engineering. Nous utiliserons une approche basée sur les microservices pour décomposer notre application en différents services indépendants qui peuvent être développés, déployés et exécutés de manière autonome.

``` Extraction des données ``` Ce microservice extrait les données de différentes sources et les stocke dans un format standardisé pour un traitement ultérieur.

``` Stockage des données ``` Ce microservice gère le stockage des données dans un stockage distribué, tel que Apache Cassandra ou Amazon S3, pour une accessibilité fiable et une scalabilité horizontale.

``` Transformation des données ``` Ce microservice se charge de transformer les données extraites en un format standard pour une analyse et une visualisation plus faciles.

``` Analyse des données ``` CCe microservice se charge de l'analyse des données, telles que les agrégations, les filtrages et les analyses statistiques.

``` Visualisation des données ``` Ce microservice se charge de générer des graphiques et des tableaux pour visualiser les données analysées.




