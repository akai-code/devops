root
|
|-- microservices
|    |
|    |-- tweet_collector (Collecteur de tweets)
|    |   |-- app
|    |   |   |-- main.py (Code principal)
|    |   |   |-- utils.py (Fonctions utilitaires)
|    |   |
|    |   |-- tests (Dossier pour les tests unitaires)
|    |   |   |-- test_main.py
|    |   |
|    |   |-- Dockerfile (Fichier de configuration Docker)
|    |   |-- k8s (Dossier pour la configuration Kubernetes)
|    |   |   |-- deployment.yml
|    |   |   |-- service.yml
|    |   |
|    |   |-- requirements.txt (Dépendances Python)
|    |
|    |-- sentiment_analyzer (Analyseur de sentiments)
|    |   |-- app
|    |   |   |-- main.py (Code principal)
|    |   |   |-- utils.py (Fonctions utilitaires)
|    |   |
|    |   |-- tests (Dossier pour les tests unitaires)
|    |   |   |-- test_main.py
|    |   |
|    |   |-- Dockerfile (Fichier de configuration Docker)
|    |   |-- k8s (Dossier pour la configuration Kubernetes)
|    |   |   |-- deployment.yml
|    |   |   |-- service.yml
|    |   |
|    |   |-- requirements.txt (Dépendances Python)
|    |
|    |-- data_storage (Stockage des données)
|    |   |-- app
|    |   |   |-- main.py (Code principal)
|    |   |   |-- utils.py (Fonctions utilitaires)
|    |   |
|    |   |-- tests (Dossier pour les tests unitaires)
|    |   |   |-- test_main.py
|    |   |
|    |   |-- Dockerfile (Fichier de configuration Docker)
|    |   |-- k8s (Dossier pour la configuration Kubernetes)
|    |   |   |-- deployment.yml
|    |   |   |-- service.yml
|    |   |   |-- persistent_volume.yml
|    |   |   |-- persistent_volume_claim.yml
|    |   |
|    |   |-- requirements.txt (Dépendances Python)
|    |
|    |-- data_visualization (Visualisation des données)
|    |   |-- app
|    |   |   |-- main.py (Code principal)
|    |   |   |-- utils.py (Fonctions utilitaires)
|    |   |
|    |   |-- tests (Dossier pour les tests unitaires)
|    |   |   |-- test_main.py
|    |   |
|    |   |-- Dockerfile (Fichier de configuration Docker)
|    |   |-- k8s (Dossier pour la configuration Kubernetes)
|    |   |   |-- deployment.yml
|    |   |   |-- service.yml
|    |   |
|    |   |-- requirements.txt (Dépendances Python)
|    |
|    |-- api_gateway (Passerelle API)
|    |   |-- app
|    |   |   |-- main.py (Code principal)
|    |   |   |-- utils.py (Fonctions utilitaires)
|    |   |
|    |   |-- tests (Dossier pour les tests unitaires)
|    |   |   |-- test_main.py
|    |   |
|    |   |-- Dockerfile (Fichier de configuration Docker)
|    |   |-- k8s (Dossier pour la configuration Kubernetes)
|    |   |   |-- deployment.yml
|    |   |   |-- service.yml
|    |   |
|    |   |-- requirements.txt (Dépendances Python)
|    |
|-- monitoring (Monitoring)
|    |-- prometheus
|    |   |-- prometheus.yml (Fichier de configuration Prometheus)
|    |
|    |-- grafana
|    |   |-- datasources.yml (Configurations de sources de données)
|    |   |-- dashboards.yml (Configurations de tableaux de bord)
|    |
|    |-- alerting (Alerting)
|    |   |-- alertmanager.yml (Fichier de configuration Alertmanager)
|    |
|-- deployment (Déploiement)
|    |-- kustomization.yml (Fichier de personnalisation Kubernetes)
|
|-- .gitignore (Fichier de configuration Git)
|-- README.md (Fichier README)
|-- Architecture.md (Fichier d'architecture)

