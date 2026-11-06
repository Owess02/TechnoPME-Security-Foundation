# TechnoPME Security Foundation

**Conception, sécurisation, supervision, tests de sécurité et réponse aux incidents au sein d’une infrastructure informatique de PME.**

**Auteur : AKPA SALOMON OWESS**  
**Domaines : Infrastructure Security | Network Administration | System Hardening | Security Monitoring | Vulnerability Management | Incident Response**

---

## 1. Présentation du projet

**TechnoPME Security Foundation** est un projet de laboratoire visant à concevoir, déployer, sécuriser, superviser et exploiter l’infrastructure informatique d’une PME fictive : **TechnoPME**.

Le projet reproduit les fondamentaux d’un environnement professionnel : segmentation réseau, administration d’un pare-feu, durcissement des systèmes, centralisation des journaux, détection des menaces, gestion des vulnérabilités, sauvegarde, réponse aux incidents et documentation des décisions de sécurité.

L’infrastructure est déployée dans un environnement virtualisé isolé, permettant de travailler dans des conditions proches d’une entreprise, tout en respectant un périmètre strictement contrôlé.

## 2. Objectifs du projet

- Concevoir une architecture réseau segmentée et sécurisée.
- Déployer et administrer un pare-feu pfSense.
- Mettre en place les services DHCP, DNS et le routage inter-zones.
- Définir et appliquer une politique de contrôle des flux réseau.
- Durcir les systèmes Windows et Linux.
- Centraliser les journaux de sécurité avec Wazuh.
- Mettre en place des règles de détection et des tableaux de bord SOC.
- Identifier, classer et corriger les vulnérabilités avec OpenVAS/Greenbone.
- Réaliser des tests de sécurité contrôlés et documenter les résultats.
- Mettre en place une procédure de réponse aux incidents.
- Mettre en œuvre une stratégie de sauvegarde et valider les restaurations.
- Documenter les risques, les contrôles, les exceptions et les décisions techniques.

## 3. Périmètre et environnement technique

Le projet est réalisé exclusivement dans un environnement de laboratoire isolé.

### Environnement de virtualisation et de simulation

- VMware Workstation
- VirtualBox
- GNS3

### Infrastructure cible

| Composant | Rôle |
|---|---|
| pfSense | Pare-feu, routage, DHCP, DNS, segmentation et journalisation |
| Windows 10 | Poste utilisateur durci |
| Ubuntu Server | Serveur Linux durci et administré |
| Wazuh | Supervision, collecte de journaux, détection et réponse |
| OpenVAS / Greenbone | Analyse et gestion des vulnérabilités |
| GNS3 | Simulation et pratique des concepts réseau CCNA |
| Kali Linux | Poste d’analyse et de tests contrôlés |

## 4. Architecture cible

L’architecture repose sur une segmentation réseau stricte, protégée par pfSense et supervisée par Wazuh.

| Zone | Réseau | Rôle |
|---|---|---|
| LAN_Users | 192.168.10.0/24 | Postes utilisateurs |
| LAN_Servers | 192.168.20.0/24 | Serveurs et services internes |
| LAN_Guests | 192.168.30.0/24 | Accès invités isolé |
| MGMT_Admin | 192.168.100.0/24 | Administration et supervision |

Les principes appliqués sont :

- Segmentation par zones.
- Contrôle des flux inter-zones.
- Principe du moindre privilège.
- Journalisation centralisée.
- Détection des anomalies.
- Réponse structurée aux incidents.
- Sauvegarde et capacité de restauration.

Le schéma réseau détaillé, le plan d’adressage et la matrice des flux seront ajoutés progressivement dans le dépôt.

## 5. Phases de réalisation

### Phase 1 — Cadrage et conception

- [ ] Définir les besoins de la PME fictive.
- [ ] Définir les actifs, les zones et les niveaux de criticité.
- [ ] Concevoir l’architecture réseau.
- [ ] Définir les segments et les VLAN.
- [ ] Élaborer le plan d’adressage IP.
- [ ] Définir la matrice des flux réseau.
- [ ] Documenter les choix d’architecture.
- [ ] Créer les règles d’engagement pour les tests de sécurité.

