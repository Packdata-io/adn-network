# Transparence client léger

```
[ Poste utilisateur ] --opt-in--> [ Client léger : vérifie un profil public ]
        |
        v  (hash SHA-256 + signature, jamais de brut)
[ ADN Network : scelle, chaîne, horodate ]
        |
        +--> fraîcheur partagée à tous
        +--> crédits d'extraction au contributeur
```

Packdata Lite, le client léger gratuit, peut, uniquement si l'utilisateur l'active explicitement, vérifier en arrière-plan des profils professionnels publics et renvoyer les confirmations au réseau ADN — sur le principe des applications participatives (à la manière de Waze — marque Google, citée pour expliquer, sans affiliation).

Ce qui quitte la machine : des signaux de confirmation pseudonymisés uniquement. Aucune donnée privée, aucune donnée client, aucun enregistrement brut — seuls des hash circulent (voir WHITEPAPER.md § Privacy by design).

Contrôle : l'utilisateur peut suspendre ou couper la vérification à tout moment depuis les réglages. Packdata agit comme sous-traitant (art. 28 RGPD dans l'UE, régimes équivalents ailleurs). Rien n'est partagé au réseau commun sans opt-in explicite.

Client sobre par conception : requêtes fragmentées de 40 Ko maximum, cadence réglable par l'utilisateur, impact nul sur forfait et batterie aux réglages standards.

Ciblage par segment : l'utilisateur choisit le segment que son client vérifie en priorité (ex : l'immobilier). Le réseau nettoie ce segment en premier, si bien que les données sont déjà fraîches le jour où il prend sa licence. Chacun prépare son propre terrain.

Offre équipe : chaque collaborateur équipé du client léger contribue à la fraîcheur du segment de son entreprise. Mise en place soumise à l'information préalable des équipes et au respect des règles internes — l'activation reste individuelle et réversible à tout moment.

Incitation : chaque contribution scellée rapporte des crédits d'extraction. Extraire coûte davantage que contribuer : les taux et plafonds sont affichés dans le logiciel et peuvent évoluer avec préavis. Contribuer ouvre l'extraction — plus vous rafraîchissez, plus vous pouvez extraire. Comptabilité signée et horodatée, vérifiable par tout tiers.

Le client léger contribue à son rythme : c'est la porte d'entrée du réseau. La licence donne un accès complet à l'ADN Network : recherches, croisements et extractions inclus selon le forfait.

Licences plafonnées à 1 500 par an, avec immatriculation B2B vérifiée. Le plafond garantit que chaque nœud est une entreprise identifiée et maintient la performance du réseau.

## Note d'architecture

Client natif compilé en Rust (sécurité mémoire sans GC, isolation stricte, empreinte minimale), moteur d'ingestion asynchrone multi-thread, transport mesh pair-à-pair temps réel avec traversée NAT (libp2p, WebRTC) : aucune ferme de serveurs centrale, aucun point unique de défaillance.

Intégrité : chaque contribution est scellée (empreinte SHA-256 + signature ECDSA P-256 + chaînage append-only) et vérifiable par tout tiers muni de la clé publique. Une empreinte quotidienne de la chaîne est ancrée publiquement via OpenTimestamps.

Confidentialité : transport chiffré en permanence (TLS 1.3 / DTLS, obligatoire en WebRTC). Les hash qui circulent sont pseudonymes, jamais d'enregistrements bruts sur le réseau.

Accès : entrée filtrée par clés API signées. Séparation des privilèges : la contribution n'ouvre aucun droit d'extraction au-delà des crédits gagnés. Le code source reste privé ; les propriétés ci-dessus sont auditables sur demande sous accord de confidentialité.

## Vérification continue, orchestrée par l'humain

Packdata Lite fonctionne seul en arrière-plan — disponible sur Windows, Mac, iOS, Android et Chrome. À vous de choisir : vérification humaine, pilotée, ou accélérée par votre propre agent IA. Dans tous les cas, vos moteurs privés de méta-recherche recoupent tout observable public — pages, API et métriques publiques — en parallèle, en quelques secondes et sans traçage — l'IP de votre poste n'est jamais exposée aux sources. Rien ne quitte votre poste sans opt-in : seuls des hash signés rejoignent l'ADN Network. Chaque preuve est chaînée, horodatée, vérifiable par tout tiers — scellée selon le protocole Cerveau Numérique. Vos sentinelles veillent en continu, vous ne validez que les cas sensibles. Crédits et droits d'extraction non monétaires, taux affichés dans le logiciel, 1500 licences par an à plafond contractuel, jeton éventuel à l'étude encadré MiCA sans promesse de valeur. Inclus dans Packdata Lite, natif dans le logiciel. Nos agents autonomes restent en R&D.

```
┌─ POSTE CLIENT — tous OS (périmètre de confiance) ────┐
│ Windows · Mac · iOS · Android · Chrome               │
│ Lite seul · humain / piloté / agent optionnel        │
│ Vous : mission, règles, validation cas sensibles     │
│ Agent local : votre clé, filtres, cadence réglable   │
│ Données brutes : NE QUITTENT JAMAIS le poste         │
│ Mobile : veille allégée (règles stores) · Desktop /  │
│ Chrome : veille complète                             │
└───────────────┬──────────────────────────────────────┘
                │ requêtes fragmentées ≤40 Ko, TLS 1.3
                │ opt-in explicite, coupure à tout moment
                ▼
┌─ MOTEURS PRIVÉS (opérés par vous, sans traçage) ─────┐
│ Tout observable public : pages, API, métriques       │
│ publiques — en parallèle, secondes, sans traçage     │
│ Vues par les sources : IP du moteur, jamais IP poste │
│ Aucun log requête, rate-limit + backoff              │
└───────────────┬──────────────────────────────────────┘
                │ candidats : URL + extrait + date constat
                ▼
┌─ VÉRIFICATEUR (déterministe, pas le LLM) ────────────┐
│ Croisement ≥2 sources concordantes                   │
│ trouvée → vérifiée : sources + date + agent tracé    │
└───────────────┬──────────────────────────────────────┘
                │ vérifiée seulement
                ▼
┌─ SCELLEMENT — Cerveau Numérique (preuve, pas brut) ──┐
│ SHA-256 (intégrité) + ECDSA P-256 (signature)        │
│ chaînage append-only + horodatage (OpenTimestamps)   │
│ Hash + métadonnées seuls, pseudonymes                │
└───────────────┬──────────────────────────────────────┘
                ▼
┌─ ADN NETWORK ────────────────────────────────────────┐
│ Mémoire partagée, fraîcheur mutualisée               │
│ Vérifiable par tout tiers muni de la clé publique    │
└───────────────┬──────────────────────────────────────┘
                │ veille permanente (règles versionnées)
                ▼
┌─ SENTINELLES → VALIDÉE ──────────────────────────────┐
│ Vous ou seuil de confiance (+ Supervisor/Compliance  │
│ pour actions sensibles). Corrections = resserrement  │
│ des règles. Jamais d'infaillibilité promise.         │
└──────────────────────────────────────────────────────┘
```
