# Positionnement — data B2B vivante en P2P (2026-09-14)

L'ADN Network, c'est de la data B2B vivante en P2P. Principe :
chaque utilisation (recherche, export, envoi) recontrôle les
données touchées sur leurs sources publiques et rescelle le
constat — la base se rafraîchit pendant qu'on l'utilise, sans
batch, sans snapshot figé. Architecture : aucun point de
défaillance unique (No Single Point of Failure) — la donnée vit
sur le réseau, pas sur un serveur central.

Preuve : chaque mise à jour est un certificat horodaté et chaîné
(cf. CERTIFICAT_EXEMPLE.md) ; la suite des certificats fait
l'historique, à la hausse comme à la baisse. À l'inverse d'une
base achetée qui perd ~30 % de fraîcheur par an : ici, chaque
usage renouvelle la donnée consommée.

## Le moteur (tel que présenté sur packdata.io)
« Notre protocole distribué propriétaire : un flux vivant qui
s'auto-nettoie. Fini les snapshots figés — chaque usage du réseau
rafraîchit la donnée pour tous. » Le client léger gratuit Packdata Lite (bêta) permet aux contributeurs d'aider le réseau à
rester à jour — sur le principe des applications participatives (à la manière de Waze — marque Google, citée pour expliquer, sans affiliation).

## Crédits
Les crédits sont des unités de contribution non monétaires. Un éventuel
jeton échangeable est à l'étude et serait encadré juridiquement (MiCA)
avant tout lancement — aucune promesse de valeur ou de rendement.

## Vision — agents IA : BYOA piloté disponible, autonome Packdata en R&D
Votre agent que vous branchez (votre clé, vos règles) : disponible — il vérifie et vous rapporte. Nos agents autonomes opérés par Packdata : en R&D, non déployés. Direction future : des flux vérifiés comme couche de confiance pour agents IA (anti-hallucination). Statut suit la réalité : passage à opérationnel uniquement sur preuve.
