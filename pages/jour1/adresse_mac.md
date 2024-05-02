# Votre adresse MAC est-elle unique ?

<br/>
<p v-click class="opacity-90 border-1 border-separate p2">Une adresse MAC (Media Access Control1), parfois nommée adresse physique, est un identifiant physique stocké dans une carte réseau ou une interface réseau similaire. </p>

<p v-click class="opacity-90 border-1 border-separate p2">L'adresse MAC est attribué par le constructeur (conventions). Mais peut-être changé de façon logicielle :</p>

<div class="mb-30" v-click>

```bash
sudo ifconfig wlan1 down
sudo ifconfig wlan1 hw ether 12:e1:7d:f8:a3:e5
```


</div>

</br>


<a v-click href="https://fr.wikipedia.org/wiki/Adresse_MAC">
Plus d'infos
</a>

<!-- Standard : 6 Octets, notion hexadécimale. 

Combien ça fait de bits ? (48)
-->
