### HQDCSRV - File Services

#### Contexte et Objectifs

Le serveur **HQDCSRV** a pour mission principale d’assurer la gestion des services de fichiers pour les différents départements de l’organisation. Cela comprend la centralisation, la gestion des permissions, la mise en place de quotas, et l’accès sécurisé aux fichiers partagés. Ce document décrit l’état actuel de la configuration du serveur, incluant les partages SMB, les volumes, les quotas, les disques physiques, et les permissions associées.

---

#### Configuration des Partages SMB

Voici la liste des partages configurés sur **HQDCSRV** :

|**Nom**|**Chemin**|**Description**|
|---|---|---|
|`ADMIN$`|`C:\Windows`|Administration à distance|
|`C$`|`C:\`|Partage par défaut|
|`CertEnroll`|`C:\Windows\system32\CertSrv\CertEnroll`|Services de certificats Active Directory|
|`D$`|`D:\`|Partage par défaut|
|`Department2`|`D:\shares\Department`|Partage du département|
|`img`|`C:\img`|Répertoire des images|
|`jticipe`|`D:\shares\datausers\jticipe`|Espace utilisateur individuel (jticipe)|
|`npresso`|`D:\shares\datausers\npresso`|Espace utilisateur individuel (npresso)|
|`rola`|`D:\shares\datausers\rola`|Espace utilisateur individuel (rola)|
|`Public2`|`D:\shares\Public`|Partage public|
|`Sales`|`D:\shares\Department\Sales`|Dossier pour l’équipe des ventes|
|`NETLOGON`|`C:\Windows\SYSVOL\sysvol\wsl2024.org\SCRIPTS`|Scripts de logon Active Directory|
|`SYSVOL`|`C:\Windows\SYSVOL\sysvol`|Partage pour les services Active Directory|

---

#### Volumes du Serveur**

L’état des volumes du serveur **HQDCSRV** est le suivant :

|**Lettre**|**Nom**|**Système de Fichiers**|**Type**|**Espace Libre**|**Taille Totale**|
|---|---|---|---|---|---|
|`C:`||NTFS|Fixe|39.88 GB|59.33 GB|
|||NTFS|Fixe|115.42 MB|569 MB|
|`K:`|`SSS_X64FREE_FR-FR`|Inconnu|CD-ROM|0 B|4.71 GB|
|||FAT32|Fixe|66.92 MB|96 MB|
|`D:`|`DATA`|NTFS|Fixe|1.44 GB|1.96 GB|

---

#### Quotas de Stockage

Des quotas ont été configurés sur les dossiers utilisateurs pour éviter une consommation excessive d’espace disque :

|**Chemin**|**Taille Max (MB)**|**Modèle**|**Utilisation (MB)**|
|---|---|---|---|
|`D:\shares\datausers\jticipe`|20 MB|20mb|1 MB|
|`D:\shares\datausers\npresso`|20 MB|20mb|1 MB|
|`D:\shares\datausers\rola`|100 MB|Limite de 100 Mo|4 MB|
|`D:\shares\datausers\vtim`|20 MB|20mb|1 MB|

---

#### Disques Physiques

Le serveur est équipé de plusieurs disques configurés comme suit :

|**Numéro**|**Nom**|**Type de Média**|**Taille**|**Statut Opérationnel**|**Statut de Santé**|
|---|---|---|---|---|---|
|0|VMware Virtual NVMe Disk|SSD|60 GB|OK|Sain|
|1|VMware Virtual NVMe Disk|SSD|1 GB|OK|Sain|
|2|VMware Virtual NVMe Disk|SSD|1 GB|OK|Sain|
|3|VMware Virtual NVMe Disk|SSD|1 GB|OK|Sain|

---

#### Permissions des Dossiers Partagés

Les permissions des dossiers sont configurées pour assurer un accès approprié à chaque groupe ou utilisateur.

``` powershell
D:\shares BUILTIN\Administrateurs:(F)
          BUILTIN\Administrateurs:(I)(OI)(CI)(F)
          AUTORITE NT\Système:(I)(OI)(CI)(F)
          CREATEUR PROPRIETAIRE:(I)(OI)(CI)(IO)(F)
          BUILTIN\Utilisateurs:(I)(OI)(CI)(RX)
          BUILTIN\Utilisateurs:(I)(CI)(AD)
          BUILTIN\Utilisateurs:(I)(CI)(WD)

D:\shares\datausers BUILTIN\Administrateurs:(OI)(CI)(F)
                    AUTORITE NT\Système:(OI)(CI)(F)
                    CREATEUR PROPRIETAIRE:(OI)(CI)(IO)(F)
                    BUILTIN\Utilisateurs:(R)
                    WSL2024\npresso:(RX)
                    WSL2024\rola:(RX)
                    WSL2024\Administrateur:(RX)
                    WSL2024\vtim:(RX)

