# Journal quotidien

## 2026-11-06

### Objectifs du jour
- Finaliser le README.
- Finaliser la roadmap.
- Créer les règles d’engagement.
- Créer l’inventaire des actifs.
- Créer le registre des risques.
- Créer les politiques de base.

### Réalisations
- Structure du dépôt créée.
- README finalisé.
- Roadmap finalisée.
- Politiques de cadrage créées.

### Difficultés
- Aucune difficulté majeure à ce stade.

### Prochaines étapes
- Créer les réseaux VMware isolés.
- Déployer pfSense.
- Configurer les interfaces réseau.

## 2026-11-09 — Phase 1

### Objectifs
- Créer les réseaux VMware isolés.
- Désactiver le DHCP VMware.
- Documenter les sous-réseaux.
- Préparer l’intégration de Windows Server.

### Réalisations
- Création de VMnet2 à VMnet5.
- Configuration des sous-réseaux.
- Désactivation du DHCP VMware.
- Documentation des réseaux.

### Difficultés
- Aucune difficulté majeure.

### Prochaines étapes
- Déployer pfSense.
- Configurer les interfaces.
- Attribuer les IP.
- Préparer Windows Server.

## 2026-11-10 — Phase 2

### Réalisations
- VM TPME-FW01 installée, 5 interfaces assignées et activées.
- WebGUI accessible depuis l'hôte via MGMT_ADMIN.
- Assistant de configuration terminé.

### Difficultés
- Ping KO : em1 reliée au mauvais VMnet. Diagnostic par tcpdump puis lecture du .vmx.

### Prochaines étapes
- DHCP sur LAN_USERS et LAN_GUESTS, DNS Resolver, règles de pare-feu.

## 2026-11-11 — Phase 3

### Réalisations
- DHCP activé sur LAN_USERS et LAN_GUESTS.
- DNS Resolver configuré.
- VM Windows 10 rattachée à LAN_USERS, IP 192.168.10.50 obtenue par DHCP.
- Tests ping, DNS, HTTPS validés.
- Captures Wireshark : DHCP, DNS, ICMP, HTTPS.

### Difficultés
- Erreur DNS Resolver (Localhost obligatoire).

### Prochaines étapes
- Phase 4 : alias, règles de pare-feu, journalisation, tests de blocage entre zones.
- Supprimer la règle temporaire de LAN_USERS.