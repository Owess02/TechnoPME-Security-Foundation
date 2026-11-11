# Registre des problèmes

| ID | Date | Composant | Problème | Cause probable | Solution | Statut |
|---|---|---|---|---|---|---|
| ISS-001 | 2026-11-06 | Projet | Structure initiale à organiser | Absence de modèle de projet | Création d’une arborescence standardisée | Résolu |
| ISS-002 | 2026-11-09 | VMware | DHCP VMware actif par défaut | Configuration initiale | Désactivation manuelle | Résolu |
| ISS-003 | 2026-11-10 | pfSense | Aucune communication hôte/VM vers pfSense (ping KO) | Carte em1 reliée à VMnet2 au lieu de VMnet5 (vérifié dans le .vmx) | Réaffectation des cartes réseau dans VMware | Résolu |
| ISS-004 | 2026-11-11 | DNS Resolver | Erreur à la sauvegarde : Localhost ou All requis | Interface Localhost désélectionnée alors que pfSense utilise son propre résolveur | Réactivation de Localhost dans Network Interfaces | Résolu |
| ISS-005 | 2026-11-11 | pfSense | Règles de pare-feu mal configurées (inversion « ! » sur FW-001 et FW-006, FW-003 en Pass, destination de FW-012 et FW-013 intervertie) | Erreurs de saisie dans le formulaire des règles | Correction règle par règle et relecture des listes | Résolu |
| ISS-006 | 2026-11-11 | Windows 10 | Test de navigation non concluant : carte NAT de la VM contournait pfSense | Deuxième carte réseau en NAT | Suppression de la carte NAT | Résolu |