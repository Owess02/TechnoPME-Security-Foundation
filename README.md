# TechnoPME Security Foundation

**Conception, sécurisation, supervision et exploitation d'une infrastructure informatique de PME.**

## 1. Présentation du projet

**TechnoPME Security Foundation** est un projet de laboratoire visant à concevoir, déployer, sécuriser et superviser l'infrastructure informatique d'une PME fictive : **TechnoPME**.

L'objectif est de mettre en pratique les compétences en administration systèmes et réseaux, sécurité des infrastructures, gestion des vulnérabilités, supervision et réponse aux incidents.

Le projet repose sur une infrastructure virtualisée et isolée permettant de reproduire un environnement professionnel réaliste.

## 2. Objectifs du projet

Les principaux objectifs sont les suivants :

- Concevoir une architecture réseau segmentée et sécurisée.
- Déployer et administrer un pare-feu pfSense.
- Mettre en place les services DHCP et DNS.
- Contrôler et filtrer les flux réseau.
- Durcir les systèmes Windows et Linux.
- Déployer une solution centralisée de supervision avec Wazuh.
- Identifier et gérer les vulnérabilités avec OpenVAS/Greenbone.
- Mettre en place une stratégie de sauvegarde et tester les restaurations.
- Documenter les risques, les mesures de sécurité et les décisions techniques.
- Réaliser des tests de sécurité contrôlés et documenter les résultats.

## 3. Périmètre et environnement technique

Le projet est réalisé exclusivement dans un environnement de laboratoire isolé.

### Environnement de virtualisation et de simulation

- VMware Workstation
- VirtualBox
- GNS3

### Infrastructure cible

| Composant | Rôle |
|---|---|
| pfSense | Pare-feu, routage, DHCP, DNS et segmentation réseau |
| Windows 10 | Poste utilisateur à durcir |
| Ubuntu Server | Serveur Linux à sécuriser et administrer |
| Wazuh | Supervision de sécurité et collecte centralisée des journaux |
| OpenVAS / Greenbone | Analyse et gestion des vulnérabilités |
| GNS3 | Simulation et pratique des concepts réseau CCNA |

## 4. Architecture cible

L'architecture repose sur une infrastructure réseau segmentée, protégée par pfSense et composée de plusieurs systèmes ayant des rôles distincts.

Les différents composants seront progressivement intégrés et configurés afin de permettre :

- L'isolation des différents segments réseau.
- Le contrôle des communications entre les machines.
- La centralisation des journaux de sécurité.
- La détection des vulnérabilités.
- La surveillance de l'infrastructure.
- La protection des postes et serveurs.

*Le schéma réseau détaillé et le plan d'adressage seront ajoutés au fur et à mesure de la réalisation du laboratoire.*

## 5. Phases de réalisation

### Phase 1 — Conception de l'infrastructure

- [ ] Définir les besoins de la PME fictive.
- [ ] Concevoir l'architecture réseau.
- [ ] Définir les segments réseau et les VLAN.
- [ ] Élaborer le plan d'adressage IP.
- [ ] Définir la matrice des flux réseau.
- [ ] Documenter les choix d'architecture.

### Phase 2 — Déploiement des services réseau

- [ ] Installer et configurer pfSense.
- [ ] Configurer les interfaces réseau.
- [ ] Mettre en place le routage.
- [ ] Configurer les services DHCP et DNS.
- [ ] Définir les règles de filtrage.
- [ ] Tester la segmentation et les communications réseau.

### Phase 3 — Administration et durcissement des systèmes

- [ ] Installer Windows 10.
- [ ] Appliquer les mesures de durcissement Windows.
- [ ] Installer Ubuntu Server.
- [ ] Configurer les services nécessaires.
- [ ] Appliquer les mesures de durcissement Linux.
- [ ] Vérifier les configurations et les permissions.
- [ ] Documenter les mesures appliquées.

### Phase 4 — Supervision et journalisation

- [ ] Déployer Wazuh.
- [ ] Connecter les agents Windows et Linux.
- [ ] Centraliser les journaux de sécurité.
- [ ] Configurer les règles et alertes.
- [ ] Créer les tableaux de bord.
- [ ] Vérifier la remontée des événements.

### Phase 5 — Gestion des vulnérabilités

