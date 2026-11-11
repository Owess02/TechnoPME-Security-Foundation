# Déploiement du poste Windows 10 — TechnoPME

## 1. Objectif

Valider les services réseau (DHCP, DNS, routage) sur la zone LAN_USERS avec un premier poste client.

## 2. Poste client

- VM Windows 10 existante, réutilisée comme poste utilisateur (au lieu d'un déploiement neuf)
- Réseau : LAN_USERS (VMnet2) uniquement. Carte NAT désactivée pour forcer le passage par pfSense.

## 3. Services configurés sur pfSense

| Service | Zone | Paramètres |
|---|---|---|
| DHCP | LAN_USERS | 192.168.10.50 à 192.168.10.150, bail 8 h, domaine technopme.local |
| DHCP | LAN_GUESTS | 192.168.30.50 à 192.168.30.100, bail 30 min |
| DNS Resolver | MGMT_ADMIN, LAN_USERS, LAN_GUESTS, Localhost | Sortie par WAN, enregistrement DHCP activé |

## 4. Règle temporaire

Règle « Pass any » sur LAN_USERS (source LAN_USERS subnets) pour les tests.
À supprimer et remplacer en Phase 4.

## 5. Tests réalisés

- Attribution DHCP : 192.168.10.50, passerelle 192.168.10.1
- Ping de la passerelle
- Résolution DNS (nslookup)
- Test HTTPS (port 443)
- Analyse Wireshark : DHCP (DORA), DNS, ICMP, TLS

## 6. Preuves

- CAP-PF-011 à CAP-PF-013b : `01-evidence/03-pfsense/`
- CAP-WIN-006 à CAP-WIN-013 et fichiers .pcapng : `01-evidence/04-windows/`