### Phase 2 — Déploiement réseau

- [ ] Créer les réseaux isolés dans VMware.
- [ ] Déployer pfSense.
- [ ] Configurer les interfaces réseau.
- [ ] Mettre en place le routage.
- [ ] Configurer DHCP et DNS.
- [ ] Créer les alias et règles de pare-feu.
- [ ] Activer la journalisation.
- [ ] Tester la segmentation et les communications.

### Phase 3 — Administration et durcissement

- [ ] Déployer Windows 10.
- [ ] Appliquer les mesures de durcissement Windows.
- [ ] Déployer Ubuntu Server.
- [ ] Sécuriser SSH, UFW, Fail2ban et Auditd.
- [ ] Appliquer le principe du moindre privilège.
- [ ] Réduire la surface d’attaque.
- [ ] Automatiser les contrôles avec PowerShell et Bash.
- [ ] Documenter les configurations avant/après.

### Phase 4 — Supervision SOC

- [ ] Déployer Wazuh.
- [ ] Connecter les agents Windows et Linux.
- [ ] Centraliser les journaux de sécurité.
- [ ] Configurer les règles de détection.
- [ ] Créer des tableaux de bord SOC.
- [ ] Mettre en place des alertes.
- [ ] Réaliser des requêtes de threat hunting.
- [ ] Valider la remontée des événements.

### Phase 5 — Gestion des vulnérabilités

- [ ] Déployer OpenVAS / Greenbone.
- [ ] Définir les cibles autorisées.
- [ ] Réaliser les analyses initiales.
- [ ] Identifier et classer les vulnérabilités.
- [ ] Définir les mesures correctives.
- [ ] Appliquer les corrections.
- [ ] Effectuer les analyses de vérification.
- [ ] Comparer les résultats avant/après.

### Phase 6 — Tests de sécurité contrôlés

Tous les tests sont réalisés uniquement sur les systèmes du laboratoire, dans le respect des règles d’engagement définies.

#### Préparation

- [ ] Valider les Rules of Engagement.
- [ ] Définir le périmètre des tests.
- [ ] Définir les cas de test.
- [ ] Identifier les systèmes concernés.
- [ ] Définir les conditions d’arrêt.

#### Exécution

- [ ] Réaliser la découverte réseau.
- [ ] Scanner les services exposés.
- [ ] Tester les accès inter-VLAN.
- [ ] Tester les accès SSH, SMB et RDP.
- [ ] Identifier les failles potentielles.
- [ ] Évaluer l’efficacité des contrôles.

#### Correction et validation

- [ ] Corriger les vulnérabilités identifiées.
- [ ] Reproduire les tests après correction.
- [ ] Vérifier l’efficacité des mesures appliquées.
- [ ] Documenter les résultats avant/après.

### Phase 7 — Réponse aux incidents

- [ ] Définir les scénarios d’incident.
- [ ] Rédiger les playbooks de réponse.
- [ ] Simuler un incident de compromission de poste.
- [ ] Simuler un incident de mouvement latéral.
- [ ] Simuler un incident d’exfiltration de données.
- [ ] Analyser les alertes et les journaux.
- [ ] Appliquer les mesures de confinement.
- [ ] Appliquer les mesures d’éradication.
- [ ] Restaurer les services.
- [ ] Rédiger un rapport d’incident.

### Phase 8 — Sauvegarde et continuité

- [ ] Définir la stratégie de sauvegarde.
- [ ] Identifier les données et configurations critiques.
- [ ] Mettre en place les sauvegardes.
- [ ] Tester les procédures de restauration.
- [ ] Vérifier l’intégrité des données restaurées.
- [ ] Définir les objectifs RPO et RTO.
- [ ] Documenter les résultats des tests.

### Phase 9 — Documentation et bilan final

- [ ] Finaliser le schéma réseau.
- [ ] Documenter les configurations techniques.
- [ ] Consolider les preuves de durcissement.
- [ ] Archiver les rapports de vulnérabilités.
- [ ] Consolider les rapports d’incidents.
- [ ] Constituer le registre des risques.
- [ ] Rédiger le rapport final.
- [ ] Rédiger le résumé exécutif en anglais.

