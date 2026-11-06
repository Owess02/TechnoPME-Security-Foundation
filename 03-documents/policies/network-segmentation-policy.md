# Politique de segmentation réseau — TechnoPME

## 1. Objectif

Définir les zones réseau, leurs rôles et les règles de communication autorisées.

## 2. Zones

| Zone | Réseau | Rôle | Accès |
|---|---|---|---|
| LAN_Users | 192.168.10.0/24 | Postes utilisateurs | Internet limité |
| LAN_Servers | 192.168.20.0/24 | Serveurs internes | Accès contrôlé |
| LAN_Guests | 192.168.30.0/24 | Invités | Internet uniquement |
| MGMT_Admin | 192.168.100.0/24 | Administration | Accès restreint |

## 3. Principes

- Aucun flux non justifié.
- Refus par défaut.
- Journalisation des règles sensibles.
- Isolation des invités.
- Protection du plan d’administration.
- Contrôle des communications inter-zones.

## 4. Règles de base

| Source | Destination | Action | Justification |
|---|---|---|---|
| LAN_Users | WAN | Autorisé | DNS, HTTP, HTTPS |
| LAN_Users | LAN_Servers | Refusé | Aucun besoin métier validé |
| LAN_Users | LAN_Guests | Refusé | Isolation des invités |
| LAN_Guests | LAN_Users | Refusé | Isolation des invités |
| LAN_Guests | WAN | Autorisé | Accès Internet limité |
| WAN | Zones internes | Refusé | Aucun service exposé |
| MGMT_Admin | pfSense | Autorisé | Administration |
| MGMT_Admin | Ubuntu SSH | Autorisé | Administration |