# Inventaire des actifs — TechnoPME

## 1. Objectif

Identifier les actifs présents dans l’environnement, leur rôle, leur criticité
et les mesures de protection associées.

## 2. Actifs

| ID | Actif | Type | Zone | IP prévue | Rôle | Criticité | Propriétaire |
|---|---|---|---|---|---|---|---|
| AST-001 | TPME-FW01 | Pare-feu | Toutes zones | 192.168.x.1 | Routage, filtrage, DHCP, DNS | Critique | IT |
| AST-002 | TPME-WS01 | Poste utilisateur | LAN_Users | DHCP | Travail quotidien | Moyen | Utilisateur |
| AST-003 | TPME-SRV01 | Serveur Linux | LAN_Servers | 192.168.20.10 | Services internes | Élevé | IT |
| AST-007 | TPME-DC01 | Serveur Windows | LAN_Servers | 192.168.20.10 | Contrôleur de domaine futur | Critique | IT |
| AST-004 | TPME-MON01 | Supervision | MGMT_Admin | 192.168.100.10 | Wazuh | Critique | SOC |
| AST-005 | TPME-VULN01 | Analyse | MGMT_Admin | 192.168.100.20 | OpenVAS | Élevé | SOC |
| AST-006 | TPME-KALI01 | Poste de test | MGMT_Admin | DHCP | Tests contrôlés | Moyen | SOC |

## 3. Données sensibles

| Type de donnée | Emplacement | Criticité | Protection |
|---|---|---|---|
| Documents RH | C:\TechnoPME\RH_Confidentiel | Élevée | Sauvegarde, accès restreint |
| Configuration pfSense | Export XML | Critique | Sauvegarde, accès restreint |
| Journaux de sécurité | Wazuh | Élevée | Accès restreint, rétention |
| Clés SSH | Ubuntu Server | Critique | Permissions strictes, non publication |

## 4. Principes

- Chaque actif doit être identifié.
- Chaque actif doit avoir un propriétaire.
- Chaque actif doit avoir un niveau de criticité.
- Chaque actif critique doit être sauvegardé.
- Chaque actif doit être surveillé.