## 6. Environnement SOC

L’environnement SOC est construit autour de Wazuh et repose sur les fonctions suivantes :

- Collecte centralisée des journaux.
- Détection d’événements de sécurité.
- Création de règles personnalisées.
- Tableaux de bord de supervision.
- Analyse des alertes.
- Threat hunting.
- Surveillance de l’intégrité des fichiers.
- Détection des vulnérabilités.
- Support à la réponse aux incidents.

Les scénarios d’incident couvriront notamment :

- Compromission d’un poste utilisateur.
- Tentative de mouvement latéral.
- Élévation de privilèges.
- Exécution suspecte.
- Exfiltration de données.
- Tentative d’accès non autorisé.
- Modification non autorisée de fichiers critiques.

La réponse aux incidents suivra le cycle NIST : préparation, détection et analyse, confinement, éradication, récupération et retour d’expérience.

## 7. Livrables attendus

| Domaine | Livrable |
|---|---|
| Architecture | Schéma réseau, plan d’adressage, matrice de flux |
| Réseau | Règles pfSense, journalisation, tests de segmentation |
| Systèmes | Preuves de durcissement Windows et Linux |
| Supervision | Tableaux de bord, alertes et requêtes Wazuh |
| Vulnérabilités | Rapports OpenVAS avant/après correction |
| Tests de sécurité | Rules of Engagement, cas de test, preuves et rapport |
| Réponse aux incidents | Playbooks, chronologies, mesures et rapports |
| Continuité | Sauvegardes, tests de restauration, RPO/RTO |
| Gouvernance | Registre des risques, exceptions et changements |
| Documentation | Rapport final et résumé exécutif en anglais |

## 8. Sécurité et règles d’utilisation

Ce laboratoire est destiné exclusivement à l’expérimentation, à la validation de compétences et à la démonstration de capacités techniques.

Les règles suivantes sont appliquées :

- Tous les tests sont réalisés dans un environnement isolé.
- Aucun scan ou test offensif n’est effectué contre des systèmes tiers sans autorisation écrite explicite.
- Les configurations sensibles, mots de passe, clés privées et identifiants ne sont pas publiés dans le dépôt.
- Les résultats des tests sont documentés et conservés à des fins de traçabilité.
- Toute modification importante est validée, testée et documentée.

## 9. Organisation du dépôt

```text
TechnoPME-Security-Foundation/
│
├── README.md
│
├── 00-worklog/
│   ├── change-log.md
│   ├── daily-notes.md
│   ├── issues.md
│   └── project-roadmap.md
│
├── 01-evidence/
│   ├── 01-vmware/
│   ├── 02-network-design/
│   ├── 03-pfsense/
│   ├── 04-windows/
│   ├── 05-linux/
│   ├── 06-monitoring/
│   ├── 07-vulnerabilities/
│   ├── 08-backup/
│   ├── 09-vpn/
│   └── 10-final-report/
│
├── 02-scripts/
│   ├── bash/
│   ├── powershell/
│   └── python/
│
├── 03-documents/
│   ├── policies/
│   ├── procedures/
│   └── reports/
│
├── 04-architecture/
│   ├── infrastructure/
│   ├── ip-addressing/
│   └── network-diagrams/
│
├── 05-soc/
│   ├── detection-rules/
│   ├── dashboards/
│   ├── incident-response/
│   └── threat-hunting/
│
├── 06-penetration-testing/
│   ├── rules-of-engagement/
│   ├── test-cases/
│   ├── evidence/
│   └── reports/
│
├── 07-vulnerability-management/
│   ├── scans/
│   └── remediation/
│
├── 08-backup-recovery/
│
└── 09-resources/
    ├── glossary.md
    ├── references.md
    └── tools-and-technologies.md
```

## 10. Statut du projet

**Projet en cours de réalisation.**

Les phases sont documentées progressivement avec les configurations, preuves techniques, résultats de tests, mesures correctives et analyses d’incidents.

---

**TechnoPME Security Foundation**  
*Infrastructure Security | Network Administration | System Hardening | Security Monitoring | Vulnerability Management | Incident Response*