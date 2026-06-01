# Lab 8 — Analyse de posture et exposition d'applications mobiles avec BeVigil et Yaazhini

**Auteure : Nisrine Gorfti**
**Institution : EMSI**
**Date : 2026-06-01**

## Objectif
Réaliser une analyse de sécurité passive sur une application mobile en utilisant BeVigil (analyse externe) et Yaazhini (analyse statique SAST), puis documenter les constats selon le référentiel OWASP MASVS.

## Outils utilisés
- **BeVigil** : Analyse de la surface d'attaque externe (endpoints, secrets, permissions)
- **Yaazhini** : Analyse statique locale du code décompilé
- **PowerShell** : Automatisation et traçabilité

## Structure du projet
```
lab-mobile-security/
├── 00-scope/
│   └── scope.md              # Périmètre et autorisation
├── 01-bevigil/
│   └── bevigil_notes.md      # Résultats BeVigil
├── 02-yaazhini/
│   └── yaazhini_notes.md     # Résultats Yaazhini
├── 03-triage/
│   ├── triage.csv            # Tableau de priorisation
│   └── owasp_mapping.md      # Mapping OWASP MASVS
├── 04-report/
│   └── rapport_final.md      # Rapport complet
├── analyse_info.txt           # Métadonnées de l'analyse
├── checklist_fin.md           # Checklist de clôture
└── commands.log               # Journal des commandes
```
**<img width="523" height="306" alt="image" src="https://github.com/user-attachments/assets/41a23584-520b-4d7a-94ff-9c48d9fc62c4" />
**<img width="1600" height="807" alt="image" src="https://github.com/user-attachments/assets/ae232733-a037-40aa-9779-f396032e866c" />


<img width="1122" height="757" alt="image" src="https://github.com/user-attachments/assets/4757b018-b6a9-445a-89eb-6332be2a3865" />

<img width="1600" height="840" alt="image" src="https://github.com/user-attachments/assets/e66ae153-c476-4388-b9ae-a7b18f6be919" />


## Constats majeurs
| ID | Description | Sévérité | OWASP |
|---|---|---|---|
| FIND-001 | API Key exposée | 🔴 Haute | MASVS-STORAGE-1 |
| FIND-002 | Communication HTTP en clair | 🔴 Haute | MASVS-NETWORK-1 |
| FIND-003 | Backup Android activé | 🟡 Moyenne | MASVS-STORAGE-2 |
| FIND-004 | Logs de débogage actifs | 🔵 Faible | MASVS-CODE |
| FIND-005 | Absence de certificate pinning | 🔵 Faible | MASVS-NETWORK-2 |
<img width="521" height="263" alt="image" src="https://github.com/user-attachments/assets/c6e95dca-7050-4725-b3a8-9a74fdbe540c" />
