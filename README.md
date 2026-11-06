# TechnoPME Security Foundation

Projet de laboratoire visant à concevoir, sécuriser, superviser et exploiter
l’infrastructure réseau initiale d’une PME fictive : TechnoPME.

## Objectifs

- Concevoir une architecture réseau segmentée.
- Déployer et administrer un pare-feu pfSense.
- Mettre en place DHCP, DNS et contrôle des flux.
- Durcir un poste Windows 10 et un serveur Ubuntu.
- Mettre en place une supervision avec Wazuh.
- Gérer les vulnérabilités avec OpenVAS/Greenbone.
- Mettre en place des sauvegardes et tester les restaurations.
- Documenter les risques, contrôles et décisions de sécurité.

## Périmètre

Ce projet est réalisé exclusivement dans un environnement de laboratoire isolé :
VMware Workstation, VirtualBox et GNS3.

Aucun test offensif, scan ou exploitation n’est réalisé contre des systèmes
tiers sans autorisation écrite explicite.

## Architecture cible

- pfSense : pare-feu, routeur, DHCP, DNS, segmentation.
- Windows 10 : poste utilisateur durci.
- Ubuntu Server : serveur Linux durci.
- Wazuh : supervision et collecte de journaux.
- OpenVAS/Greenbone : gestion des vulnérabilités.
- GNS3 : pratique des concepts réseau CCNA.

## Livrables

- Schéma réseau et plan d’adressage.
- Matrice de flux et règles pfSense.
- Preuves de durcissement Windows/Linux.
- Tableaux de bord Wazuh.
- Rapports de vulnérabilités avant/après.
- Sauvegardes et tests de restauration.
- Registre des risques et rapport final.