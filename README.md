<h1 align="center"> TheraFrozen - Système IoT de Surveillance et Traçabilité de la Chaîne du Froid </h1>

<p align="center">
  Plateforme industrielle de bout en bout dédiée à la métrologie continue, à la détection d'anomalies thermiques et à la conformité réglementaire de la chaîne du froid médicale et pharmaceutique (vaccins, banques de sang, réactifs de laboratoire et produits thermosensibles).
</p>

---

# Architecture et Fonctionnalités du Système

Le système repose sur une architecture IoT distribuée associant des microcontrôleurs connectés (ESP32), un courtier de messages de haute disponibilité (EMQX MQTT Broker), un backend d'analyse prédictive avec surveillance watchdog et une interface de supervision en temps réel basée sur les rôles.

---

## Super Administrateur (SUPER_ADMIN)

* **Tableau de Bord Haute Performance (Fast Insights & Multi-Capteurs) :**
  * Supervision simultanée en temps réel de tous les équipements connectés de la chaîne du froid.
  * Comparatif dynamique de température, d'hygrométrie et de force de signal radio (RSSI).
  * Détection instantanée des déconnexions matérielles via Watchdog actif et protocole MQTT Last Will & Testament (LWT).
  * Basculement fluide entre le mode comparatif global et le mode d'inspection détaillée par capteur.
* **Gestion du Parc d'Équipements et Passerelles IoT :**
  * Enregistrement, configuration et suppression des équipements (chambres froides, congélateurs grand froid, banques de sang).
  * Définition des plages thermiques cibles (ex. 2°C à 8°C pour vaccins, -25°C à -15°C pour congélateur grand froid).
  * Configuration personnalisée des seuils de tolérance et d'alerte critique par équipement.
* **Moteur d'Audit et Rapports Certifiés par Intelligence Artificielle :**
  * Génération immédiate d'audits certifiés analysant les dérives thermiques via intelligence artificielle (OpenAI).
  * Synthèse analytique détaillée en français ou en anglais couvrant jusqu'à 72 heures d'enregistrements continus.
  * Planification automatisée en tâche de fond (intervalles configurables de 6h, 12h, 24h ou 48h).
  * Registre immuable de rapports certifiés scellés téléchargeables au format PDF conforme aux normes d'audit.
* **Gestion des Utilisateurs et Rôles RBAC :**
  * Création, modification, blocage et suppression des comptes administrateurs et opérateurs.
  * Contrôle granulaire des permissions par module système (Tableau de bord, Rapports, Alertes, Équipements, Paramètres).
  * Supervision des sessions actives en temps réel avec capacité de révocation instantanée.
* **Configuration Globale du Système :**
  * Définition des seuils thermiques, hygrométriques et de sensibilité réseau RSSI par défaut pour la flotte.
  * Paramétrage des notifications d'urgence par courriel (intégration API Resend).
  * Sélection linguistique de l'interface (Français / Anglais).

---

## Administrateur (ADMIN)

L'Administrateur gère l'exploitation opérationnelle quotidienne des installations de stockage frigorifique.

* **Surveillance Continue des Équipements :**
  * Visualisation en temps réel des courbes thermiques et hygrométriques actualisées chaque 5 secondes.
  * Contrôle des indicateurs de conformité par rapport aux limites réglementaires HACCP.
* **Gestion Analytique des Alertes :**
  * Traitement des incidents de température (dépassement haut, risque de gel bas, dérive lente).
  * Consultation de la vélocité horaire des alertes et identification des plages horaires critiques.
  * Analyse des équipements les plus sollicités et de l'évolution mensuelle des incidents.
  * Acquittement traçable des alertes avec consignation de l'opérateur et de l'horodatage.
* **Consultation et Téléchargement des Rapports :**
  * Consultation du registre des rapports d'audit certifiés.
  * Téléchargement des rapports PDF certifiés pour archivage réglementaire.

---

## Opérateur / Utilisateur (USER)

L'Opérateur dispose d'un espace de travail ciblé garantissant la vérification rapide de l'intégrité des produits stockés.

* **Consultation Métrologique en Direct :**
  * Vue synthétique de l'état thermique et d'humidité des enceintes frigorifiques.
  * Réception des notifications visuelles d'alerte en direct via WebSocket.
* **Historique des Mesures :**
  * Consultation de l'évolution temporelle des mesures avec filtres journaliers et horaires.
  * Visualisation de la matrice de conformité globale (répartition entre mesures conformes, avertissements et alertes critiques).
* **Personnalisation de l'Espace de Travail :**
  * Sélection du thème visuel adapté à l'environnement de travail (mode sombre, mode clair, thèmes industriels à fort contraste).
  * Gestion du profil personnel et sécurisation du mot de passe.

---

# Démonstration Visuelle (Demo Pictures)

|<img width="1920" alt="Accueil" src="pics/Screenshot%202026-09-30%20172832.png" />|<img width="1920" alt="Fast Insights" src="pics/Screenshot%202026-09-30%20173053.png" />|<img width="1920" alt="Multi-Courbes" src="pics/Screenshot%202026-09-30%20173132.png" />|<img width="1920" alt="Capteur Individuel" src="pics/Screenshot%202026-09-30%20173211.png" />|
|:---:|:---:|:---:|:---:|
| **Accueil / Landing Page** | **Fast Insights (Multi-Capteurs)** | **Supervision Multi-Courbes** | **Capteur Individuel DEV-001** |

