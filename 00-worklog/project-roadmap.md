# Roadmap — TechnoPME Security Foundation

## Phase 0 — Cadrage

- [x] Créer la structure du projet
- [x] Initialiser Git
- [x] Finaliser le README
- [x] Finaliser la roadmap
- [ ] Créer les Rules of Engagement
- [ ] Créer l’inventaire des actifs
- [ ] Créer le registre des risques
- [ ] Créer le journal des changements
- [ ] Créer le journal quotidien

## Phase 1 — Conception réseau

- [ ] Définir les besoins de TechnoPME
- [ ] Définir les zones réseau
- [ ] Créer le plan d’adressage
- [ ] Créer la matrice des flux
- [ ] Créer le schéma réseau
- [ ] Documenter les choix d’architecture

## Phase 2 — Déploiement pfSense

- [ ] Créer les réseaux VMware
- [ ] Créer la VM pfSense
- [ ] Installer pfSense
- [ ] Assigner les interfaces
- [ ] Configurer les adresses IP
- [ ] Accéder au WebGUI
- [ ] Sécuriser l’accès administratif

## Phase 3 — DHCP, DNS et connectivité

- [ ] Déployer Windows Server
- [ ] Configurer l’adresse IP statique
- [ ] Préparer l’intégration à Active Directory
- [ ] Documenter le rôle futur du serveur
- [ ] Activer DHCP LAN_Users
- [ ] Activer DHCP LAN_Guests
- [ ] Configurer DNS Resolver
- [ ] Tester l’attribution d’IP
- [ ] Tester la résolution DNS
- [ ] Tester la connectivité

## Phase 4 — Pare-feu et segmentation

- [ ] Créer les alias
- [ ] Créer les règles de filtrage
- [ ] Activer la journalisation
- [ ] Tester les blocages inter-zones
- [ ] Tester les accès autorisés
- [ ] Documenter la matrice de flux

## Phase 5 — Windows 10

- [ ] Créer la VM Windows 10
- [ ] Installer Windows
- [ ] Capturer l’état initial
- [ ] Créer les comptes
- [ ] Appliquer la politique de mots de passe
- [ ] Durcir le système
- [ ] Créer un script d’audit PowerShell
- [ ] Sauvegarder et restaurer

## Phase 6 — Ubuntu Server

- [ ] Créer la VM Ubuntu Server
- [ ] Configurer une IP statique
- [ ] Durcir SSH
- [ ] Configurer UFW
- [ ] Configurer Fail2ban
- [ ] Configurer Auditd
- [ ] Créer un script d’audit Bash
- [ ] Sauvegarder et restaurer

## Phase 7 — Supervision SOC

- [ ] Créer la VM Wazuh
- [ ] Installer Wazuh
- [ ] Déployer les agents Windows/Linux
- [ ] Centraliser les journaux
- [ ] Créer des règles personnalisées
- [ ] Créer des tableaux de bord
- [ ] Tester les alertes

## Phase 8 — Gestion des vulnérabilités

- [ ] Créer la VM OpenVAS
- [ ] Installer OpenVAS/Greenbone
- [ ] Définir les cibles
- [ ] Réaliser un scan initial
- [ ] Identifier les vulnérabilités
- [ ] Appliquer les corrections
- [ ] Réaliser un scan final
- [ ] Comparer les résultats

## Phase 9 — Tests de sécurité contrôlés

- [ ] Valider les Rules of Engagement
- [ ] Définir les cas de test
- [ ] Réaliser la découverte réseau
- [ ] Scanner les services
- [ ] Tester les accès inter-VLAN
- [ ] Tester SSH, SMB et RDP
- [ ] Identifier les failles
- [ ] Corriger les failles
- [ ] Re-tester
- [ ] Documenter avant/après

## Phase 10 — Réponse aux incidents

- [ ] Définir les scénarios d’incident
- [ ] Rédiger les playbooks
- [ ] Simuler un incident
- [ ] Analyser les alertes
- [ ] Confiner
- [ ] Éradiquer
- [ ] Restaurer
- [ ] Rédiger un rapport d’incident

## Phase 11 — Sauvegarde et continuité

- [ ] Définir la stratégie de sauvegarde
- [ ] Sauvegarder Windows
- [ ] Sauvegarder Ubuntu
- [ ] Sauvegarder pfSense
- [ ] Tester les restaurations
- [ ] Vérifier l’intégrité
- [ ] Définir RPO/RTO

## Phase 12 — Rapport final

- [ ] Finaliser le schéma réseau
- [ ] Consolider les preuves
- [ ] Rédiger le rapport final
- [ ] Rédiger le résumé exécutif en anglais
- [ ] Créer la démo vidéo
- [ ] Publier le projet final