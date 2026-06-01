# Mapping OWASP MASVS

## FIND-001: API Key exposée
- **Catégorie OWASP**: MASVS-STORAGE
- **Référence spécifique**: V2.1
- **Justification**: Les clés API sont des données sensibles qui doivent être stockées de manière sécurisée et non en clair dans les assets.

## FIND-002: Communication HTTP en clair
- **Catégorie OWASP**: MASVS-NETWORK
- **Référence spécifique**: V5.1
- **Justification**: Les données en transit doivent être protégées par TLS. HTTP expose les données aux attaques Man-in-the-Middle.

## FIND-003: Backup Android activé
- **Catégorie OWASP**: MASVS-STORAGE
- **Référence spécifique**: V2.8
- **Justification**: Les sauvegardes automatiques peuvent exposer des données sensibles si elles ne sont pas correctement protégées.

## FIND-004: Logs de débogage actifs
- **Catégorie OWASP**: MASVS-CODE
- **Référence spécifique**: V7.6
- **Justification**: Les logs de débogage facilitent la rétro-ingénierie et peuvent exposer des informations sensibles.

## FIND-005: Absence de certificate pinning
- **Catégorie OWASP**: MASVS-NETWORK
- **Référence spécifique**: V5.4
- **Justification**: Sans certificate pinning, un certificat frauduleux peut être utilisé pour intercepter les communications HTTPS.
