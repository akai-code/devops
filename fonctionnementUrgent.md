**api_gateway**: Ce microservice joue le rôle de passerelle pour les requêtes entrantes. Il s'assure que les requêtes sont redirigées vers les bons microservices pour traitement et renvoie les réponses appropriées aux utilisateurs. C'est l'interface utilisateur de l'application.

**data_storage**: Ce microservice est responsable du stockage des données collectées par le microservice tweet_collector. Il peut être implémenté avec un système de gestion de bases de données tels que MongoDB ou Cassandra pour stocker les tweets en temps réel.

**data_visualization**: Ce microservice se concentre sur la visualisation des données stockées dans data_storage. Il peut utiliser des technologies telles que D3.js pour créer les diagrammes en temps réel que vous souhaitez afficher dans votre interface utilisateur.

**sentiment_analyser**: Ce microservice est responsable de l'analyse des sentiments des tweets collectés. Il peut utiliser des algorithmes de machine learning pour analyser les tweets et déterminer leur polarité (positive, négative ou neutre).

**tweet_collector**: Ce microservice est responsable de la collecte des tweets en temps réel en utilisant l'API Twitter. Il peut filtrer les tweets en fonction des mots clés spécifiés par l'utilisateur pour les stocker dans data_storage.

Lorsque vous entrez quelque chose dans la barre de recherche, l'api_gateway redirigera la requête vers tweet_collector pour collecter les tweets correspondants. Le sentiment_analyser analysera les tweets pour déterminer leur polarité et les enregistrera dans data_storage. Finalement, les données seront visualisées dans l'interface utilisateur en utilisant data_visualization.