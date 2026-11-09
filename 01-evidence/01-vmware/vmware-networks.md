# Réseaux VMware — TechnoPME

## 1. Objectif

Créer les réseaux virtuels isolés nécessaires à la segmentation de
l’infrastructure TechnoPME.

## 2. Réseaux créés

| VMnet | Nom logique | Type | Sous-réseau | Masque | DHCP VMware | Rôle |
|---|---|---|---|---|---|---|
| VMnet2 | LAN_Users | Host-only | 192.168.10.0/24 | 255.255.255.0 | Désactivé | Postes utilisateurs |
| VMnet3 | LAN_Servers | Host-only | 192.168.20.0/24 | 255.255.255.0 | Désactivé | Serveurs Windows/Linux |
| VMnet4 | LAN_Guests | Host-only | 192.168.30.0/24 | 255.255.255.0 | Désactivé | Invités |
| VMnet5 | MGMT_Admin | Host-only | 192.168.100.0/24 | 255.255.255.0 | Désactivé | Administration |

## 3. Justification

La segmentation vise à :

- Limiter le mouvement latéral.
- Isoler les zones sensibles.
- Contrôler les communications inter-zones.
- Préparer la supervision et la réponse aux incidents.
- Réduire la surface d’attaque.

## 4. Décisions techniques

- Le DHCP VMware est désactivé sur toutes les zones.
- pfSense sera le seul service d’attribution d’adresses IP.
- Windows Server sera placé dans LAN_Servers avec une IP statique.
- Les communications inter-zones seront contrôlées par pfSense.

## 5. Preuves

- CAP-VM-001 : Virtual Network Editor global.
- CAP-VM-002 : VMnet2 LAN_Users.
- CAP-VM-003 : VMnet3 LAN_Servers.
- CAP-VM-004 : VMnet4 LAN_Guests.
- CAP-VM-005 : VMnet5 MGMT_Admin.
- CAP-VM-006 : Vue globale finale.