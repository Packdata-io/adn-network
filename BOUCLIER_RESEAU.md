# Bouclier réseau — le protocole face au terrain

**Date :** 2026-10-06

## 1. Ce que le protocole établit

L'application tourne en local sur le terminal de l'utilisateur. Seules des
empreintes signées rejoignent le réseau, jamais les données brutes. Les
requêtes de vérification sont fragmentées (≤ 40 Ko) à cadence réglable par
l'utilisateur. Il n'existe pas de serveur central de collecte : le trafic de
vérification part des terminaux des contributeurs eux-mêmes.

## 2. Ce que les réseaux apportent

En accès fixe comme mobile, les opérateurs mutualisent des centaines
d'abonnés derrière une même adresse publique, réattribuée fréquemment. Une
micro-requête se fond donc dans le trafic ordinaire. Conséquence mesurable :
bloquer ces adresses à grande échelle provoque des dommages collatéraux
massifs (abonnés légitimes coupés), ce qui rend le blocage par adresse IP
coûteux et impraticable comme méthode principale — sans le rendre impossible.

## 3. Synergie, sans absolu

| Protocole | Réseau | Effet |
|---|---|---|
| Requêtes ≤ 40 Ko à cadence réglable | Trafic léger indistinguable d'une navigation normale | Détection comportementale rendue difficile, non exclue |
| Aucune IP ni identifiant personnel exposé | Adresses publiques partagées et rotatives | Blocage par IP impraticable à grande échelle, non impossible |
| Empreintes seules, données jamais sorties | Transport chiffré | Interception inexploitable ; surface juridique réduite (données publiques, consentement, traçabilité), jamais totale |
| Pas de serveur central de collecte | Terminaux répartis | Aucun point unique à bloquer ; l'amorçage initial et les mises à jour logicielles restent les seuls points centralisés admis |

© 2026 — lecture autorisée ; toute copie, modification ou usage commercial
requiert l'autorisation écrite de l'auteur.
