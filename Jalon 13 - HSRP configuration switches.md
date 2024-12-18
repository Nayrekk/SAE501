# HSRP (Hot Standby Router Protocol)
***

- **Rôle** : Assure une passerelle par défaut redondante pour les hôtes dans chaque VLAN.
- **Avantages** :
    - **Haute disponibilité** : Si le switch actif tombe, le switch en veille prend le relais automatiquement.
    - **Continuité du service** : Les hôtes n’ont aucune interruption de connectivité.

Nous avons configurer HSRP sur les switchs CoreSW1 et CoreSW2 pour assurer une redondance si l'un venait à tomber.
# Configuration HSRP
***
*Captures d'écran prises dans en executant "show running-config"*
<br>
![[Jalon13.4.png]]
**Explication :**
- Les lignes `ip address` sont juste pour les adresses des interfaces VLANs 
- `standby x ip <10.5.x.x>` désignent les adresses ip virtuels
- `standby x priority 110/100` désigne la priorité pour le switchs la priorité la plus haute sera active pendant que l'autre sera en standby lorsque les deux switchs fonctionnes comme il faut
- `standby x preempt` permet à un switch avec une priorité plus élevée de reprendre automatiquement le rôle de switch actif lorsqu'il revient en ligne après une panne.
# CoreSW1 HSRP
***
*Captures d'écran prises dans en executant "show standby brief"*
<br>
![[Jalon13.1.png]]
Nous pouvons voir que le switch "CoreSW1" est actif.
# CoreSW2 HSRP
***
_Captures d'écran prises dans en executant "show standby brief"_
<br>
![[Jalon13.2.png]]
Nous pouvons voir que le switch "CoreSW2" est en standby.