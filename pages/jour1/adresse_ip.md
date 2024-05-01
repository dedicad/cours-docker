# Qu'est ce qu'une addresse IP ?
### IP v4

<p v-click class="opacity-90 border-1 border-separate p2">Une adresse IP (Internet Protocol) est un numéro d'identification unique attribué de façon permanente ou provisoire à chaque périphérique faisant partie d'un même réseau informatique utilisant l'Internet Protocol</p>

<br/>

<div class="flex flex-row justify-between">
<div>
<img
  v-click
  class="w-60 border-rounded rounded-4"
  src="assets/Adresse_Ipv4.png"
  alt=""
/>
</div>

<div v-click>
<p class="text-xl font-bold">255.255.255.255</p>
<p>Adresse dite de Broadcast</p>
</div>

<div v-click>
<p class="text-xl font-bold">127.0.0.0</p>
<p>Localhost</p>
</div>

<div v-click>
<p class="text-xl font-bold"></p>
<p></p>
</div>

</div>


<br/>
<br/>
<br/>
<a href="https://www.paessler.com/fr/it-explained/ip-address">
Pour aller plus Loin
</a>


<br/>
<!-- Donc quelle est la plus grande addresse IP possible ?

-->
---
transition: fade-out
hideInToc: true
---

## IP Privée ou Publique

<div>
<p>Certains plages d'IP sont, par convention, dites "privées" ou "internes".</p>

</div>
</br>

<div class="flex flex-row justify-around">

<div v-click class="border-3 rounded-1 px-5 border-black">
<p class="font-bold">Bloc Privé 1</p>
<p class="text-xl">10.0.0.0/8</p>
</div>

<div v-after class="border-3 rounded-1 px-5 border-black">
<p class="font-bold">Bloc Privé 2</p>
<p class="text-xl">172.16.0.0/12</p>
</div>

<div v-after class="border-3 rounded-1 px-5 border-black">
<p class="font-bold">Bloc Privé 3</p>
<p class="text-xl">192.168.0.0/16</p>
</div>
</div>
</br>
</br>

<div v-click>

## Masques de sous-réseau
</div>

<p v-click class="opacity-90 border-1 border-separate p2">Une seule et même adresse IP identifie à la fois le réseau et une interface unique sur celui-ci</p>
<div v-after>
 Le masque de sous-réseau, détermine l’endroit auquel la partie d’une adresse correspondant au réseau se termine, et donc l’endroit où la portion correspond à l’hôte commence.
 </div>

<div class="flex flex-row justify-between">

<div v-click>
<p class="font-bold">Adresse IP</p>
<p class="text-xl">192.168.1.1/24</p>
</div>
<div v-click>
<p class="font-bold">Adresse de l'hôte</p>
<p class="text-xl">192.168.1.1</p>
</div>

<div v-click>
<p class="font-bold">Masque de réseau</p>
<p class="text-xl">11111111 11111111 11111111 00000000</p>
<p class="text-xl">255. &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 255. &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 255.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0</p>
</div>
  

<div v-click>
<p class="font-bold">Adresse du réseau</p>
<p class="text-xl">192. 168. 1. 0</p>
</div>
  
  
</div>




<!-- Exemple dans l'adresse suivante, on indique à la fois le réseau, mais également l'hôte concerné. Cela permet de router vers le bon réseau, puis vers le bon hôte.-->


---
transition: fade-out
hideInToc: true
---
# Calcul de l'adresse du réseau
<div class="flex flex-row justify-around">

<div v-click>
<p class="font-bold">Adresse IP</p>
<p class="text-xl">192.168.1.1/24</p>
</div>

<div v-after>
<p class="font-bold">Masque de réseau</p>
<p class="text-xl">255. 255. 255. 0</p>
</div>

</div>
</br>
</br>

<div v-click>
<img
  class="border-rounded rounded-4"
  src="assets/reseau-adresse-ipv4-calcul-masque-sous-reseau.png"
  alt=""
/>
</div>

<div class="flex flex-row justify-around" >
<div v-click class=" border-black border-3 p-3 m-3">
<p class="font-bold">Adresse du réseau</p>
<p class="text-xl">192. 168. 1. 0</p>
</div>
</div>

---
transition: fade-out
hideInToc: true
---

# Pourquoi des IP v6 ?
<p class="opacity-90 border-1 border-separate p2 text-black">Une adresse IP comporte 32 bits, ce qui permet de créer jusqu'à 4 milliards de numéros.

4 294 967 296 = $2^{32}$</p>


