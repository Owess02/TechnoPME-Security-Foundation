# Journal des changements

| Date | Composant | Modification | Justification | Test de validation | Preuve |
|---|---|---|---|---|---|
| 2026-11-06 | Projet | Initialisation du dépôt | Mise en place du cadre de travail | Structure créée | `README.md` |
| 2026-11-06 | Documentation | Création des politiques de cadrage | Définir le périmètre et les règles | Fichiers créés | `03-documents/policies/` |
| 2026-11-09 | Architecture | Ajout de Windows Server au périmètre | Préparer les services d’entreprise | Mise à jour du plan d’adressage | `README.md`, `asset-inventory.md` |
| 2026-11-09 | VMware | Création de VMnet2 à VMnet5 | Segmentation TechnoPME | Vérification Virtual Network Editor | `01-evidence/01-vmware/` |
| 2026-11-10 | pfSense | Déploiement de TPME-FW01 | Mise en place du pare-feu central | 5 interfaces actives avec IP | `01-evidence/03-pfsense/` |
| 2026-11-11 | pfSense | Activation DHCP (LAN_USERS, LAN_GUESTS) et DNS Resolver | Fournir les services réseau de base | Tests DHCP/DNS | `01-evidence/03-pfsense/` |
| 2026-11-11 | pfSense | Règle temporaire Pass any sur LAN_USERS | Permettre les tests de connectivité | Tests ping/DNS/HTTPS | `01-evidence/03-pfsense/` |
| 2026-11-11 | Windows 10 | Rattachement de la VM existante à LAN_USERS | Premier poste client | Tests connectivité et Wireshark | `01-evidence/04-windows/` |
| 2026-11-11 | pfSense | Alias et règles de pare-feu (LAN_USERS, LAN_GUESTS, MGMT_ADMIN) | Segmentation et refus par défaut | Tests de blocage et d'autorisation | `01-evidence/03-pfsense/` |
| 2026-11-11 | pfSense | Désactivation des règles « Default allow LAN to any » | Appliquer le refus par défaut | Accès WebGUI vérifié | `01-evidence/03-pfsense/` |