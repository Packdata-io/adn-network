# Client léger — sobriété des requêtes (2026-09-14)

Le client léger Packdata est bridé par conception : requêtes de
40 Ko maximum (données fragmentées), cadence réglable par
l'utilisateur (intervalle entre cycles, délai entre requêtes, mode
auto piloté par l'IA) avec estimation affichée avant contrôle — impact nul sur
forfait et batterie aux réglages standards.

Chaque contrôle part d'une simple URL publique, ne rapatrie que le
compteur observé, et seule la différence avant/après voyage. Chaque
contrôle est déclaré, visible par l'utilisateur et désactivable à
tout moment. Les requêtes ne transportent que des empreintes,
jamais de données brutes.
