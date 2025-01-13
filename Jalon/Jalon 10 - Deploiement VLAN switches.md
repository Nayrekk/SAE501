Pour le déploiement des VLANs sur les switches nous avons d'abord créé les VLANs et les avons nommés.
Nous les avons ensuite attribués aux interfaces selon notre plan de notre infrastructure.
Sur les CoreSWs, nous avons attribués une ip par interface sur chaque VLANs selon notre plan ip.
# CoreSW1
***
*Captures d'écran prises dans en executant "show running-config"*
<br>
![[Jalon10.1.png]]
***Liste des VLANs sur CoreSW1***
<br>
![[Jalon10.2.png]]
***Configuration des interfaces VLANs sur CoreSW2***

# CoreSW2
***
*Captures d'écran prises dans en executant "show running-config"*
<br>
![[Jalon10.3.png]]
***Liste des VLANs sur CoreSW2***
<br>
![[Jalon10.4.png]]
***Configuration des interfaces VLANs sur CoreSW2***
# AccSW1
***
*Captures d'écran prises dans en executant "show running-config"*
<br>
![[Jalon10.5.png]]
***Liste des VLANs sur AccSW1***
<br>
![[Jalon10.6.png]]
***Configuration des interfaces VLANs sur AccSW1***
# AccSW2
***
*Captures d'écran prises dans en executant "show running-config"*

![[Jalon10.7.png]]
***Liste des VLANs sur AccSW2***
<br>
![[Jalon10.8.png]]
***Configuration des interfaces VLANs sur AccSW2***