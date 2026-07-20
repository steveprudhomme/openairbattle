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
- déploiement normal : Appareil engagé, non exposé et non interceptable;
- Décollage rapide : Appareil redressé, non exposé, puis exposé seulement après son action;
- engagement et exposition indépendants : engager n’expose pas, redresser par un effet ne retire pas l’exposition;
- fin de l’exposition au début du prochain tour de la personne qui contrôle l’Appareil;
- Furtif fondé sur l’exposition, y compris pour un Appareil engagé juste après son déploiement;
- interdiction d’intercepter tout Appareil non exposé;
- Retraite d’un Appareil redressé suivie immédiatement d’un déploiement;
- impossibilité de faire battre en Retraite un Appareil engagé;
- une seule Retraite autorisée avant chaque déploiement et aucune Retraite sans déploiement légal;
- défausse simultanée de l’Appareil en Retraite et de son Équipement;
- absence de déclenchement des effets « détruit » lors d’une Retraite;
- plateau de 5 Appareils renouvelable sans dépasser la limite;
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
