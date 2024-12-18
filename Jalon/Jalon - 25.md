### HQDCSRV ADCS

##### Introduction

Le rôle **ADCS** (Active Directory Certificate Services) permet d'établir une infrastructure de gestion de certificats pour sécuriser les communications internes et authentifier les utilisateurs, machines et serveurs d’un domaine.

L’ADCS repose sur la mise en place d’une **Autorité de Certification** (CA), qui délivre des certificats numériques. Voici la configuration et les composants essentiels pour ce jalon.

---

### 1. Déploiement de l’Autorité de Certification

##### Contexte

L’autorité de certification interne permet de gérer les certificats nécessaires aux services internes tels que :

- **Authentification des utilisateurs et des machines**.
- **Sécurisation des échanges réseau (SSL/TLS)**.
- **Signature des messages et des documents**.

##### Configuration appliquée

- **Autorité de Certification Racine :** `WSFR-INT-ROOT-CA`
    - Cette CA racine est l’autorité centrale pour émettre et signer des certificats dans le domaine.
![[Jalon - 25-1.webp]]
<p align="center"><em><small>Vue de l'Autorité de Certification WSFR-INT-ROOT-CA</small></em></p> 

---

### 2. Détails d’un certificat émis

##### Objectif

Vérifier les détails d’un certificat délivré par la CA **WSFR-INT-ROOT-CA** pour le serveur de messagerie interne.

##### Détails du certificat

- **Émis pour :**
    - **Nom commun (CN) :** `hqmailsrv.hq.wsl2024.org`
    - **Organisation (O) :** `ws/2024`
    - **Unité d'organisation (UO) :** `HQ`
- **Émis par :**
    - **Autorité de Certification :** `WSFR-INT-ROOT-CA`
- **Période de validité :**
    - **Date d’émission :** dimanche 15 décembre 2024 à 13:59:45
    - **Date d’expiration :** mardi 15 décembre 2026 à 13:59:45
- **Empreinte SHA-256 :** Une empreinte unique permettant de vérifier l’intégrité du certificat.
![[Jalon - 25-2.webp]]
<p align="center"><em><small>Détails du certificat émis pour hqmailsrv.hq.wsl2024.org</small></em></p> 

---

### 3. Visionneuse de certificats - Informations générales

##### Objectif

Analyser les informations affichées dans la visionneuse de certificats pour valider l'utilisation prévue.

##### Informations visibles :

- **Titre de la fenêtre :** "Certificat"
- **Onglet "Général" :**
    - **Rôles du certificat :** Toutes les stratégies d'émission et d'application.
    - **Émetteur :** `WSFR-INT-ROOT-CA`
    - **Validité :** Du 11/12/2024 au 11/12/2029
- **Bouton OK :** Permet de fermer la visionneuse.
![[Jalon - 25-3.webp]]
<p align="center"><em><small>Vue de la visionneuse de certificats - onglet Général</small></em></p> 

---

### 4. Liste des certificats délivrés

##### Objectif

Afficher la liste des certificats délivrés par l’autorité de certification locale.

##### Détails des colonnes :

- **Identifiant :** Numéro unique de chaque certificat.
- **Date d’effet :** Début de validité du certificat.
- **Date d’expiration :** Fin de validité.
- **Nom commun d’émission (CN) :** Nom du serveur ou de l'utilisateur associé.
- **Organisation d'émission (O) :** Nom de l’organisation.

##### Types de certificats gérés :

- **Certificats délivrés :** Clés actuellement actives.
- **Demandes en attente :** Requêtes en cours de traitement.
- **Demandes ayant échoué :** Requêtes rejetées.
- **Modèles de certificats :** Modèles servant de base pour émettre de nouveaux certificats.
![[Jalon - 25-4.webp]]
<p align="center"><em><small>Liste des certificats délivrés par WSFR-INT-ROOT-CA</small></em></p>