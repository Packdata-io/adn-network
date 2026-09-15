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
rafraîchit la donnée pour tous. » Le client léger gratuit Light
Packdata (bêta) permet aux contributeurs d'aider le réseau à
rester à jour — effet Waze appliqué à la data B2B.
