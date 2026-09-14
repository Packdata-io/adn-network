# Certificat ADN — exemple de sortie logiciel (2026-09-14)

Exemple illustratif généré par le logiciel Packdata, scellé dans
l'ADN Network. Identité masquée pour l'illustration ; chiffres et
sources authentiques. Le certificat remis au client porte les
valeurs constatées complètes, vérifiables par empreinte.

## Identité constatée
- Sujet : •••• •••• — Dirigeant, grand groupe
- Nature : profil public, constaté via navigateur
- Date du constat : 2026-09-14 12:12:29 (UTC : 2026-09-14T10:12:44Z)

## Données publiques constatées
- Abonnés (public) : 2 600
- Fiabilité : 14/20 (profil confirmé +6 · URL = notre URL +4 · compteur présent +3 · date +1)
- E-mails publics : ••••••@••••••.fr (liste — N adresses génériques possibles, non nominatives)
- Adresses publiques : siège •••• · 9•••• — registre open-data (liste — N adresses possibles)

## Sources publiques — preuves opposables
| Nature | Lien public | Consulté le |
|---|---|---|
| Profil public (URL masquée) | linkedin.com/in/•••••••• | 2026-09-14 |
| Indexation moteur (preuve publique) | google.com/search?q="••••" "••••" | 2026-09-14 |
| Open-data entreprise (officiel) | recherche-entreprises.api.gouv.fr — SIREN 410 001 ••• | 2026-09-14 |
| (3 sources minimum — lignes ajoutées selon les sources) | | |

## Empreinte cryptographique & horodatage
- Certificat ID : b606d9ef-dec2-4d88-863b-b••••7e9e5
- SHA-256 : 2035f050…68cc16ff61 (tronqué pour l'illustration)
- Signature ECDSA P-256 : vérifiable par un tiers (clé publique partageable)
- Signature HMAC : scellé d'intégrité
- Chaînage ADN Network : chaque bloc pointe le précédent (bloc 4022d8…addc04944)
- Horodatage UTC : 2026-09-14T10:12:44Z — instant de la demande, figé

## Historique
Chaque demande fige un état daté. La suite des certificats fait
l'historique, à la hausse comme à la baisse (ex. 2 400 → 2 600
abonnés, ou 2 400 → 2 102 en cas de perte), sans qu'aucun état
passé ne soit modifiable.

## Attestation
Les informations ci-dessus ont été constatées sur des sources
publiques librement accessibles à tous, à la date indiquée. Aucune
donnée privée, ni session authentifiée, n'a été utilisée.

## Provenance du générateur
Généré par le code source scellé : `search_engine/market_report.py`
(générateur) + App Native Packdata — cf. MANIFEST.sha256 (30
empreintes) et dépôt e-Soleau n° DSO2026033766 du 13/09/2026.

## Doctrine
Scellé · intégrité vérifiable. Sur la chaîne ne circulent que des
empreintes, jamais la donnée brute. Mécanisme décrit dans
WHITEPAPER.md (inchangé, v1.2).
