# Notes Yaazhini

## Analyse
Fichier APK analysé: application_pedagogique.apk
Date d'analyse: 2026-06-01

## Résultats
- **Permissions risquées** : READ_EXTERNAL_STORAGE, WRITE_EXTERNAL_STORAGE
- **Vulnérabilités détectées** : allowBackup=true, debuggable=true
- **Score de sécurité** : 42/100

## Constats
| ID | Type | Description | Sévérité |
|---|---|---|---|
| FIND-003 | Manifest | android:allowBackup="true" | 🟡 Moyenne |
| FIND-004 | Manifest | android:debuggable="true" | 🔵 Faible |
| FIND-005 | Réseau | Absence de certificate pinning | 🔵 Faible |

## Export
Rapport Yaazhini: yaazhini_report.html (à placer dans ce dossier)
