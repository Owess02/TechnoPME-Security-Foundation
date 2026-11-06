\# Rules of Engagement — TechnoPME Security Foundation



\## 1. Objectif



Ce document définit les règles, limites et conditions d’exécution des tests

de sécurité réalisés dans le cadre du projet TechnoPME Security Foundation.



\## 2. Périmètre autorisé



Tous les tests sont réalisés exclusivement sur les systèmes suivants :



\- TPME-FW01 (pfSense)

\- TPME-WS01 (Windows 10)

\- TPME-SRV01 (Ubuntu Server)

\- TPME-MON01 (Wazuh)

\- TPME-VULN01 (OpenVAS/Greenbone)

\- TPME-KALI01 (Kali Linux)

\- Réseaux VMware isolés : VMnet2 à VMnet5



\## 3. Interdictions



\- Aucun scan vers Internet.

\- Aucun scan vers le réseau domestique.

\- Aucun scan vers des systèmes tiers.

\- Aucune attaque sans autorisation écrite explicite.

\- Aucune destruction de données.

\- Aucune exfiltration de données réelles.

\- Aucune publication de secrets, mots de passe, clés ou identifiants.



\## 4. Méthodes autorisées



\- Découverte réseau.

\- Scan de ports.

\- Énumération de services.

\- Analyse de vulnérabilités.

\- Tests d’accès inter-VLAN.

\- Tests de configuration SSH/SMB/RDP.

\- Simulation de mouvement latéral contrôlé.

\- Tests de détection Wazuh.



\## 5. Niveau d’agressivité



\- Scan non destructif.

\- Pas d’exploit destructeur.

\- Pas de denial of service.

\- Pas de modification non documentée.

\- Toute action doit être journalisée.



\## 6. Conditions d’arrêt



Les tests doivent être interrompus immédiatement si :



\- Un système devient instable.

\- Une action dépasse le périmètre autorisé.

\- Une donnée sensible est exposée.

\- Une configuration critique est modifiée sans validation.

\- Un risque de propagation est identifié.



\## 7. Validation



Chaque test doit produire :



\- Une preuve (capture, log, export).

\- Un résultat attendu.

\- Un résultat obtenu.

\- Une conclusion.

\- Une action corrective si nécessaire.

