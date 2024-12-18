### REMDCSRV - Configuration ADDS + DNS

La configuration d'Active Directory Domain Services (ADDS) et de DNS sous Windows Server implique plusieurs étapes essentielles, telles que la configuration du domaine, des contrôleurs de domaine, des forêts, et des partitions DNS. Les commandes PowerShell utilisées permettent d'extraire des informations sur la configuration d'ADDS et DNS.

#### 1.Informations sur le domaine avec `Get-ADDomain`

La commande `Get-ADDomain` permet d'afficher des informations sur le domaine Active Directory actuel.

Exemple de sortie :
```
PS C:\Users\Administrateur> Get-ADDomain                                                                                

AllowedDNSSuffixes                 : {}
ChildDomains                       : {}
ComputersContainer                 : CN=Computers,DC=rem,DC=wsl2024,DC=org
DeletedObjectsContainer            : CN=Deleted Objects,DC=rem,DC=wsl2024,DC=org
DistinguishedName                  : DC=rem,DC=wsl2024,DC=org
DNSRoot                            : rem.wsl2024.org
DomainControllersContainer         : OU=Domain Controllers,DC=rem,DC=wsl2024,DC=org
DomainMode                         : Windows2016Domain
DomainSID                          : S-1-5-21-999973892-646059867-1061345356
ForeignSecurityPrincipalsContainer : CN=ForeignSecurityPrincipals,DC=rem,DC=wsl2024,DC=org
Forest                             : wsl2024.org
InfrastructureMaster               : REMDCSRV.rem.wsl2024.org
LastLogonReplicationInterval       :
LinkedGroupPolicyObjects           : {cn={439ACC18-A326-480C-9528-FD2C714E2BDF},cn=policies,cn=system,DC=rem,DC=wsl2024
                                     ,DC=org, CN={31B2F340-016D-11D2-945F-00C04FB984F9},CN=Policies,CN=System,DC=rem,DC
                                     =wsl2024,DC=org}
LostAndFoundContainer              : CN=LostAndFound,DC=rem,DC=wsl2024,DC=org
Name                               : rem
NetBIOSName                        : REM
ObjectClass                        : domainDNS
ObjectGUID                         : 095c2fc1-28b5-4b46-abc4-5e96f62489e4
ParentDomain                       : wsl2024.org
PDCEmulator                        : REMDCSRV.rem.wsl2024.org
PublicKeyRequiredPasswordRolling   : True
QuotasContainer                    : CN=NTDS Quotas,DC=rem,DC=wsl2024,DC=org
ReadOnlyReplicaDirectoryServers    : {}
ReplicaDirectoryServers            : {REMDCSRV.rem.wsl2024.org}
RIDMaster                          : REMDCSRV.rem.wsl2024.org
SystemsContainer                   : CN=System,DC=rem,DC=wsl2024,DC=org
UsersContainer                     : CN=Users,DC=rem,DC=wsl2024,DC=org
```
- **DNSRoot** : Le nom DNS du domaine est `rem.wsl2024.org`.
- **PDCEmulator, RIDMaster, InfrastructureMaster** : Ce sont les rôles FSMO (Flexible Single Master Operation) détenus par le contrôleur de domaine `REMDCSRV.rem.wsl2024.org`.
- **DomainMode** : Le mode du domaine est **Windows2016Domain**, ce qui signifie que le domaine fonctionne avec les fonctionnalités de Windows Server 2016.

#### 2. Informations sur la forêt avec `Get-ADForest`

La commande `Get-ADForest` fournit des informations sur la forêt Active Directory.

Exemple de sortie :
```
PS C:\Users\Administrateur> Get-ADForest

ApplicationPartitions : {DC=DomainDnsZones,DC=wsl2024,DC=org, DC=ForestDnsZones,DC=wsl2024,DC=org}
CrossForestReferences : {}
DomainNamingMaster    : HQDCSRV.wsl2024.org
Domains               : {rem.wsl2024.org, wsl2024.org}
ForestMode            : Windows2016Forest
GlobalCatalogs        : {HQDCSRV.wsl2024.org, REMDCSRV.rem.wsl2024.org}
Name                  : wsl2024.org
RootDomain            : wsl2024.org
SchemaMaster          : HQDCSRV.wsl2024.org
Sites                 : {Default-First-Site-Name}
```
- **DomainNamingMaster** : Le contrôleur de domaine responsable du nommage des domaines dans la forêt est `HQDCSRV.wsl2024.org`.
- **GlobalCatalogs** : Les serveurs global catalog de la forêt sont `HQDCSRV.wsl2024.org` et `REMDCSRV.rem.wsl2024.org`.
- **ForestMode** : Le mode de la forêt est **Windows2016Forest**, ce qui permet d'utiliser les fonctionnalités de Windows Server 2016.

#### 3. Informations sur le contrôleur de domaine avec `Get-ADDomainController`

La commande `Get-ADDomainController` fournit des informations détaillées sur les contrôleurs de domaine.

Exemple de sortie :
```
PS C:\Users\Administrateur> Get-ADDomainController

ComputerObjectDN           : CN=REMDCSRV,OU=Domain Controllers,DC=rem,DC=wsl2024,DC=org
Enabled                    : True
Forest                     : wsl2024.org
HostName                   : REMDCSRV.rem.wsl2024.org
IPv4Address                : 10.5.100.1
IsGlobalCatalog            : True
IsReadOnly                 : False
Name                       : REMDCSRV
OperatingSystem            : Windows Server 2022 Standard
OperationMasterRoles       : {PDCEmulator, RIDMaster, InfrastructureMaster}
```

- **HostName** : Le nom de l'hôte du contrôleur de domaine est `REMDCSRV.rem.wsl2024.org`.
- **IPv4Address** : L'adresse IPv4 du contrôleur de domaine est `10.5.100.1`.
- **IsGlobalCatalog** : `REMDCSRV` est un serveur Global Catalog, ce qui permet de stocker des informations sur tous les objets dans la forêt Active Directory.

#### 4. Configuration DNS sur le serveur

Active Directory repose sur le DNS pour la résolution de noms. Le serveur DNS utilisé est généralement celui du contrôleur de domaine.

- **DNS** : Les zones DNS pour le domaine **rem.wsl2024.org** et la forêt **wsl2024.org** sont configurées sur les serveurs DNS associés, généralement configurés sur les contrôleurs de domaine (`REMDCSRV` et `HQDCSRV`).

