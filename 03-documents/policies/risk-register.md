# Registre des risques — TechnoPME

## 1. Objectif

Identifier les risques majeurs, évaluer leur impact et documenter les mesures
de réduction mises en place.

## 2. Échelle de risque

| Niveau | Description |
|---|---|
| Faible | Impact limité, contrôle suffisant |
| Moyen | Impact modéré, contrôle partiel |
| Élevé | Impact important, contrôle insuffisant |
| Critique | Impact majeur, contrôle absent ou défaillant |

## 3. Registre

| ID | Risque | Scénario | Impact | Probabilité | Risque initial | Contrôles | Risque résiduel |
|---|---|---|---|---|---|---|---|
| RSK-001 | Rançongiciel | Ouverture d’une pièce jointe malveillante | Élevé | Moyenne | Élevé | Defender, mises à jour, sauvegarde | Moyen |
| RSK-002 | Compromission de compte | Mot de passe faible ou réutilisé | Élevé | Moyenne | Élevé | Longueur minimale, verrouillage, comptes séparés | Moyen |
| RSK-003 | Mouvement latéral | Poste compromis tente de joindre les serveurs | Élevé | Moyenne | Élevé | Segmentation, règles pfSense | Faible à moyen |
| RSK-004 | Perte de données | Suppression accidentelle ou panne disque | Élevé | Moyenne | Élevé | Sauvegarde testée | Moyen |
| RSK-005 | Exposition administrative | Interface pfSense accessible depuis une zone utilisateur | Critique | Faible | Élevé | Zone MGMT isolée, règles restrictives | Faible |
| RSK-006 | Vulnérabilité non corrigée | Service obsolète ou mal configuré | Élevé | Moyenne | Élevé | OpenVAS, mises à jour, durcissement | Moyen |

## 4. Suivi

Chaque risque doit être revu après :
- Mise en place d’un contrôle.
- Correction d’une vulnérabilité.
- Test de sécurité.
- Incident simulé.
- Changement d’architecture.