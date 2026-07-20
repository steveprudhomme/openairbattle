# Stratégie de tests

Les tests restent séparés du code de production.

## Invariants de catalogue

- 200 cartes uniques dans cards-usa.csv;
- 200 cartes uniques dans cards-russia.csv;
- identifiants uniques et préfixés USA ou RUS;
- exactement 60 cartes dans chaque deck;
- aucune carte non basique à plus de 2 copies;
- toute carte d’un deck existe dans l’extension correspondante;
- coûts, PV, puissance et mission sont des entiers dans les plages documentées;
- aucune carte exclue dans docs/05-sources-et-hypotheses-2026.md.

## Tests unitaires futurs

- paiement et redressement des ressources;
- exposition et interception;
- dégâts simultanés;
- destruction et défausse des équipements;
- Verrouillage, Réseau, Formation et Barrage;
- priorité des mots « ne peut pas »;
- conditions de victoire simultanées.

## Tests d’intégration

- partie complète avec chaque deck de départ;
- import CSV vers le moteur;
- sauvegarde et reprise déterministes;
- rendu des caractères français.

## Non-régression d’équilibrage

Conserver pour chaque version :

- taux de victoire par faction;
- durée médiane;
- tour médian du premier point;
- fréquence des mains sans ressource;
- cartes gardées, jouées et mortes en main.

Un objectif raisonnable pour un premier échantillon de 100 parties est un taux de victoire compris entre 45 % et 55 % pour chaque starter, sans conclure à l’équilibre définitif.

