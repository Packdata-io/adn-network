# Packdata — White Paper : ADN Network (snapshot 2026-09-21)

> Snapshot Markdown du White Paper publié sur https://packdata.io/white-paper.html.

**WHITE PAPER · V1.0 · 2026**

# La data B2B peer-to-peer, gratuite pour le contributeur

« L'effet Waze appliqué à la data B2B. »

Réseau contributif et vérifiable : le code sera public sur [GitHub](https://github.com/Packdata-io).

ADN Network — la data P2P, libre et ouverte

Deux rôles, un même réseau : les **entreprises consomment** une data B2B fraîche, les **contributeurs la rafraîchissent** et sont récompensés. Un modèle de **preuve de contribution**, bâti sur des données publiques professionnelles et respectueux du RGPD.

**RÉSUMÉ**

## Le problème : une donnée qui vieillit dès l'achat

La plupart des bases B2B sont des **fichiers figés** : justes le jour de l'achat, périmés quelques mois plus tard. Une base perd en moyenne près de **30 % de fraîcheur par an** — e-mails qui rebondissent, interlocuteurs qui ont changé de poste, temps perdu.

L'ADN Network répond autrement : une donnée **vivante**, qui se rafraîchit pendant qu'on l'utilise, et dont chaque mise à jour est **tracée, scellée et récompensée**.

**LE RÉSEAU**

## Un réseau vivant, pas un fichier livré une fois

La fraîcheur de chacun profite à tous : plus le réseau est utilisé, plus la data est à jour.

La donnée se rafraîchit au fil de l'usage du réseau. Vous ne prospectez jamais sur une base périmée.

Chaque donnée est contrôlée. Vous parlez à de vraies personnes, à jour, sur 110 pays.

Confidentiel par conception : vos requêtes et vos données ne quittent pas votre poste. Sur le réseau ne circulent que des empreintes, jamais la donnée brute.

**DEUX RÔLES, UN MÊME RÉSEAU**

## Les entreprises consomment, les contributeurs rafraîchissent

Un cercle vertueux : ceux qui utilisent la data et ceux qui la tiennent à jour, reliés par le même réseau, l'ADN Network.

ENTREPRISE — Sous licence : utilise **Packdata Lite** (gratuit) + **Packdata Desktop** (licence ADN Network) pour prospecter et contacter des décideurs sur une data fraîche. Accès à toute la data B2B + IA + envoi. Extraction illimitée selon forfait. L'usage rafraîchit aussi le réseau.

Les employés de l'entreprise : utilisent **Packdata Lite** (gratuit, PC/Mac/iOS/Android/Chrome), l'app qui alimente le réseau en mises à jour et rapporte des ADN. Augmentent les extractions de l'entreprise et réduisent le prix de sa mise à jour annuelle.

CONTRIBUTEUR — Particulier : utilise **Packdata Lite** (gratuit) : l'app interroge aléatoirement des données publiques pour les confirmer ou les rafraîchir dans l'ADN Network. Chaque contribution est signée et horodatée. Gagne des droits d'extraction à chaque contribution, cumule des crédits d'extraction (année 2). Peut revendre ses crédits aux entreprises.

**L'effet Waze appliqué à la data B2B :** chaque **Packdata Lite** valide et rafraîchit les données publiques en arrière-plan — plus il y a d'utilisateurs, plus la base devient précise et s'auto-nettoie en temps réel.

Waze est une marque déposée de Google LLC, citée ici à titre purement illustratif.

Réseau contributif et vérifiable : le code sera public sur [GitHub](https://github.com/Packdata-io).

**CERTIFICATION**

## Chaque donnée peut être scellée et horodatée

Une information relevée sur une **source publique** peut être certifiée : une empreinte **SHA-256** (intégrité), une **signature ECDSA P-256** vérifiable par un tiers (clé publique partageable), et un **chaînage** — chaque bloc pointe le précédent, sans effacement possible.

Nous restons volontairement mesurés : on parle de **scellé · intégrité vérifiable**, pas d'« infalsifiable ». La chaîne est aujourd'hui interne ; une **empreinte quotidienne sera ancrée publiquement** (voir la roadmap) pour la rendre opposable à tous.

**ADN Network certifie chaque donnée par un certificat**, intégré à l'application.

**À l'échelle d'un groupe** : filiales, participations et organigrammes issus de Sherlock se scellent de la même façon, à chaque niveau.

**Point clé** : sur la chaîne ne circulent que des **empreintes** (hachages), **jamais la donnée brute**.

*Figure — Exemple de sortie du logiciel Packdata, scellé dans l'ADN Network — identité masquée, chiffres et sources authentiques.*

Contenu d'un certificat : identité vérifiée, données publiques (abonnés, fiabilité /20, e-mail générique, siège), 3 sources opposables minimum (profil public, indexation moteur, open-data SIREN), empreinte — identifiant unique, SHA-256, signature ECDSA P-256 vérifiable par un tiers, clé publique partageable, signature HMAC, chaînage (bloc + bloc précédent), horodatage UTC. Chaque demande fige un état daté ; la suite des certificats fait l'historique, à la hausse comme à la baisse.

Client léger sobre par conception : requêtes bridées à 40 Ko maximum (données fragmentées), cadence réglable par l'utilisateur (intervalle entre cycles, délai entre requêtes, mode auto piloté par l'IA) avec estimation affichée avant contrôle — impact nul sur forfait et batterie aux réglages standards. Chaque contrôle est déclaré, visible et désactivable à tout moment.

**GOUVERNANCE DU PROTOCOLE**

## Ce qui tourne seul, ce qui exige une signature

Le **Cerveau Numérique** est le protocole de décision et de mise à jour de l'**ADN Network** : logiciel local-first compilé, réseau P2P en streaming natif, sans cloud central ni point unique de défaillance.

Règle 1 : **ce qui peut s'exécuter seul s'exécute seul**. Règle 2 : **ce qui engage la responsabilité exige une signature**. Chaque version est journalisée, vérifiable, réversible.

Coûts d'infrastructure déportés sur le poste client, modèle licence fixe et vie. Détail opposable en data room sous NDA.

## Contribuez à la fraîcheur, gagnez des droits

À chaque fois qu'un contributeur **confirme ou rafraîchit** une donnée publique professionnelle, sa contribution est **signée**, horodatée et chaînée. Le réseau sait ainsi, de façon vérifiable, qui a contribué à quoi — sans jamais exposer la donnée brute.

Ces contributions ouvrent des droits d'extraction : plus vous contribuez à la fraîcheur, plus vous pouvez extraire.

1. Contribution : le contributeur confirme ou rafraîchit une donnée → gagne des droits d'extraction. Plus de contributions = données plus fraîches pour tous.
2. Extraction : l'entreprise utilise ses droits pour extraire des données, selon son forfait. L'usage rafraîchit aussi le réseau.
3. Cycle : plus le réseau est actif → données fraîches → chacun en profite. Un cercle vertueux : fraîcheur partagée.
4. Équilibre : les entreprises extraient selon leur forfait, le réseau reste frais. Chacun prospecte sur une data à jour.

**Lexique — à ne pas confondre**

**ADN Network** : le réseau de données. **Crédit** : l’unité de contribution interne du réseau (non monétaire) — 1 crédit ≈ 1 donnée publique confirmée ou rafraîchie.

**Crédits d'extraction** : droits d'extraire des données, gagnés en contribuant, utilisables dès l'année 2.

**Token** : piste à l'étude — le code sera public sur GitHub. Aucune date annoncée.

C'est quoi le token ? Piste à l'étude, code public sur GitHub. Dépôt e-Soleau INPI n° DSO2026033766 du 13/09/2026. Renseignez-vous sans engagement.

**RÉCOMPENSES**

## Contribuer, ça rapporte

Plus vous tenez la data à jour, plus le réseau vous rend.

Professionnel : des crédits pour l'année 2. Pas de licence disponible cette année ? Contribuez **dès maintenant** avec Packdata Lite et cumulez des **crédits d'extraction**. En année 2, quand la licence ADN Network vous sera ouverte, vos crédits vous attendent — vous extrayez **sans attendre**, et vos contributions passées **réduisent aussi le prix** de votre mise à jour annuelle. **Bon à savoir : votre usage du logiciel contribue déjà aux mises à jour — et vous pouvez accélérer en installant Packdata Lite (gratuit) sur d'autres postes.**

Particulier : nano-crédits. Chaque mise à jour vous rapporte des **nano-crédits**, à garder ou à échanger contre des extractions et des avantages du réseau.

À l'étude : jeton échangeable. Un jeton d’usage échangeable est **à l'étude**, qui serait **encadré juridiquement** (cadre MiCA). Décrit à titre d'information — **aucune promesse de valeur ni de rendement**.

**PARTENAIRES**

## Nous recherchons des partenaires

Faire évoluer l'ADN Network ne se fera pas seuls : nous cherchons des partenaires pour déployer, enrichir et faire rayonner le réseau — en France comme à l'international.

Revendeurs & intégrateurs : distribuez la licence ADN Network sur votre territoire ou votre verticale, avec **formation, support et conditions partenaires dédiées**.

Fournisseurs de données : connectez vos bases au réseau. **Vos données restent les vôtres**, leur fraîcheur profite à tous et vous rapporte des **droits d'extraction**.

Prescripteurs & territoires : agences, fédérations, collectivités : faites bénéficier **votre écosystème** d'une data à jour et participez au rayonnement du réseau.

**ROADMAP**

## Deux phases, prudence d'abord

### Crédits, remises & ancrage public

Remise de licence pour les pros contributeurs, **nano-crédits** pour les particuliers, et une empreinte quotidienne de la chaîne ancrée publiquement via **OpenTimestamps** (gratuit, sur Bitcoin) — la traçabilité s’en trouve renforcée. Aucune régulation particulière.

### Jeton échangeable — à l'étude, encadré

Un jeton d’usage échangeable serait **encadré juridiquement** (cadre MiCA, conseil spécialisé) avant tout lancement. Ce document ne constitue ni une offre, ni une sollicitation, ni une promesse de valeur.

**CADRE LÉGAL & ÉTHIQUE**

## Construit pour être conforme

**LE CLIENT DE CONTRIBUTION**

## Léger, multiplateforme, volontaire

Un client léger (**macOS, Windows, iOS, Android, Chrome**) permet de contribuer au réseau : l'app interroge **aléatoirement** des données publiques professionnelles pour les confirmer ou les rafraîchir dans l'ADN Network. Rien n'est collecté à l'insu des personnes. Chaque contribution est **chiffrée** et récompensée en droits d'extraction.

Ce document est fourni à titre d'information et décrit une vision produit susceptible d'évoluer. Il ne constitue ni une offre, ni une sollicitation d'investissement, ni une promesse de rendement. Le volet « jeton » est à l'étude et serait, le cas échéant, encadré juridiquement avant tout lancement.

macOS — ● ACTIF · Windows — Beta · iOS — TestFlight · Android — Test interne · Chrome — Beta · API — ● DISPONIBLE · GitHub — @Packdata-io

Packdata — ADN NETWORK

La data B2B, l'IA et l'envoi — réunis.
