## Processus de visualisation entre data_visualization et frontend_app

Le processus entre le microservice Data_Visualization et le microservice Frontend_App peut se dérouler de la manière suivante :

- Le microservice Data_Visualization extrait les données stockées dans la base de données du microservice Data_Storage.

- Il analyse les données pour créer les visualisations souhaitées, telles que les graphiques en cercles et les graphiques à bandes.

- Une fois les visualisations créées, le microservice Data_Visualization les expose via une API REST pour que d'autres microservices puissent les consommer.

- Le microservice Frontend_App envoie une requête à l'API REST du microservice Data_Visualization pour obtenir les visualisations.

- Le microservice Data_Visualization renvoie les visualisations au microservice Frontend_App sous forme de données structurées (par exemple, en JSON).

- Le microservice Frontend_App utilise les visualisations reçues pour les afficher sur la page de visualisation en temps réel pour l'utilisateur.

En résumé, le microservice Data_Visualization extrait les données de la base de données, crée les visualisations, les expose via une API REST et les renvoie au microservice Frontend_App qui les affiche pour l'utilisateur. Les deux microservices communiquent entre eux en utilisant des API REST pour échanger les informations.



