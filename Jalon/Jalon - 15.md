***
### NAT EDGE WANRTR

**Objectif** : Ajouter la configuration de **NAT** pour le **routeur WANRTR** afin d'assurer l'accès des services internes (Web, VPN, Webmail) depuis Internet. Ce NAT permettra la traduction des adresses IP privées des serveurs internes vers les adresses publiques et l'accès via les ports spécifiques.

#### 1. Configuration de NAT sur le routeur WANRTR

Dans ce jalon, nous allons configurer le NAT sur le routeur **WANRTR** pour que le trafic entrant et sortant du réseau interne vers Internet soit correctement traduit. Voici les éléments principaux :

- **NAT dynamique** : Nous allons configurer un NAT dynamique pour permettre à plusieurs hôtes du réseau interne de partager la même adresse IP publique pour l'accès à Internet.
- **NAT statique** : Nous avons déjà configuré des règles NAT statiques pour rediriger les services spécifiques (Web, VPN, Webmail) depuis l'extérieur vers les serveurs internes.

#### 2. Configuration des interfaces et du NAT dynamique

Tout d'abord, nous allons configurer les interfaces du routeur WANRTR pour établir les interfaces internes et externes.

##### Interface interne (LAN) - Réseau Privé
```ios
interface GigabitEthernet0/1
 description LAN interface (Internal Network)
 ip address 192.168.1.1 255.255.255.0  ! Adresse IP privée du réseau interne
 ip nat inside                   ! Marquer cette interface comme "inside" pour le NAT
```
**Interface externe (WAN) - Réseau Public**
```ios
interface GigabitEthernet0/0
 description WAN interface (Internet)
 ip address 217.5.160.1 255.255.255.252  ! Adresse IP publique fournie par le FAI
 ip nat outside                  ! Marquer cette interface comme "outside" pour le NAT
```
#### 3. Configuration du NAT dynamique sur WANRTR

Le NAT dynamique permet à plusieurs hôtes internes d'utiliser l'adresse IP publique pour l'accès à Internet. Nous allons configurer une règle **PAT (Port Address Translation)** qui utilise l'adresse publique du routeur pour traduire les connexions sortantes des hôtes internes.

##### Configuration de PAT pour NAT dynamique
```ios
ip nat inside source list 1 interface GigabitEthernet0/0 overload
```
- **list 1** : Liste d'accès qui définit les adresses IP internes autorisées à accéder à Internet.
- **GigabitEthernet0/0** : Interface externe (WAN) du routeur.
- **overload** : Permet à plusieurs adresses internes d'utiliser la même adresse publique (PAT).

##### Définir la liste d'accès pour le NAT dynamique
```ios
access-list 1 permit 192.168.1.0 0.0.0.255
```
- Cette liste d'accès permet à toutes les adresses IP internes du réseau **192.168.1.0/24** de pouvoir accéder à Internet.

#### 4. Configuration du NAT statique pour les services spécifiques

Nous avons déjà configuré les règles NAT statiques pour permettre l'accès aux services spécifiques. Voici un rappel des configurations NAT statiques sur **WANRTR** pour ces services.

##### Accès au serveur Web (HQWEBSRV
```ios
ip nat inside source static tcp 10.5.10.5 80 217.5.160.5 80
ip nat inside source static tcp 10.5.10.5 443 217.5.160.5 443
```
**Accès au serveur VPN (HQINFRASRV)**
```ios
ip nat inside source static tcp 10.5.10.5 4443 191.5.157.33 4443
```
**Accès au serveur Webmail (HQMAILSRV)**
```ios
ip nat inside source static tcp 10.5.10.5 80 191.5.157.33 80
ip nat inside source static tcp 10.5.10.5 443 191.5.157.33 443
```