- [ ] Déployer OpenVAS / Greenbone.
- [ ] Configurer les cibles de laboratoire.
- [ ] Réaliser les analyses de vulnérabilités.
- [ ] Identifier et classer les vulnérabilités.
- [ ] Définir les mesures correctives.
- [ ] Appliquer les corrections.
- [ ] Effectuer des analyses de vérification.
- [ ] Comparer les résultats avant et après correction.

### Phase 6 — Tests de sécurité contrôlés

Tous les tests seront réalisés uniquement sur les systèmes du laboratoire et dans le respect des règles d'autorisation définies.

**Préparation et autorisation**

- [ ] Rédiger les Rules of Engagement (RoE).
- [ ] Définir le périmètre des tests.
- [ ] Définir les cas de test.
- [ ] Identifier les systèmes concernés.
- [ ] Définir les conditions d'arrêt des tests.

**Exécution des tests**

- [ ] Réaliser la découverte réseau.
- [ ] Scanner les services exposés.
- [ ] Tester les accès inter-VLAN.
- [ ] Tester les accès SSH, SMB et RDP.
- [ ] Identifier les failles potentielles.
- [ ] Évaluer les mesures de protection.

**Correction et validation**

- [ ] Corriger les vulnérabilités identifiées.
- [ ] Reproduire les tests après correction.
- [ ] Vérifier l'efficacité des mesures appliquées.
- [ ] Documenter les résultats avant/après.

### Phase 7 — Sauvegarde et restauration

- [ ] Définir une stratégie de sauvegarde.
- [ ] Identifier les données et configurations critiques.
- [ ] Mettre en place les sauvegardes.
- [ ] Tester les procédures de restauration.
- [ ] Documenter les résultats des tests.

### Phase 8 — Documentation et bilan final

- [ ] Finaliser le schéma réseau.
- [ ] Documenter les configurations techniques.
- [ ] Consolider les preuves de durcissement.
- [ ] Archiver les rapports de vulnérabilités.
- [ ] Constituer le registre des risques.
- [ ] Rédiger le rapport final du laboratoire.

## 6. Livrables attendus

À la fin du projet, les livrables comprendront :

| Domaine | Livrable |
|---|---|
| Architecture | Schéma réseau et plan d'adressage IP |
| Réseau | Matrice des flux et règles pfSense |
| Systèmes | Preuves de durcissement Windows et Linux |
| Supervision | Tableaux de bord et alertes Wazuh |
| Vulnérabilités | Rapports OpenVAS avant/après correction |
| Tests de sécurité | Cas de test, résultats et preuves |
| Continuité | Sauvegardes et tests de restauration |
| Gouvernance | Registre des risques et rapport final |

## 7. Sécurité et règles d'utilisation

Ce laboratoire est destiné exclusivement à l'apprentissage, à l'expérimentation et à la validation de compétences en cybersécurité.

Les règles suivantes sont appliquées :

- Tous les tests sont réalisés dans un environnement isolé.
- Aucun scan ou test offensif n'est effectué contre des systèmes tiers sans autorisation écrite explicite.
- Les configurations sensibles et les identifiants ne doivent pas être publiés dans le dépôt.
- Les résultats des tests sont documentés et conservés à des fins pédagogiques.
- Toute modification importante de l'infrastructure doit être vérifiée et documentée.

## 8. Organisation du dépôt

L'organisation des fichiers sera progressivement structurée comme suit :

```text
TechnoPME-Security-Foundation/
│
├── README.md
│
├── docs/
│   ├── architecture/
│   ├── network/
│   ├── security/
│   └── reports/
│
├── configurations/
│   ├── pfsense/
│   ├── windows/
│   └── ubuntu/
│
├── wazuh/
│   ├── configuration/
│   └── alerts/
│
├── vulnerability-management/
│   ├── scans/
│   └── remediation/
│
├── penetration-testing/
│   ├── rules-of-engagement/
│   ├── test-cases/
│   └── evidence/
│
├── backup-recovery/
│
└── evidence/
    ├── screenshots/
    └── diagrams/
```

*Cette arborescence représente l'organisation cible et sera adaptée à mesure que les composants seront réalisés.*

## 9. Statut du projet

**Projet en cours de réalisation.**

Les phases seront documentées progressivement avec les configurations, les preuves techniques, les résultats des tests et les mesures correctives appliquées.

---

**TechnoPME Security Foundation**  
*Infrastructure Security | Network Administration | System Hardening | Security Monitoring | Vulnerability Management*