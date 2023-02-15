**ReRoutes** : Décrit la façon dont les requêtes entrantes doivent être transmises à des services web spécifiques en fonction de leur URI (Uniform Resource Identifier) et de leur méthode HTTP. Pour chaque route, il y a plusieurs éléments configurables:

```DownstreamPathTemplate : ``` l'URI de la ressource cible sur le serveur backend

```DownstreamScheme : ``` le protocole utilisé pour communiquer avec le serveur backend. Dans ce cas, c'est HTTP

```DownstreamHostAndPorts : ```  les informations de l'hôte et du port du serveur backend auquel transmettre la requête

```UpstreamPathTemplate : ``` l'URI de la ressource sur le serveur API Gateway qui doit être utilisé pour acheminer la requête

```UpstreamHttpMethod : ```  les méthodes HTTP prises en charge par cette route. Dans ce cas, "Get" et "Post" sont autorisées pour la première route, "Post" seulement pour la seconde et la troisième route, et "Get" seulement pour la quatrième route.

```LoadBalancerOptions : ``` la stratégie de répartition de charge à utiliser. Dans ce cas, la répartition de charge peut être "RoundRobin" (tour par tour), "LeastConnection" (connexion la plus faible) ou "Random" (aléatoire) en fonction de la route

``` QoSOptions : ``` les options de qualité de service à utiliser, telles que les temps de réponse maximum et les tolérances d'erreur

``` SecurityOptions : ``` les options de sécurité à utiliser, telles que les portées autorisées et les clés d'authentification pour chaque route


**GlobalConfiguration** : Décrit les paramètres de configuration généraux pour l'API Gateway

``` BaseUrl : ``` l'URL de base utilisée pour construire les URL des ressources cibles

``` RequestIdKey : ``` le nom de l'en-tête HTTP à utiliser pour transmettre l'ID de requête

``` ServiceDiscoveryProvider : ``` le fournisseur de découverte de services utilisé pour découvrir les services backend. Dans ce cas, le fournisseur est Consul

``` RateLimitOptions : ``` les options de limitation de taux à utiliser pour chaque client

``` QoSOptions : ``` les options de qualité de service globales à utiliser pour toutes les routes