# Notes BeVigil

## Projet
Nom: LAB-BEGINNER-20260601

## Résultats
- **Assets détectés** : Clé API exposée dans les assets publics
- **Endpoints trouvés** : 3 endpoints HTTP non sécurisés
- **URLs identifiées** : 7 URLs dont 2 en HTTP clair
- **Technologies** : Retrofit, OkHttp, Firebase

## Constats
| ID | Type | Description | Sévérité |
|---|---|---|---|
| FIND-001 | Secret | API Key exposée dans assets | 🔴 Haute |
| FIND-002 | Réseau | Endpoint HTTP non chiffré | 🔴 Haute |

## Export
Fichier: bevigil_export.json (à placer dans ce dossier)
