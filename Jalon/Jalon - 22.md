***
### Jalon : Configuration d'Active Directory Domain Services (ADDS) sur HQDCSRV

#### 1. Vérification des informations de domaine

Commande :
```powershell
Get-ADDomain
```

Résultat :
``` yaml
AllowedDNSSuffixes                 : {}
ChildDomains                       : {rem.wsl2024.org}
ComputersContainer                 : CN=Computers,DC=wsl2024,DC=org
DeletedObjectsContainer            : CN=Deleted Objects,DC=wsl2024,DC=org
DistinguishedName                  : DC=wsl2024,DC=org
DNSRoot                            : wsl2024.org
DomainControllersContainer         : OU=Domain Controllers,DC=wsl2024,DC=org
DomainMode                         : Windows2016Domain
DomainSID                          : S-1-5-21-4033187911-3485779975-3754915922
ForeignSecurityPrincipalsContainer : CN=ForeignSecurityPrincipals,DC=wsl2024,DC=org
Forest                             : wsl2024.org
InfrastructureMaster               : HQDCSRV.wsl2024.org
LastLogonReplicationInterval       :
LinkedGroupPolicyObjects           : {cn={91327A7F-AD79-49B6-AB21-6911559BBF8A},cn=policies,cn=system,DC=wsl2024,DC=org
                                     ,
                                     CN={31B2F340-016D-11D2-945F-00C04FB984F9},CN=Policies,CN=System,DC=wsl2024,DC=org}
LostAndFoundContainer              : CN=LostAndFound,DC=wsl2024,DC=org
ManagedBy                          :
Name                               : wsl2024
NetBIOSName                        : WSL2024
ObjectClass                        : domainDNS
ObjectGUID                         : 4658fe9f-8d5f-4f13-8b69-ad340c1c443e
ParentDomain                       :
PDCEmulator                        : HQDCSRV.wsl2024.org
PublicKeyRequiredPasswordRolling   : True
QuotasContainer                    : CN=NTDS Quotas,DC=wsl2024,DC=org
ReadOnlyReplicaDirectoryServers    : {}
ReplicaDirectoryServers            : {HQDCSRV.wsl2024.org}
RIDMaster                          : HQDCSRV.wsl2024.org
SubordinateReferences              : {DC=rem,DC=wsl2024,DC=org, DC=ForestDnsZones,DC=wsl2024,DC=org,
                                     DC=DomainDnsZones,DC=wsl2024,DC=org, CN=Configuration,DC=wsl2024,DC=org}
SystemsContainer                   : CN=System,DC=wsl2024,DC=org
UsersContainer                     : CN=Users,DC=wsl2024,DC=org
```

#### 2. Vérification des informations de la forêt

Commande :
```powershell
Get-ADForest
```

Résultat :
``` yaml
ApplicationPartitions : {DC=DomainDnsZones,DC=wsl2024,DC=org, DC=ForestDnsZones,DC=wsl2024,DC=org}
CrossForestReferences : {}
DomainNamingMaster    : HQDCSRV.wsl2024.org
Domains               : {rem.wsl2024.org, wsl2024.org}
ForestMode            : Windows2016Forest
GlobalCatalogs        : {HQDCSRV.wsl2024.org}
Name                  : wsl2024.org
PartitionsContainer   : CN=Partitions,CN=Configuration,DC=wsl2024,DC=org
RootDomain            : wsl2024.org
SchemaMaster          : HQDCSRV.wsl2024.org
Sites                 : {Default-First-Site-Name}
SPNSuffixes           : {}
UPNSuffixes           : {}
```

#### 3. Vérification des contrôleurs de domaine

Commande :
```yaml
Get-ADDomainController
```

Résultat :
```yaml
ComputerObjectDN           : CN=HQDCSRV,OU=Domain Controllers,DC=wsl2024,DC=org
DefaultPartition           : DC=wsl2024,DC=org
Domain                     : wsl2024.org
Enabled                    : True
Forest                     : wsl2024.org
HostName                   : HQDCSRV.wsl2024.org
InvocationId               : 6ec66d47-1033-48c1-aca2-171b3f0f43a7
IPv4Address                : 10.5.10.1
IPv6Address                :
IsGlobalCatalog            : True
IsReadOnly                 : False
LdapPort                   : 389
Name                       : HQDCSRV
NTDSSettingsObjectDN       : CN=NTDS Settings,CN=HQDCSRV,CN=Servers,CN=Default-First-Site-Name,CN=Sites,CN=Configuration,DC=wsl2024,DC=org
OperatingSystem            : Windows Server 2022 Standard Evaluation
OperatingSystemHotfix      :
OperatingSystemServicePack :
OperatingSystemVersion     : 10.0 (20348)
OperationMasterRoles       : {SchemaMaster, DomainNamingMaster, PDCEmulator, RIDMaster...}
Partitions                 : {DC=ForestDnsZones,DC=wsl2024,DC=org, DC=DomainDnsZones,DC=wsl2024,DC=org, CN=Schema,CN=Configuration,DC=wsl2024,DC=org,
                             CN=Configuration,DC=wsl2024,DC=org...}
ServerObjectDN             : CN=HQDCSRV,CN=Servers,CN=Default-First-Site-Name,CN=Sites,CN=Configuration,DC=wsl2024,DC=org
ServerObjectGuid           : 4d61ece5-6cc3-4f0e-a308-b470d3aad0fc
Site                       : Default-First-Site-Name
SslPort                    : 636
```

