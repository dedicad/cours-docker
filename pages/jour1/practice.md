# Passage à la pratique !
### A. Les masques de réseau
<p></p>
<p class="opacity-90 border-1 border-separate p2">Dans l'ensemble des sessions pratiques, les commandes "man" et "tldr" sont vos amies !</p>

1. Citez 3 exemples de masques de sous-réseau
2. Soit l'adresse 192.16.5.133/29. Combien de bits sont utilisés pour identifier la partie réseau ? Combien de bits sont utilisés pour identifier la partie hôte ?
3. Quelle est l'adresse du réseau auquel appartient l'IP 210.205.52.24/12 
4. Quelle est l'adresse du réseau auquel appartient l'IP 210.205.52.24/8 
5. Quelle est l'adresse du réseau auquel appartient l'IP 210.160.12.4/16 

---
transition: fade-out
hideInToc: true
---

### B. La taille des réseaux
<br/>

1. L'adresse IP 172.18.2.5 est-elle publique ?
2. Combien peut-on stocker d'adresses dans le réseau 172.16.0.0/12 ? 
3. Et dans le réseau 205.88.12.16/32 ? Et dans le réseau 205.88.12.16/4 ?
4. On attribue le réseau 132.45.0.0/16. Il faut redécouper ce réseaux en 8 sous-réseaux.
   1. Quel est le masque réseau qui permet la création de huit sous-réseaux ?
   2. Quelle est l'adresse réseau de chacun des huit sous-réseaux ainsi définis ?
   3. Quelle est la plage des adresses utilisables du sous-réseau numéro 3 ?

Une source utile : https://www.it-connect.fr/adresses-ipv4-et-le-calcul-des-masques-de-sous-reseaux/

---
transition: fade-out
hideInToc: true
---

### C. Mieux manipuler les réseaux
<br/>


1. Que renvoie la commande "sipcalc 192.168.1.0/24" à lancer dans le terminal ?
2. Pouvez vous obtenir depuis votre terminal l'adresse IP du DNS de coda.school ? (nslookup or dig)
3. Pouvez vous obtenir votre addresse IP privée ?
4. Quelle est votre adresse IP Privée ?
5. Combien de blocs faudrait-il pour écrire en base 10 une adresse IPv6 (comme on le fait avec les IPv4) ?
6. En base 16, comme c'est la convention (avec notation hexadécimale), combien en faut-il ?

---
transition: fade-out
hideInToc: true
---

### D. Bonus Réseau 1
<br/>

1. Affichez l'ensemble des interfaces réseaux disponibles
2. Désactiver l'une de vos interface réseau
3. Ré-activer l'interface
4. Afficher l'ensemble des ports réseaux en fonctionnement (avec netstat) 
5. Pouvez vous filtrer pour n'afficher que les ports TCP ?
6. Installer un firewall avec ufw


---
transition: fade-out
hideInToc: true
---

### E. Annuaire ARP
<br/>


1. Utilisez [l'éditeur live de Mermaid](https://mermaid-js.github.io/mermaid-live-editor/edit#pako:eNptkd1Kw0AQhV9lnCuFpmS3RXSQlNqCVGhN9U5ysyYTu9Bk6_4IUvouvosv5qalVNG9mj18czgzs8XSVIyEjt8CtyVPtXq1qilaiG9hPIN5Zwv5RPTyiSSY6roOTpsWzm-tUVWpnL840JFJkmxPLYMGBQWKa9kXl1f9tC8LhNHNi82m2rNL1gxfn78AUeDRRiZZtBEE9wwuaNdJXessJ_jh2Enz8YQgTUkIkpIGAxoOKZX_pCeYa8fALZSqXDGMH_NT6uyQOp8t7mD0J0X-EOUz7GHDtlG6itvadlCBfsUNF0ixrLhWYe27IXYRVcGbp4-2RPI2cA_DplL-uFykWq1dVDeqfTbm9OdKe2Pnh4vsD7P7Bh3decA) pour expliquer les requêtes ARP dans le cas de 3 ordinateur dans la configuration suivante : 
   1. PC1 et PC2 partagent le même réseau A
   2. PC2 et PC3 partagent le même réseau B
   3. PC2 est donc présent sur les 2 réseaux
   4. PC1 cherche à joindre l'adresse IP de PC3 mais ne peut pas communiquer directement avec lui lors du Broadcast
5. Bonus : A quoi ressemble la table ARP du PC2 après les échanges

---
transition: fade-out
hideInToc: true
---

### F. Annuaire DNS
<br/>

1. Qu'est ce que le DNS menteur ? Comment cela fonctionne-t-il ?
2. Quelle est l'adresse IP du serveur DNS de Google ?
3. Que se passe-t-il lorsqu'un serveur DNS n'est plus fonctionnel ?
   

---
transition: fade-out
hideInToc: true
---

### G. Bonus Réseau 2
<br/>

1. Montez votre propre serveur DNS en local avec Dnsmasq. Voici un [lien pour aider](https://www.howtogeek.com/devops/how-to-run-your-own-dns-server-on-your-local-network/)