**Les amélioration d'IPv6 :**
- Routage plus efficace sans fragmentation des paquets
- Qualité de service (QoS) intégrée qui identifie les paquets prioritaires
- Sécurité de couche réseau intégrée (IPsec)
- Structure d'en-tête améliorée et réduction du coût de traitement

</br>

Pour aller plus Loin :
<div>

- [Epuisement des adresses IPv4](https://fr.wikipedia.org/wiki/%C3%89puisement_des_adresses_IPv4)
- [Différence entre IPv4 et IPv6 (Juniper)](https://www.juniper.net/fr/fr/research-topics/what-is-ipv4-vs-ipv6.html)
</div>

<!--
Combien d'humains sur Terre ? 
Concept de NAT, double NAT, triple NAT-->

---
transition: fade-out
hideInToc: true
---
# IPv4 vs IPv6
<p class="opacity-90 border-1 border-separate p2 text-black">
La taille des adresses passe de 32 bits en IPv4 à 128 bits en IPv6.
</p>



<div v-click>
<img
  class="h-60 border-rounded rounded-4"
  src="assets/ipv4-vs-ipv6-1.avif"
  alt=""
/>
</div>

<div class="flex flex-row justify-between">
<div v-click>
<p class="font-bold">Adresse IP v4</p>
<p class="text-xl">192.168.1.1/24</p>
</div>

<div v-click>
<p class="font-bold">Adresse IP v6</p>
<p class="text-xl">2DAB:FFFF:0000:3EAE:01AA:00FF:DD72:2C4A</p>
</div>

</div>

<!--
en IPv6 soit on compte en binaire. Soit on utilise la base 16 et donc l'hexadécimal pour permettre l'écriture.
Tout ce qui compte, c'est la valeur binaire. 

Mais si on écrivait en binaire, combien de blocs faudrait-il ?
-->

---
transition: fade-out
hideInToc: true
---

# Le protocole ARP
### Comment faire le lien entre une adresse IP (=adresse Internet) et une adresse physique (=mac)


<p v-click class="opacity-90 border-1 border-separate p2">Address Resolution Protocol : Le protocole ARP peut être vu comme la mise en annuaire des correspondances MAC/IP</p>

<div v-click>
<img
  class="h-10 border-rounded rounded-4"
  src="assets/arp.png"
  alt=""
/>
</div>


</br>

<div class="text-xs">

**Fonctionnement :** 

<ul>
  <li> Le routeur reçoit une trame provenant d’un équipement connecté à un des réseaux auquel il est lui-même rattaché.</li>
  <li> Les datagrammes sont transmis à la couche IP.</li>
  <li> Le routeur vérifie l’entête du datagramme.</li>
  <li> Si l’adresse IP fait partie des réseaux connus auquel le routeur est rattaché, l’information peut être envoyée à la couche APPLICATION, après que l’entête ait été désencapsulée. Dans le cas contraire, le routeur consulte sa table de routage, à la recherche d’un chemin à emprunter pour délivrer l’information.</li>
  <li> Le datagramme est ensuite envoyé via la carte réseau reliée au réseau sur lequel le routeur a décidé de l’envoyer.</li>
</ul>
</div>

</br>



---
transition: fade-out
hideInToc: true
---

# Table de routage et requête ARP

<p v-click class="opacity-90 border-1 border-separate p2">
La table de routage est une table de correspondance entre l’adresse de la machine destinatrice et le nœud suivant auquel le routeur doit délivrer le message.
</p>

<div class="mb-10" v-click>
<img
  class="w-100 border-rounded rounded-4"
  src="assets/arp-table.png"
  alt=""
/>
</div>
</br>

<a  href="https://www.it-connect.fr/chapitres/a-la-decouverte-de-ladresse-ethernet-et-darp/">
Pour aller plus Loin
</a>

---
transition: fade-out
hideInToc: true
---

# Exemple de requête ARP 

```mermaid {scale: 0.7, alt: 'An ARP Request'}
sequenceDiagram
    Note over PC1,PC2: Diffusion (Broadcast)
    PC1-->PC2: Qui a "192.168.0.2" ?<br>Dites-le à "192.168.0.1"
    PC2->>PC1: Je suis PC2<br>IP: 192.168.0.2<br>MAC: 00:11:22:33:44:02
    Note over PC1: Mise en cache ARP
    PC1->>PC2: PING ?
    PC2->>PC1: PONG !
```

<a  href="https://cours.rihan.fr/docs/reseau/protocole-arp/">
Source
</a>

<!--
Vous verrez en TP ensuite en détails, comment ça fonctionne, notamment quand on ne sait pas ou envoyer où envoyer un paquet.
-->

