# Installation de pfSense — TechnoPME

## 1. Objectif

Déployer le pare-feu central de TechnoPME.

## 2. Paramètres VM

- Nom : TPME-FW01
- Version : pfSense CE 2.9.0-RELEASE (amd64)
- vCPU : 2
- RAM : 4 Go
- Disque : 20 Go
- 5 cartes réseau e1000

## 3. Interfaces

| Interface pfSense | Carte | MAC | Réseau VMware | Rôle |
|---|---|---|---|---|
| WAN | em0 | 00:0c:29:09:c3:84 | NAT (VMnet8) | Accès sortant |
| LAN (MGMT_ADMIN) | em1 | 00:0c:29:09:c3:8e | VMnet5 | Administration |
| OPT1 (LAN_SERVERS) | em2 | 00:0c:29:09:c3:98 | VMnet3 | Serveurs |
| OPT2 (LAN_GUESTS) | em3 | 00:0c:29:09:c3:a2 | VMnet4 | Invités |
| OPT3 (LAN_USERS) | em4 | 00:0c:29:09:c3:ac | VMnet2 | Utilisateurs |

## 4. Adressage

| Interface | IP | Masque |
|---|---|---|
| WAN | 192.168.230.133 (DHCP) | 255.255.255.0 |
| MGMT_ADMIN | 192.168.100.1 | 255.255.255.0 |
| LAN_SERVERS | 192.168.20.1 | 255.255.255.0 |
| LAN_GUESTS | 192.168.30.1 | 255.255.255.0 |
| LAN_USERS | 192.168.10.1 | 255.255.255.0 |

## 5. Accès WebGUI

- URL : https://192.168.100.1
- Accès depuis MGMT_ADMIN (adaptateur VMnet5 de l'hôte : 192.168.100.10).
- Mot de passe administrateur changé.

## 6. Incident rencontré

Le ping vers 192.168.100.1 échouait. `tcpdump` sur em1 ne voyait aucun trafic.
Le fichier .vmx a montré que ethernet1 était sur VMnet2 au lieu de VMnet5.
Correction : réaffectation des cartes dans VMware (em1 sur MGMT_admin, em4 sur LAN_Users).

## 7. Preuves

- CAP-PF-006 : Dashboard avec les cinq interfaces.
- CAP-PF-008 : changement du mot de passe.
- CAP-PF-010 : commit Git.