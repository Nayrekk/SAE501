### WLC - Configuration de base

La configuration de base d'un contrôleur de réseau sans fil (WLC) implique plusieurs étapes essentielles pour assurer une gestion efficace du réseau sans fil. Voici les étapes recommandées :

#### 1. Création du VLAN de gestion

- Créez le VLAN 99 sur votre commutateur pour la gestion.
- Assurez-vous que le VLAN est propagé à travers le réseau et que les ports nécessaires sont affectés à ce VLAN.

#### 2. Attribution de l'adresse IP au VLAN 99

- Attribuez une adresse IP statique au VLAN 99 sur le commutateur.
- Cette adresse IP servira de passerelle par défaut pour le WLC.

#### 3. Configuration de l'interface GigabitEthernet2

- Configurez l'interface GigabitEthernet2 en mode accès et affectez-la au VLAN 99.
- Désactivez les autres interfaces sur l'hôte ESXi pour éviter tout conflit.

#### 4. Ajout de la route par défaut

- Ajoutez une route par défaut sur le WLC pointant vers l'adresse IP de la passerelle (par exemple, 10.5.99.254).

***
### Configuration sur le commutateur Cisco :
```ios
# Création du VLAN 99
HQWLC# configure terminal
HQWLC(config)# vlan 99
HQWLC(config-vlan)# name Management
HQWLC(config-vlan)# exit

# Attribution de l'adresse IP au VLAN 99
HQWLC(config)# interface vlan 99
HQWLC(config-if)# ip address 10.5.99.1 255.255.255.0
HQWLC(config-if)# no shutdown
HQWLC(config-if)# exit

# Configuration de l'interface GigabitEthernet2
HQWLC(config)# interface range gigabitEthernet 2
HQWLC(config-if-range)# switchport mode access
HQWLC(config-if-range)# switchport access vlan 99
HQWLC(config-if-range)# exit
```

---

### Configuration sur le WLC :

```ios
# Accès au mode de configuration

# Configuration de l'interface VLAN 99
WLC(config)# interface vlan 99
WLC(config-if)# ip address 10.5.99.2 255.255.255.0
WLC(config-if)# no shutdown
WLC(config-if)# exit

# Ajout de la route par défaut
WLC(config)# ip route 0.0.0.0 0.0.0.0 10.5.99.254
```