D:\shares\Department BUILTIN\Administrateurs:(F)
                     WSL2024\Administrateur:(OI)(CI)(F)
                     BUILTIN\Administrateurs:(OI)(CI)(F)
                     AUTORITE NT\Système:(OI)(CI)(F)
                     WSL2024\Sales:(RX)
                     WSL2024\Direction:(RX)
                     WSL2024\Factory:(RX)
                     WSL2024\IT:(RX)
                     WSL2024\Administrateur:(RX)
                     WSL2024\Warehouse:(RX)
                     WSL2024\Sales:(OI)(CI)(RX)
                     WSL2024\IT:(OI)(CI)(RX)
                     WSL2024\Direction:(OI)(CI)(RX)
                     WSL2024\Warehouse:(OI)(CI)(RX)
                     WSL2024\Factory:(OI)(CI)(RX)

D:\shares\Public AUTORITE NT\Système:(OI)(CI)(M)
                 WSL2024\OU_Shadow:(OI)(CI)(F)
                 WSL2024\Administrateur:(OI)(CI)(F)
                 BUILTIN\Administrateurs:(OI)(CI)(F)

D:\shares\datausers\jticipe AUTORITE NT\Système:(OI)(CI)(M)
                            WSL2024\jticipe:(OI)(CI)(F)
                            WSL2024\Administrateur:(OI)(CI)(F)
                            BUILTIN\Administrateurs:(OI)(CI)(F)

D:\shares\datausers\npresso AUTORITE NT\Système:(OI)(CI)(F)
                            WSL2024\npresso:(OI)(CI)(M)
                            WSL2024\Administrateur:(OI)(CI)(F)
                            BUILTIN\Administrateurs:(OI)(CI)(F)

D:\shares\datausers\rola AUTORITE NT\Système:(OI)(CI)(M)
                         WSL2024\rola:(OI)(CI)(F)
                         WSL2024\Administrateur:(OI)(CI)(F)
                         BUILTIN\Administrateurs:(OI)(CI)(F)

D:\shares\datausers\vtim WSL2024\vtim:(OI)(CI)(M)
                         WSL2024\Administrateur:(OI)(CI)(IO)(M)
                         BUILTIN\Administrateurs:(F)
                         BUILTIN\Administrateurs:(I)(OI)(CI)(F)
                         AUTORITE NT\Système:(I)(OI)(CI)(F)
                         CREATEUR PROPRIETAIRE:(I)(OI)(CI)(IO)(F)

D:\shares\datausers\rola\Nouveau dossier AUTORITE NT\Système:(I)(OI)(CI)(M)
                                         WSL2024\rola:(I)(OI)(CI)(F)
                                         WSL2024\Administrateur:(I)(OI)(CI)(F)
                                         BUILTIN\Administrateurs:(I)(OI)(CI)(F)

D:\shares\Department\Direction WSL2024\Administrateur:(OI)(CI)(F)
                               BUILTIN\Administrateurs:(OI)(CI)(F)
                               AUTORITE NT\Système:(OI)(CI)(F)
                               WSL2024\Direction:(OI)(CI)(M)

D:\shares\Department\Factory WSL2024\Administrateur:(OI)(CI)(F)
                             BUILTIN\Administrateurs:(OI)(CI)(F)
                             AUTORITE NT\Système:(OI)(CI)(F)
                             WSL2024\Factory:(OI)(CI)(M)

D:\shares\Department\IT WSL2024\Administrateur:(OI)(CI)(F)
                        BUILTIN\Administrateurs:(OI)(CI)(F)
                        AUTORITE NT\Système:(OI)(CI)(F)
                        WSL2024\IT:(OI)(CI)(M)

D:\shares\Department\Sales WSL2024\Administrateur:(OI)(CI)(F)
                           BUILTIN\Administrateurs:(OI)(CI)(F)
                           AUTORITE NT\Système:(OI)(CI)(F)
                           WSL2024\Sales:(OI)(CI)(M)

D:\shares\Department\Warehouse WSL2024\Administrateur:(OI)(CI)(F)
                               BUILTIN\Administrateurs:(OI)(CI)(F)
                               AUTORITE NT\Système:(OI)(CI)(F)
                               WSL2024\Warehouse:(OI)(CI)(M)

D:\shares\Public\logows.png WSL2024\Ordinateurs du domaine:(RX)
                            BUILTIN\Utilisateurs:(RX)
                            WSL2024\Utilisateurs du domaine:(RX)
                            AUTORITE NT\Système:(I)(M)
                            WSL2024\OU_Shadow:(I)(F)
                            WSL2024\Administrateur:(I)(F)
                            BUILTIN\Administrateurs:(I)(F)
```

