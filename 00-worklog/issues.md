# Registre des problèmes

| ID | Date | Composant | Problème | Cause probable | Solution | Statut |
|---|---|---|---|---|---|---|
| ISS-001 | 2026-11-06 | Projet | Structure initiale à organiser | Absence de modèle de projet | Création d’une arborescence standardisée | Résolu |
| ISS-002 | 2026-11-09 | VMware | DHCP VMware actif par défaut | Configuration initiale | Désactivation manuelle | Résolu |
| ISS-003 | 2026-11-10 | pfSense | Aucune communication hôte/VM vers pfSense (ping KO) | Carte em1 reliée à VMnet2 au lieu de VMnet5 (vérifié dans le .vmx) | Réaffectation des cartes réseau dans VMware | Résolu |