|<img width="1920" alt="Générateur IA" src="pics/Screenshot%202026-09-30%20173239.png" />|<img width="1920" alt="Registre Rapports" src="pics/Screenshot%202026-09-30%20173309.png" />|<img width="1920" alt="Rapport PDF" src="pics/Screenshot%202026-09-30%20173340.png" />|<img width="1920" alt="Historique" src="pics/Screenshot%202026-09-30%20173428.png" />|
|:---:|:---:|:---:|:---:|
| **Générateur & Planificateur IA** | **Registre des Rapports Scellés** | **Rapport PDF Certifié Généré par IA** | **Évolution Temporelle des Mesures** |

|<img width="1920" alt="Matrice HACCP" src="pics/Screenshot%202026-09-30%20173450.png" />|<img width="1920" alt="Vélocité Alertes" src="pics/Screenshot%202026-09-30%20173552.png" />|<img width="1920" alt="Top Équipements" src="pics/Screenshot%202026-09-30%20173927.png" />|<img width="1920" alt="Thèmes Visuels" src="pics/Screenshot%202026-09-30%20174017.png" />|
|:---:|:---:|:---:|:---:|
| **Matrice de Conformité HACCP** | **Vélocité Horaire des Alertes** | **Top Équipements & Croissance** | **Sélecteur de Thèmes (20+ Thèmes)** |

|<img width="1920" alt="Gestion Appareils" src="pics/Screenshot%202026-09-30%20174057.png" />|<img width="1920" alt="Paramètres & Seuils" src="pics/Screenshot%202026-09-30%20174132.png" />|<img width="1920" alt="Gestion RBAC" src="pics/Screenshot%202026-09-30%20174235.png" />|<img width="1920" alt="Mon Compte" src="pics/Screenshot%202026-09-30%20174313.png" />|
|:---:|:---:|:---:|:---:|
| **Gestion des Passerelles & Capteurs** | **Paramétrage des Seuils & Langues** | **Gestion des Comptes RBAC & Sessions** | **Espace Utilisateur & Profil** |

---

# Démonstration Vidéo (Demo Video)

Une démonstration complète du fonctionnement en temps réel, de la génération de rapports certifiés et de la gestion des alertes est disponible :

* **Fichier vidéo local :** [`demo.mp4`](demo.mp4)

---

# Stack Technologique

### Matériel & IoT (Hardware) :
* **Microcontrôleur :** ESP32 NodeMCU / WROOM-32 (Wi-Fi 802.11 b/g/n, double cœur 240 MHz).
* **Capteurs :** DHT11 / DHT22 (Mesure de température et d'humidité relative).
* **Synchronisation Temporelle :** Client NTP intégré (`pool.ntp.org`, UTC+1) générant des clés d'idempotence uniques (`eventId`) pour garantir l'absence de doublons.
* **Résilience Réseau :** Mécanisme Last Will & Testament (LWT) publiant automatiquement un statut `OFFLINE` en cas de coupure physique d'alimentation.

### Courtier de Messages (Message Broker) :
* **Broker :** EMQX MQTT Broker (Broker MQTT distribué à haut débit supportant les protocoles TCP 1883 et WebSocket 8083).
* **Architecture des Topics :** Routage hiérarchique avec wildcards (`therafrozen/devices/+/metrics`, `therafrozen/devices/+/status`).
* **Niveau de Service :** MQTT QoS 1 avec persistance de statut via messages retenus (`retained: true`).

### Backend & Microservices :
* **Moteur d'Exécution :** Node.js & Express.js.
* **Persistance des Données :** MongoDB (Mongoose ODM) avec indexation temporelle pour requêtes analytiques accélérées.
* **Diffusion en Temps Réel :** Socket.io pour la transmission bi-directionnelle instantanée des métriques et des statuts matériels.
* **Watchdog Matériel :** Service de surveillance automatique marquant hors-ligne les équipements inactifs depuis plus de 25 secondes.
* **Intelligence Artificielle :** OpenAI API pour la rédaction automatisée des audits certifiés de traçabilité.
* **Notification d'Urgence :** API Resend pour l'expédition instantanée de courriels d'alerte critique.
* **Génération Documentaire :** Moteur PDFKit pour l'édition de fiches d'audit scellées conformes aux normes réglementaires.

### Frontend & Interface Utilisateur :
* **Framework :** React avec TypeScript et Vite.
* **Design & Styles :** Tailwind CSS, composants scifi personnalisés et moteur de thèmes dynamiques (20+ palettes).
* **Visualisation Graphique :** Recharts pour les graphiques d'évolution, multi-courbes et jauges de conformité en donut.
* **Animation & Ergonomie :** Framer Motion pour les micro-interactions et transitions de pages.
* **Internationalisation :** Context i18n avec basculement bilingue complet (Français / Anglais).

### Déploiement & Infrastructure (DevOps) :
* **Conteneurisation :** Docker & Docker Compose orchestrant backend, frontend, worker et simulateur IoT.
* **Reverse Proxy :** Nginx avec terminaison TLS/SSL (HTTPS) et compression Gzip.
* **Intégration & Déploiement Continus :** GitHub Actions CI/CD avec validation de syntaxe, compilation TypeScript et redémarrage automatisé des conteneurs.

---

# Licence

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

---

