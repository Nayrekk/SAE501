# Switch en dessous ESXI
***
![[Jalon9.6.png]]
# NIC Physiques
***
- **Connexion réseau de l’hyperviseur :**
    
    - Elle connecte le serveur ESXi aux autres équipements réseau (switch, routeur, etc.) pour fournir une connectivité au réseau local (LAN) ou à Internet.

- **Connectivité pour les machines virtuelles :**
    
    - Les machines virtuelles (VMs) sur ESXi utilisent les NIC physiques pour envoyer et recevoir des données via les réseaux physiques externes.

![[Jalon9.1.png]]
# NIC VmKernel
***
- **Gestion de l’hyperviseur (Management Network)** :
    
    - Interface utilisée pour administrer le serveur ESXi.
    - Permet également l'accès à ESXi via SSH ou HTTP.

- **vMotion** :
    
    - Utilisée pour migrer des machines virtuelles d’un serveur ESXi à un autre sans interruption.

![[Jalon9.2.png]]
# Virtuals Switchs
***
- **Connectivité des machines virtuelles (VMs) :**
    
    - Un vSwitch relie les cartes réseau virtuelles des VMs (vNICs) aux NICs physiques du serveur.
    - Permet aux VMs de communiquer entre elles ou avec l’extérieur via le réseau physique.

- **Gestion des services ESXi :**
    
    - Relie les interfaces VMkernel aux NICs physiques pour permettre à l’hyperviseur de fournir ses services.

![[Jalon9.3.png]]
# PortGroup
***
- **Segmentation réseau :**
    
    - Associe un VLAN spécifique aux interfaces réseau des VMs ou aux services (via VMkernel).
    - Permet d’organiser les VMs en groupes isolés.

- **Application de politiques réseau :**
    
    - Définit des règles de sécurité, de gestion de trafic.
    - Facilite la gestion réseau pour un groupe de VMs partageant les mêmes besoins.

- **Simplification des connexions :**
    
    - Les VMs connectées à un Port Group partagent automatiquement les configurations réseau définies pour ce groupe.

![[Jalon9.4.png]]
# Vlan 20 sur ESXI
***
![[Jalon9.5.png]]
***Nous pouvons voir une machine comment un VLAN est configuré dans l'ESXI***