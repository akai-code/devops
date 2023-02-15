# Microservices

- [1 - api-gateway](#1---api-gateway)
- [2 - data_storage](#2---data_storage)
- [3 - data_visualization](#3---data_visualization)
- [4 - frontend](#4---frontend)
- [5 - sentiment_analyzer](#5---sentiment_analyzer)
- [6 - tweet_collector](#6---tweet_collector)
- [7 - rabbitmq](#7---rabbitmq)

## 1 - api-gateway

### 1.1 - Qu'est-ce qu'un api-gateway ?

Un api-gateway est un point d'entrée unique pour les clients. Il permet de centraliser les appels vers les microservices.
C'est aussi un composant critique de l'architecture cloud native, car il permet de fournir une interface utilisateur cohérente tout en gérant la complexité de l'infrastructure sous-jacente. Il permet également de gérer les problèmes de sécurité, de performance et de scalabilité.

### 1.2 - Technologies utilisées

- [Ocelot](https://ocelot.readthedocs.io/en/latest/introduction/gettingstarted.html)

### 1.3 - Implémentation

D'abord j'ai installé Node.js et npm sur mon ordinateur. Ensuite j'ai créé un nouveau projet Node.js avec la commande suivante:

```npm init -y```

Ensuite j'ai installé Ocelot avec la commande suivante:

```npm install ocelot ```

Apres j'ai créé un fichier de configuration ocelot.json avec la commande suivante:

```touch ocelot.json```

Ce fichier contient la configuration de l'api-gateway. Il contient les informations suivantes:

- Les routes vers les microservices
- Les informations de sécurité
- Les informations de performance
- Les informations de scalabilité


