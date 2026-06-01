# Rapport Final — Analyse de Sécurité Mobile
## Lab 8 — BeVigil & Yaazhini

| Champ | Valeur |
|---|---|
| **Date** | 2026-06-01 |
| **Analyste** | Nisrine Gorfti |
| **Établissement** | EMSI |
| **Cible** | Application mobile pédagogique |
| **Outils** | BeVigil, Yaazhini |

---

## 1. Résumé exécutif

L'analyse passive réalisée sur l'application mobile autorisée a permis d'identifier **5 constats de sécurité**, dont **2 de sévérité haute**. Les vulnérabilités détectées sont représentatives des problèmes les plus fréquents selon OWASP MASVS.

---

## 2. Constats

### 🔴 Sévérité Haute

**FIND-001 — API Key exposée**
- **Outil** : BeVigil
- **Description** : Une clé API a été détectée dans les assets publiquement accessibles.
- **Référence OWASP** : MASVS-STORAGE-1 (V2.1)
- **Recommandation** : Révoquer la clé, utiliser Android Keystore.

**FIND-002 — Communication HTTP en clair**
- **Outil** : BeVigil
- **Description** : Des endpoints utilisent HTTP non chiffré.
- **Référence OWASP** : MASVS-NETWORK-1 (V5.1)
- **Recommandation** : Forcer HTTPS, définir `usesCleartextTraffic=false`.

### 🟡 Sévérité Moyenne

**FIND-003 — Backup Android activé**
- **Outil** : Yaazhini
- **Description** : `android:allowBackup="true"` dans le manifeste.
- **Référence OWASP** : MASVS-STORAGE-2 (V2.8)
- **Recommandation** : Définir `android:allowBackup="false"`.

### 🔵 Sévérité Faible

**FIND-004 — Logs de débogage**
- **Outil** : Yaazhini
- **Recommandation** : Supprimer ou désactiver via ProGuard/R8.

**FIND-005 — Absence de certificate pinning**
- **Outil** : Yaazhini
- **Recommandation** : Implémenter via Network Security Configuration.

---

## 3. Tableau récapitulatif

| ID | Description | Sévérité | OWASP | Statut |
|---|---|---|---|---|
| FIND-001 | API Key exposée | 🔴 Haute | MASVS-STORAGE-1 | À corriger |
| FIND-002 | HTTP en clair | 🔴 Haute | MASVS-NETWORK-1 | À corriger |
| FIND-003 | Backup activé | 🟡 Moyenne | MASVS-STORAGE-2 | À corriger |
| FIND-004 | Logs debug | 🔵 Faible | MASVS-CODE | À corriger |
| FIND-005 | Pas de pinning | 🔵 Faible | MASVS-NETWORK-2 | Accepté |

---

## 4. Conclusion

Aucune exploitation n'a été réalisée. L'analyse s'est déroulée dans le respect strict du périmètre autorisé.

---

*Nisrine Gorfti — EMSI — 2026-06-01 — Usage pédagogique uniquement*
