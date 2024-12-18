***
# HSRP EDGE routeurs

**Objectif** : Mettre en place HSRP (Hot Standby Router Protocol) entre les routeurs EDGE1 et EDGE2 pour assurer la redondance et la haute disponibilité des routes réseau sur le VLAN 30.

#### 1. Présentation de HSRP

HSRP est un protocole de redondance de passerelle qui permet à deux ou plusieurs routeurs de partager une même adresse IP virtuelle (VIP) pour assurer la continuité du service en cas de défaillance d'un des routeurs. Dans ce cas, EDGE1 et EDGE2 travailleront ensemble pour fournir une passerelle commune pour les dispositifs sur le VLAN 30.

#### 2. Objectifs de la configuration

- **EDGE1** et **EDGE2** seront configurés pour participer à HSRP sur le VLAN 30 (adresse IP virtuelle : `217.5.160.14`).
- Le routeur **actif** sera celui avec la priorité la plus élevée. En cas de défaillance du routeur actif, le routeur avec la priorité suivante deviendra actif.
- **EDGE1** aura une priorité de 110 pour devenir le routeur principal (actif) sur le VLAN 30, tandis que **EDGE2** aura une priorité plus faible.

### Configuration HSRP sur EDGE1 et EDGE2

#### Configuration sur EDGE1 :
```ios
interface GigabitEthernet0/1.33
 description HSRP VLAN 30 connection to EDGE2
 encapsulation dot1Q 30
 ip address 217.5.160.11 255.255.255.240
 standby version 2
 standby 30 ip 217.5.160.14  
 standby 30 priority 110  
 standby 30 preempt            
```
- **interface GigabitEthernet0/1.33** : Interface VLAN 30 sur EDGE1.
- **standby version 2** : Définit la version du protocole HSRP (version 2 est plus moderne et prend en charge la priorité et d'autres fonctionnalités avancées).
- **standby 30 ip 217.5.160.14** : L'adresse IP virtuelle partagée entre EDGE1 et EDGE2.
- **standby 30 priority 110** : EDGE1 a une priorité plus élevée pour devenir le routeur actif.
- **standby 30 preempt** : Cette option permet à EDGE1 de reprendre le rôle de routeur actif si celui-ci redémarre ou redevient disponible après une panne.

#### Configuration sur EDGE2
```ios
interface GigabitEthernet0/1.33
 description HSRP VLAN 30 connection to EDGE1
 encapsulation dot1Q 30
 ip address 217.5.160.12 255.255.255.240
 standby version 2
 standby 30 ip 217.5.160.14
 standby 30 priority 100
 standby 30 preempt
```

- **interface GigabitEthernet0/1.33** : Interface VLAN 30 sur EDGE2.
- **standby version 2** : Version 2 de HSRP.
- **standby 30 ip 217.5.160.14** : L'adresse IP virtuelle partagée entre EDGE1 et EDGE2.
- **standby 30 priority 100** : EDGE2 a une priorité plus basse, ce qui le rend passif tant qu'EDGE1 est actif.
- **standby 30 preempt** : Permet à EDGE2 de devenir le routeur actif si EDGE1 échoue ou devient inactif.

### Explications des Configurations

1. **Interface VLAN 30** :
    
    - La configuration HSRP est appliquée sur l'interface VLAN 30 sur les deux routeurs. Cette interface est responsable de l'accès au réseau et utilise le VLAN 30 avec l'encapsulation **dot1Q 30**.
2. **Adresse IP virtuelle (VIP)** :
    
    - **217.5.160.14** est l'adresse IP virtuelle partagée entre les deux routeurs. Elle est utilisée par les hôtes du VLAN 30 pour la passerelle par défaut, assurant ainsi la redondance. Les hôtes n'ont pas besoin de savoir quel routeur est actif, car ils utiliseront toujours cette adresse IP.
3. **Priorité HSRP** :
    
    - **EDGE1** a une priorité de **110**, tandis qu'**EDGE2** a une priorité de **100**. Cela signifie que, normalement, EDGE1 sera le routeur actif. Si EDGE1 tombe en panne, EDGE2 prendra le relais et deviendra le routeur actif.
4. **Preemption** :
    
    - L'option **preempt** permet à un routeur de reprendre le rôle de routeur actif si sa priorité est plus élevée et s'il redémarre après avoir perdu ce rôle. Ainsi, si EDGE1 redémarre, il deviendra le routeur actif de nouveau, même si EDGE2 était auparavant devenu actif en raison d'une panne de EDGE1.
5. **HSRP Version 2** :
    
    - La version 2 d'HSRP est utilisée, car elle offre des fonctionnalités avancées comme la gestion de la priorité et du préemption. Elle permet également un plus grand nombre de groupes HSRP (jusqu'à 4096).

### Routage de secours avec HSRP

Avec HSRP configuré, les hôtes sur le VLAN 30 utiliseront l'adresse IP virtuelle **217.5.160.14** comme passerelle par défaut. En cas de panne d'un des routeurs, le second prendra automatiquement le relais avec une interruption minimale pour les utilisateurs.