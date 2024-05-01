# Et docker, à quoi ça sert ?
<div>
<img
  v-click
  class="w-30 border-rounded rounded-4"
  src="assets/docker.png"
  alt=""
/>
</div>
<p v-click class="opacity-90 border-1 border-separate p2">
Docker est une plateforme Open-Source qui permet d'automatiser le déploiement, la mise en échelle et la gestion d'application. <span class="font-bold"> Via la contenerisation</span></p>

<p v-click class="opacity-90 border-1 border-separate p2">
Le projet a été lancé en France (Autour de ~2013), à Télécom Paris Tech.</p>

<div>
<img
  v-click
  class="border-rounded rounded-4"
  src="assets/docker-stats.png"
  alt=""
/>
</div>

---
transition: fade-out
hideInToc: true
---

# Les méthodes de déploiements avant Docker
<p></p>
<p v-click class="opacity-90 border-1 border-separate p2">
Avant, on utilisait des serveurs physiques : 1 serveur = 1 application.
</p>

<p v-click class="opacity-90 border-1 border-separate p2">
Pour augmenter les capacités, on utilisait du "scaling vertical" : Mainframe (IBM Z) pour une application bancaire
</p>

<p v-click class="opacity-90 border-1 border-separate p2">
Ensuite, on a voulu mutualiser via les hyperviseurs et les machines virtuelles : Hyperscale, Proxmox, OpenStack
</p>

<div v-click>
Désormais, Docker facilite : 

- l'isolation des applications
- la portabilité
- le déploiement en continu

</div>

<!--
Ex: appli d'une banque : 1 seul server mainframe. avec plus d'1 Tera de RAM

Hypervisuers : On met un ordinateur entier (virtualBox par ex) dans un autre ordinateur

Combien de VM virtual Box vous pouvez avoir sur votre ordi en même temps ? 

on peut avoir 50 containers dockers qui tournent sans soucis.

-->

---
transition: fade-out
hideInToc: true
---

# Qu'est ce qu'un container
<p></p>

<p v-click class="opacity-90 border-1 border-separate p2">
De façon déclarative, couche par couche, on définit ce dont on a besoin pour faire tourner notre application</p>
<p v-click class="opacity-90 border-1 border-separate p2">
On parle de <span class="font-italic">Dockerisation d'une application</span></p>

<p v-click class="opacity-90 border-1 border-separate p2">
Ensuite on lance autant de container de notre application, sur les machines que l'on veut.</p>

<div>
<img
  v-click
  class="h-50 border-rounded rounded-4"
  src="assets/docker_container.png"
  alt=""
/>
</div>
<!--
On va dockeriser une application, pour la faire tourner sur quelque chose d'isolé et de réduit à sa portion congrue
-->

---
transition: fade-out
hideInToc: true
---

# Qu'est ce qu'une image
<p></p>

<p v-click class="opacity-90 border-1 border-separate p2 text-sm">
Une image Docker, ou image de conteneur, est un fichier exécutable autonome utilisé pour créer un conteneur. Cette image de conteneur contient toutes les bibliothèques, dépendances et fichiers dont le conteneur a besoin pour s'exécuter.</p>



<p v-click class="opacity-90 border-1 border-separate p2 text-sm">
On construit une image docker couche par couche</p>

<div v-click>
On peut définir les couches de la façon suivante : 

- Base Image
- Parent Image
- Layers
- Container Layers
- Docker Manifest
  
</div>

<!--
A partir d'une image, on va pouvoir contruire un container. Imaginez-vous, mettre sur une clé-usb votre ordinateur. 

La clé usb est l'image, et lorsque vous voulez démarrer votre ordinateur pour faire des tâches, on considère qu'on va a démarrer un container basé sur cette image. 

On peut démarrer plusieurs containers à partir d'une image, on peut partager une image pour pouvoir démarrer un container avec la même application sur pleins de serveurs. 

Si l'image est bien configuré, on a besoin de rien d'autre pour pouvoir démarrer l'application. 

Imaginons par exemple le code du site du CNRS. Vous avez ce code dans une image, et vous pouvez la distribuer sur plusieurs serveurs. Chacun peut alors lancer exactement la même application, dans la même version :) 
-->

---
transition: fade-out
hideInToc: true
---

# Un Dockerfile pour décrire une image

<p class="opacity-90 border-1 border-separate p2">
Le dockerfile va vous permettre de <span class="font-bold"> build </span> une image à partir d'instructions. 
</p>



````md magic-move
```dockerfile {*}
# Comment
INSTRUCTION arguments
```

```dockerfile {*}
FROM ubuntu:22.04

CMD ["ls", "/var/log"]
```

```dockerfile {*|1|3-5|7-8|10-13|*}
FROM ubuntu:22.04

# install app dependencies
RUN apt-get update && apt-get install -y python3 python3-pip
RUN pip install flask==3.0.*

# install app
COPY hello.py /

# final configuration
ENV FLASK_APP=hello
EXPOSE 8000
CMD ["flask", "run", "--host", "0.0.0.0", "--port", "8000"]
```
````

<!--
On va dockeriser une application, pour la faire tourner sur quelque chose d'isolé et de réduit à sa portion congrue
-->