2 Jours de cours


- Jour 1 : 
  - Introduction aux réseaux
    - Qu'est ce que le modèle OSI et ses 7 couches 
    - Qu'est ce qu'une adresse IP v4 ?
    - Pourquoi des IP v6 ?
    - Qu'est ce qu'une addresse MAC ?
    - Comment fonctionne un DNS
  
  - Proposition : TP Virtual Box sur 3 VM ? 
  - Gros TP : 
    - Calcul de filtres, de sous réseaux, de plages d'IP, etc.
  - 13h30 : Introduction globale à docker : qu'est ce que ça fait (30mn max)
    - Pourquoi on utilise des systèmes de contenerisation?
    - Les méthodes de déploiement avant docker ? Comment on faisait avant ? (VM, Mainframe (IBM Z), virtualiseur (Hyperscale, Proxmox, OpenStack))
    - Qu'est ce qu'un container
    - Qu'est ce qu'une image
    - Qu'est ce qu'un dockerFile
  - Slide pour expliquer comment installer docker (hello world)
  - Préparation de mini-exposé (toute l'après-midi)



- Jour 2
  - passage de chaque groupe sur les différents sujets (10mn par groupe + 10mn de questions)  
    - Les exposés compteront pour 8 points de la note finale du cours.   
  - on compte toute la matinée pour les différents passages (~3h) même si cela peut-être plus court.
  - Après-midi : 
    - TP 13h30 -> 16h : Docker en pratique
      - Préparer un gros TP (s'inspirer de ce que j'avais demandé pendant Intro Linux)
      - Fonctionnalité avancée avec du docker-compose
      - Idée de Bonus : 
        - Utilisation d'un autre système de contenerisation (kaniko)
        - Déployer dans le cloud (lequel pour avoir un truc gratuit ?) votre container
        - Explication de comment fonctionne le routage (switch) et questions précises sur un cas d'exemple
    - 16h : QCM 1h (difficile) sur Docker
  
  




Sujets d'exposés : 
- Les stockages des images docker : les différentes façon de gérer ces artifacts (Nexus, version sur les clouds, etc.)
- Qu'est ce que le docker daemon ? (quels droits ? Docker in docker ? etc. )
- Tout savoir sur le docker hub (version, comment pousser des nouvelles images, les tags, etc.)
- Gérer des paramètres d'environnement avec docker : arg variables et env variables
- Le processus de build à partir d'un docker File et la construction par couche
- Faire fonctionner plusieurs containers ensemble à l'aide de docker-compose
- Les volumes de Docker : partager du contenu entre le container et le système
- La gestion des réseaux avec Docker
- Accéder à un container en production : Visualiser l'état du container, les logs, ouvrir un terminal, etc.



TODO : 
Jour 1 : 
[x] Faire les slides pour addresses IP : V4 et V6
[x] Faire les slides pour addresses MAC
[x] Faire les slides pour DNS
[x] Faire le TP jour 1 sur le réseau
[x] Faire les slides pour les 30mn d'intro à docker


Jour 2 : 
[x] Lister les différens sujet d'exposé : 7 sujets maximum
[ ] Me renseigner sur les différents sujets d'exposé
[ ] Sur chaque sujet, avoir un mini descriptif de questions, de buzzwords à creuser, etc.
[ ] Me faire un petit excel rapide pour noter sur 8 les exposés (4 critères sur 2 points chacun)
  - Communication
  - Clarté des recherches et informations
  - Qualité techniques
  - Profondeur technique




Bonus : 

- Fonctionnement d'un NAT