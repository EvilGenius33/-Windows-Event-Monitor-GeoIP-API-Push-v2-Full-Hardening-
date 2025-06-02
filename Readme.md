🎯 Description
Ce script PowerShell surveille en temps réel les événements de sécurité Windows critiques, les enrichit par une géolocalisation IP (dans le cas de connexions RDP), et envoie automatiquement les alertes vers une API distante (serveur SIEM ou SOC personnalisé).

⚙️ Fonctionnalités principales
✅ Surveillance live des événements critiques de sécurité (Security.evtx)

🌍 Résolution GeoIP automatique sur connexions RDP entrantes

🛰️ Push JSON vers une API distante pour traitement centralisé

💾 Journalisation locale complète sur le Bureau de l'utilisateur

🔐 Surveillance avancée de l'activité utilisateur, processus, privilèges, tâches planifiées, clés de registre, accès fichiers partagés, etc.

🔍 Événements Windows couverts (exemples)
Connexions réussies ou échouées

Création / suppression / modification de comptes

Tentatives d’élévation de privilèges

Insertion de périphériques USB

Exécution de nouveaux processus

Création de tâches planifiées

Suppression de Shadow Copies

Nettoyage de logs

Détection de malware

🔗 API à configurer
Remplacer http://<YOUR_API_ENDPOINT>:5000/api/log par l’URL de votre serveur d’agrégation

Le push JSON contient : timestamp, eventID, message (+ géolocalisation si applicable)

📦 Prérequis
PowerShell 5.1 ou plus

Connexion Internet pour la géolocalisation IP

Un endpoint API accessible (ou un serveur local Flask/Python si en test)

📌 Remarques
Ce script n’utilise aucune dépendance externe.

Il peut être intégré dans une stratégie de durcissement ou déployé à l’échelle.

Les alertes peuvent être couplées à un système de notification secondaire.

