## Jalon HQDCSRV - Configuration GPO


## 1. GPO "fond d'écran"

### Objectif

Déployer un fond d'écran standardisé pour assurer une cohérence visuelle sur l’ensemble des machines du domaine.

### Configuration appliquée

- **Stratégie :**
    - **Paramètre :** **Papier peint du Bureau**
        - **Chemin UNC :** `\\10.5.10.1\img\logows.jpg`
        - **Style :** Centré

### Avantages

- Uniformité visuelle sur les postes clients.
- Identification rapide de la machine appartenant au domaine.
![[Jalon - 24-1.webp]]
<p align="center"><em><small>Configuration GPO pour le fond d'écran via un chemin UNC</small></em></p> 

---

## 2. GPO "EDGE"

### Objectif

Contrôler la page d'accueil et les paramètres de démarrage pour **Internet Explorer** et **Microsoft Edge** afin de rediriger les utilisateurs vers un site d’entreprise.

### Configuration appliquée

- **Internet Explorer :**
    
    - **Désactiver la modification de la page d’accueil :** Activé
        - **Page d'accueil :** `www.wsl2024.org`
- **Microsoft Edge :**
    
    - **Configurer l’URL de la page d’accueil :** Activé
        - **URL :** `www.wsl2024.org`
    - **Définir la page Nouvel onglet comme page d’accueil :** Activé
        - **Sites au démarrage :** `www.wsl2024.org`

### Avantages

- Standardisation de l’environnement de navigation.
- Amélioration de la productivité avec une page d’accueil centralisée.
![[Jalon - 24-2.webp]]
<p align="center"><em><small>Configuration GPO pour les paramètres d'Internet Explorer et Edge</small></em></p> ![Image 2](file-8qsB2keqYbjawjt6PxfSvX)

---

## 3. GPO "Import_CA"

### Objectif

Importer des certificats racine pour sécuriser les connexions et assurer la confiance des communications internes.

### Configuration appliquée

- **Certificats ajoutés :**
    - **WSFR-EXT-ROOT-CA :**
        - **Date d’expiration :** 14/12/2034 01:32:20
    - **WSFR-INT-ROOT-CA :**
        - **Date d’expiration :** 11/12/2029 15:04:30

### Avantages

- Sécurisation des communications internes (SSL/TLS).
- Validation automatique des certificats pour les services internes.
![[Jalon - 24-3.webp]]
<p align="center"><em><small>Importation des certificats racine dans la configuration GPO</small></em></p> 

---

## 4. GPO "Panel"

### Objectif

Restreindre l’accès au **Panneau de configuration** et aux **applications** pour éviter des modifications non autorisées sur les postes clients.

### Configuration appliquée

- **Stratégie :**
    - **Interdire l’accès au Panneau de configuration :** Activé
    - **Interdire l’accès aux applications (liste noire) :** Activé
        - Liste d'applications interdites :
            - `control.exe` (Panneau de configuration)
            - `*.msc` (outils de gestion MMC)

### Avantages

- Renforce la sécurité des postes clients.
- Empêche les utilisateurs d’effectuer des modifications non autorisées.
![[Jalon - 24-4.webp]]
<p align="center"><em><small>Configuration GPO pour interdire l'accès au Panneau de configuration et aux applications</small></em></p>
