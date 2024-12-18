### REMDCSRV - Configuration DHCP sur Windows Server

Le service DHCP (Dynamic Host Configuration Protocol) sur Windows Server permet d'attribuer dynamiquement des adresses IP aux appareils d'un réseau. La configuration de base comprend la création d'une portée DHCP, la définition des options de configuration réseau et l'attribution d'adresses IP.

#### Exemple `ipconfig /renew` sur un poste client

Carte réseau Remote :
    Suffixe DNS propre à la connexion. . . : rem.wsl2024.org
    Adresse IPv6 de liaison locale. . . . .: fe80::679f:407f:8cae:2a08%4
    Adresse IPv4. . . . . . . . . . . . . .: 10.5.100.52
    Masque de sous-réseau. . . . . . . . . : 255.255.255.128
    Passerelle par défaut. . . . . . . . . : 10.5.100.126

Les informations retournées par la commande `ipconfig /renew` indiquent l'adresse IP, le masque de sous-réseau et la passerelle par défaut. Ces informations proviennent du serveur DHCP si le client est correctement configuré pour obtenir ses paramètres automatiquement.

#### Configuration du serveur DHCP sur Windows Server
1. **Installation du rôle DHCP**
    - Ouvrez le Gestionnaire de serveur.
    - Allez dans **Ajouter des rôles et fonctionnalités**.
    - Sélectionnez **Rôle DHCP** et suivez l'assistant pour installer le rôle sur le serveur.
2. **Création de la portée DHCP**
    - Dans le **Gestionnaire DHCP**, faites un clic droit sur **Vérifier les étendues DHCP** puis choisissez **Nouvelle étendue**.
    - Définissez les paramètres de la portée :
        - **Plage d'adresses IP** : Par exemple, de `10.5.100.10` à `10.5.100.110`.
        - **Masque de sous-réseau** : `255.255.255.128`.
        - **Passerelle par défaut** : `10.5.100.126` (Adresse de la passerelle du réseau).
        - **Serveurs DNS** : Indiquez l'adresse IP de vos serveurs DNS internes (par exemple, `10.5.100.1`).
3. **Configurer les options DHCP (exemple pour les routeurs et DNS)**
    - Allez dans **Options de serveur** sous **Serveur DHCP**.
    - Configurez les options suivantes :
        - **Option 003 - Routeur** : Ajoutez l'adresse de la passerelle `10.5.100.126`.
        - **Option 006 - Serveurs DNS** : Ajoutez l'adresse du serveur DNS `10.5.100.1`.
4. **Activation de la portée DHCP**
    Une fois la portée configurée, activez-la en cliquant droit sur la portée et sélectionnez **Activer**.

