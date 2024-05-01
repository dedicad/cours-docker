# Gérer son domaine avec un DNS

<p v-click class="opacity-90 border-1 border-separate p2">Le DNS (Domain Name System) est un service distribué qui associe un nom de domaine à une adresse IP</p>


<div class="flex flex-row justify-around">
<div v-after>
```mermaid {theme: 'neutral', scale: 0.5}
graph TD
A[Ordinateur] -- coda.school --> B[Requête DNS]
B --> C[Serveur DNS]
C --> D[Interprétation de la requête]
D --> E[Réponse DNS]
E -- Je connais ce NDD, voici l'IP --> A
```
</div>
<div v-after>
```mermaid {theme: 'neutral', scale: 0.5}
graph TD
A[Ordinateur] --> F[Serveur cible]
```
</div>
<div v-click class="w-40 text-xs">
  <div>
  Ex: Lorsqu'on tape <span v-mark.circle.orange="2">coda.school</span>, on fait appel à 1 serveur DNS
  Ce serveur va alors nous répondre en indiquant l'IP du serveur auquel on cherche à accéder. Notre ordinateur va donc ensuite pouvoir faire la requête directement à 
  </div>
  <div>
  <div v-mark.highlight.orange="2">l'IP demandé.</div>
  </div>
</div>
</div>




<!-- 

Sur votre navigateur Internet, vous tapez google.com : vous n'avez pas de besoin de connaitre l'IP du serveur qui va vous répondre.
Pensez annuaire / répertoire
-->


---
transition: fade-out
hideInToc: true
---

# Hiérarchie du DNS

<div>
```mermaid {scale: 0.7}
graph TB
  a((www.coda-school.ymag.cloud))
  a -- Sous-domaine --> b[www]
  a -- Nom d'hôte ou de second niveau --> c[coda-school]
  a -- Sous-domaine de second niveau --> d[ymag]
  a -- Domaine de premier niveau (TLD) --> e[cloud]
```

</div>
</br>
<p v-click class="opacity-90 border-1 border-separate p2">Les notions à retenir : Racine, top-level domain, domaine, sous-domaine</p>
<p v-after class="opacity-90 border-1 border-separate p2">Le nom est résolu de <span class="font-bold">droite à gauche</span>, en partant de la racine</p>
<!-- 
Exemple de hiérarchie de DNS 
-->

---
transition: fade-out
hideInToc: true
---

# Comment acheter un nom de domaine ?

Vous aurez probablement besoin à un moment d'acheter et de gérer un nom de Domaine. (Gérer les A-Record, C-Name, etc.)

Parmis les fournisseurs connus en France pour les noms de domaines, on trouve : 
- Gandi
- OVH
- GoDaddy


<!-- 
de 10€ par an (voire gratuit) à beaucoup (plusieurs milliers d'euros annuels)
-->