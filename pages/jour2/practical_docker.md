# Passage à la pratique !
### A. Manipuler Docker
<p></p>

1. Utiliser le "Get Started" de docker pour l'installer sur votre machine et lancer le container hello_world
3. Lancer une image de docker avec [la distribution Alpine](https://hub.docker.com/_/alpine) ou [Debian Slim](https://hub.docker.com/_/debian)
4. Accéder au shell dans le container docker et éteindre le container depuis l'intérieur
5. Rallumez le container. Transférez des fichiers entre votre machine et le container docker (qu'on appellera container-server)
6. Ajouter un serveur http qui écoute sur le port 80 et répond hello_world (language de votre choix, vous pouvez en récupérez des déjà écrits)
   1. Par exemple : python3 -m http.server 8080
7. Lancer ce serveur http dans le container
8. Accéder à l'url depuis votre navigateur web




### B. Construction d'image
<p></p>

1. Créer un dockerfile simple pour lancer un serveur http sur une image de base debian slim
2. Utiliser la commande docker build pour construire une image à partir de votre dockerfile
3. Lancer un container à partir de votre image


Vous pouvez vous inspirer du [tutoriel officiel ici](https://docs.docker.com/get-started/02_our_app/#build-the-apps-image)

### C. Docker-compose
<p></p>

1. Lancer un serveur http dans un premier container
1. Utilisez docker-compose pour ajouter un second container alpine (appelé container-client)
   1. Permettez la communication sur le port 80 entre les deux containers via la configuration du docker-compose
   2. Depuis container-client, installer un script qui fait 4 appels à une adresse précise (celle de container-server) sur le port 80
   3. Observez bien les appels entre les 2 containers dans les logs de container-server


### C. Bonus
<p></p>

1. Utilisez [kaniko](https://github.com/GoogleContainerTools/kaniko) pour build votre image de container avec un serveur http
2. Injecter une variable d'environnement pour lors de la phase de build pour indiquer le Port sur lequel le serveur tournera
3. Publier votre image sur le docker Hub
4. Utilisez un cloud provider (Heroku, Google Cloud, Azure, AWS, etc.) pour déployer votre application contenerisé en ligne. (Prenez une version d'essai / gratuite si vous voulez tester)
   