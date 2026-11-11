# Règles de pare-feu — TechnoPME

## 1. Objectif

Contrôler les flux entre les zones avec une politique de refus par défaut.

## 2. Principes

- Refus par défaut (aucune règle « allow any » active).
- Blocages explicites journalisés.
- Les règles sont évaluées de haut en bas, la première correspondance gagne.
- L'accès au WebGUI est garanti par la règle Anti-Lockout.

## 3. Alias

| Nom | Type | Valeur |
|---|---|---|
| NET_PRIVATE | Network(s) | 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16 |
| ADMIN_HOSTS | Host(s) | 192.168.100.10 |
| SERVERS_RESERVED | Network(s) | 192.168.20.0/24 |
| WEB_OUTBOUND | Port(s) | 80, 443 |
| DNS_OUTBOUND | Port(s) | 53 |
| MGMT_PORTS | Port(s) | 22, 443 |

## 4. Règles LAN_USERS

| ID | Action | Protocole | Source | Destination | Port | Log |
|---|---|---|---|---|---|---|
| FW-001 | Pass | TCP/UDP | LAN_USERS subnets | LAN_USERS address | DNS_OUTBOUND | Non |
| FW-003 | Block | Any | LAN_USERS subnets | LAN_SERVERS subnets | Any | Oui |
| FW-004 | Block | Any | LAN_USERS subnets | LAN_GUESTS subnets | Any | Oui |
| FW-005 | Block | Any | LAN_USERS subnets | MGMT_ADMIN subnets | Any | Oui |
| FW-002 | Pass | TCP | LAN_USERS subnets | ! NET_PRIVATE | WEB_OUTBOUND | Non |

## 5. Règles LAN_GUESTS

| ID | Action | Protocole | Source | Destination | Port | Log |
|---|---|---|---|---|---|---|
| FW-006 | Pass | TCP/UDP | LAN_GUESTS subnets | LAN_GUESTS address | DNS_OUTBOUND | Non |
| FW-008 | Block | Any | LAN_GUESTS subnets | LAN_USERS subnets | Any | Oui |
| FW-009 | Block | Any | LAN_GUESTS subnets | LAN_SERVERS subnets | Any | Oui |
| FW-010 | Block | Any | LAN_GUESTS subnets | MGMT_ADMIN subnets | Any | Oui |
| FW-007 | Pass | TCP | LAN_GUESTS subnets | ! NET_PRIVATE | WEB_OUTBOUND | Non |

## 6. Règles MGMT_ADMIN

| ID | Action | Protocole | Source | Destination | Port | Log |
|---|---|---|---|---|---|---|
| (auto) | Pass | Any | Any | MGMT_ADMIN address | 443, 80 | Non |
| FW-011 | Pass | TCP | ADMIN_HOSTS | This Firewall | 443 | Oui |
| FW-012 | Pass | TCP | ADMIN_HOSTS | SERVERS_RESERVED | 22 | Oui |
| FW-013 | Block | Any | MGMT_ADMIN subnets | Any | Any | Oui |

Les règles « Default allow LAN to any » (IPv4 et IPv6) sont désactivées.

## 7. Tests réalisés (depuis le poste Windows 10, 192.168.10.50)

| Test | Résultat attendu | Résultat | Règle |
|---|---|---|---|
| nslookup google.com | Autorisé | OK | FW-001 |
| HTTPS vers example.com | Autorisé | OK | FW-002 |
| ping 192.168.20.1 | Bloqué | 100 % de perte | FW-003 |
| ping 192.168.30.1 | Bloqué | 100 % de perte | FW-004 |
| TCP 443 vers 192.168.100.1 | Bloqué | False | FW-005 |

## 8. Preuves

- CAP-PF-015 à CAP-PF-025 dans `01-evidence/03-pfsense/`.
- Non réalisées pour l'instant : CAP-PF-026 (Packet Capture) et CAP-PF-027 (Wireshark filtré).