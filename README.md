# Table of contents 


- [1 - Introduction à la conception d'une application cloud native](#1---introduction-a-la-conception-d-une-application-cloud-native)
  - [1.1 - Présentation des microservices et leur rôle dans une application cloud native](#11---presentation-des-microservices-et-leur-role-dans-une-application-cloud-native)
  - [1.2 - Objectifs de la mise en place de l'application](#12---objectifs-de-la-mise-en-place-de-l-application)
- [2 - Planification des microservices](#2---planification-des-microservices)
  - [2.1 - Analyse de la fonctionnalité requise pour chaque microservice](#21---analyse-de-la-fonctionnalite-requise-pour-chaque-microservice)
  - [2.2 - Détermination des dépendances entre les microservices](#22---determination-des-dependances-entre-les-microservices)
    - [2.2.1 - Diagramme de flux de travail pour l'extraction des données](#221---diagramme-de-flux-de-travail-pour-lextraction-des-donnees)
    - [2.2.2 - Diagramme de flux de travail pour le stockage des données](#222---diagramme-de-flux-de-travail-pour-le-stockage-des-donnees)
    - [2.2.3 - Diagramme de flux de travail pour la transformation des données](#223---diagramme-de-flux-de-travail-pour-la-transformation-des-donnees)
    - [2.2.4 - Diagramme de flux de travail pour l'analyse des données](#224---diagramme-de-flux-de-travail-pour-l-analyse-des-donnees)
    - [2.2.5 - Diagramme de flux de travail pour la visualisation des données](#225---diagramme-de-flux-de-travail-pour-la-visualisation-des-donnees)
- [3 - Développement des microservices](#3---developpement-des-microservices)
  - [3.1 - Développement du microservice d'extraction des données](#31---developpement-du-microservice-d-extraction-des-donnees)
    - [3.1.1 - Définition des exigences](#311---definition-des-exigences)
    - [3.1.2 - Définition des technologies](#312---definition-des-technologies)
    - [3.1.3 - Développement du microservice](#313---developpement-du-microservice)
  - [3.2 - Développement du microservice de stockage des données](#32---developpement-du-microservice-de-stockage-des-donnees)
    - [3.2.1 - Définition des exigences](#321---definition-des-exigences)
    - [3.2.2 - Définition des technologies](#322---definition-des-technologies)
    - [3.2.3 - Développement du microservice](#323---developpement-du-microservice)
  - [3.3 - Développement du microservice de transformation des données](#33---developpement-du-microservice-de-transformation-des-donnees)
    - [3.3.1 - Définition des exigences](#331---definition-des-exigences)
    - [3.3.2 - Définition des technologies](#332---definition-des-technologies)
    - [3.3.3 - Développement du microservice](#333---developpement-du-microservice)
  - [3.4 - Développement du microservice d'analyse des données](#34---developpement-du-microservice-d-analyse-des-donnees)
    - [3.4.1 - Définition des exigences](#341---definition-des-exigences)
    - [3.4.2 - Définition des technologies](#342---definition-des-technologies)
    - [3.4.3 - Développement du microservice](#343---developpement-du-microservice)
  - [3.5 - Développement du microservice de visualisation des données](#35---developpement-du-microservice-de-visualisation-des-donnees)
    - [3.5.1 - Définition des exigences](#351---definition-des-exigences)
    - [3.5.2 - Définition des technologies](#352---definition-des-technologies)
    - [3.5.3 - Développement du microservice](#353---developpement-du-microservice)
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

## 1.2 - Objectifs de la mise en place de l'application

Les objectifs de la mise en place de l'application sont les suivants :

  - Extraire les données de différentes sources de manière efficace et en temps réel.
  - Stocker les données de manière sécurisée et scalable.
  - Transformer les données en un format utilisable pour les analyses.
  - Visualiser les données de manière claire et intuitive pour permettre une meilleure compréhension.
  - Automatiser les processus de collecte, de transformation et de visualisation des données pour une utilisation efficace.
  - Utiliser les principes DevOps pour améliorer la rapidité et la qualité du développement, du déploiement et de la maintenance de l'application.
  - Tirer pleinement parti des avantages offerts par le cloud pour garantir une disponibilité - élevée, une évolutivité et une rentabilité à long terme.


# 2 - Planification des microservices

## 2.1 - Analyse de la fonctionnalité requise pour chaque microservice

Dans cette section, nous allons examiner les fonctionnalités requises pour chaque microservice de notre application de data engineering. Nous utiliserons une approche basée sur les microservices pour décomposer notre application en différents services indépendants qui peuvent être développés, déployés et exécutés de manière autonome.

``` Extraction des données ``` Ce microservice extrait les données de différentes sources et les stocke dans un format standardisé pour un traitement ultérieur.

``` Stockage des données ``` Ce microservice gère le stockage des données dans un stockage distribué, tel que Apache Cassandra ou Amazon S3, pour une accessibilité fiable et une scalabilité horizontale.

``` Transformation des données ``` Ce microservice se charge de transformer les données extraites en un format standard pour une analyse et une visualisation plus faciles.

``` Analyse des données ``` CCe microservice se charge de l'analyse des données, telles que les agrégations, les filtrages et les analyses statistiques.

``` Visualisation des données ``` Ce microservice se charge de générer des graphiques et des tableaux pour visualiser les données analysées.

## 2.2 - Détermination des dépendances entre les microservices

Dans cette section, nous allons déterminer les dépendances entre les différents microservices de notre application. Cela nous permettra de comprendre comment les microservices interagissent les uns avec les autres et comment les modifications apportées à l'un d'entre eux peuvent affecter le fonctionnement de l'application dans son ensemble.

Pour ce faire, nous utiliserons des diagrammes de flux de travail pour représenter les relations entre les microservices, ainsi que les entrées et les sorties pour chaque service. Nous analyserons également les dépendances en termes de données, en déterminant les points de partage de données entre les microservices et en les documentant.

Cette analyse des dépendances nous permettra de mieux comprendre comment les microservices interagissent les uns avec les autres et comment ils peuvent être modifiés ou mis à jour sans affecter le fonctionnement de l'application dans son ensemble. Elle nous aidera également à déterminer les besoins en matière de test et de validation pour chaque microservice, ce qui est crucial pour assurer la qualité et la fiabilité de l'application dans le temps.

### 2.2.1 - Diagramme de flux de travail pour l'extraction des données

Le diagramme de flux de travail suivant représente le flux de données pour l'extraction des données. Il montre les différentes étapes de l'extraction des données et les différents microservices qui interagissent avec les données.

[Image: image]

image.png1920×1080 201 KB

### 2.2.2 - Diagramme de flux de travail pour le stockage des données

Le diagramme de flux de travail suivant représente le flux de données pour le stockage des données. Il montre les différentes étapes de stockage des données et les différents microservices qui interagissent avec les données.

[Image: image]

image.png1920×1080 201 KB

### 2.2.3 - Diagramme de flux de travail pour la transformation des données

Le diagramme de flux de travail suivant représente le flux de données pour la transformation des données. Il montre les différentes étapes de transformation des données et les différents microservices qui interagissent avec les données.

[Image: image]

image.png1920×1080 201 KB

### 2.2.4 - Diagramme de flux de travail pour l'analyse des données

Le diagramme de flux de travail suivant représente le flux de données pour l'analyse des données. Il montre les différentes étapes d'analyse des données et les différents microservices qui interagissent avec les données.

[Image: image]

image.png1920×1080 201 KB

### 2.2.5 - Diagramme de flux de travail pour la visualisation des données

Le diagramme de flux de travail suivant représente le flux de données pour la visualisation des données. Il montre les différentes étapes de visualisation des données et les différents microservices qui interagissent avec les données.

[Image: image]

image.png1920×1080 201 KB


# 3 - Développement de des microservices

## 3.1 - Développement du microservice d'extraction des données

Dans cette section, nous allons développer le microservice d'extraction des données. Ce microservice se charge de l'extraction des données de différentes sources et de leur stockage dans un format standardisé pour un traitement ultérieur.

### 3.1.1 - Définition des exigences

### 3.1.2 - Définition des technologies

### 3.1.3 - Développement du microservice

## 3.2 - Développement du microservice de stockage des données

Dans cette section, nous allons développer le microservice de stockage des données. Ce microservice se charge du stockage des données dans un stockage distribué, tel qu'Apache Cassandra ou Amazon S3, pour une accessibilité fiable et une scalabilité horizontale.

### 3.2.1 - Définition des exigences

### 3.2.2 - Définition des technologies

### 3.2.3 - Développement du microservice

## 3.3 - Développement du microservice de transformation des données

Dans cette section, nous allons développer le microservice de transformation des données. Ce microservice se charge de transformer les données extraites en un format standard pour une analyse et une visualisation plus faciles.

### 3.3.1 - Définition des exigences

### 3.3.2 - Définition des technologies

### 3.3.3 - Développement du microservice

## 3.4 - Développement du microservice d'analyse des données

Dans cette section, nous allons développer le microservice d'analyse des données. Ce microservice se charge d'analyser les données extraites et transformées pour en extraire des informations utiles.

### 3.4.1 - Définition des exigences

### 3.4.2 - Définition des technologies

### 3.4.3 - Développement du microservice

## 3.5 - Développement du microservice de visualisation des données

Dans cette section, nous allons développer le microservice de visualisation des données. Ce microservice se charge de visualiser les données extraites, transformées et analysées pour en extraire des informations utiles.

### 3.5.1 - Définition des exigences

### 3.5.2 - Définition des technologies

### 3.5.3 - Développement du microservice


# 4 - Orchestration avec Kubernetes

## 4.1 - Présentation de Kubernetes et ses fonctionnalités

## 4.2 - Configuration des objets Kubernetes pour gérer les microservices

## 4.3 - Mise en place de la mise à l'échelle et de la fiabilité en utilisant les fonctionnalités de Kubernetes


# 5 - Surveillance et tests

## 5.1 - Mise en place de l'outil de surveillance pour surveiller les microservices

## 5.2 - Écriture de tests pour vérifier la qualité et la disponibilité des microservices

## 5.3 - Configuration de l'outil de test pour s'exécuter automatiquement en cas de modification du code


# 6 - Déploiement et mise à l'échelle

## 6.1 - Préparation du déploiement dans le cloud

## 6.2 - Déploiement des microservices sur le cloud en utilisant des outils tels que Terraform ou CloudFormation

## 6.3 - Mise à l'échelle des microservices en fonction des besoins en utilisant les fonctionnalités de Kubernetes


# 7 - Conclusion

## 7.1 - Résumé de la mise en place de l'application cloud native basée sur des microservices

## 7.2 - Discussion sur les avantages et les limites de cette approche

## 7.3 - Discussion sur les prochaines étapes pour améliorer l'application



































