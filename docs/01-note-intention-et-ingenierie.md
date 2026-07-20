# Phase 1 — Note d’intention et ingénierie du jeu

## 1. Promesse

Open Air Battle veut faire ressentir une bataille aérienne moderne sans demander de connaître l’aéronautique. Une partie doit pouvoir commencer après dix minutes d’explication et durer environ 25 à 35 minutes.

La profondeur vient d’un choix visible à chaque tour : un appareil prêt peut accomplir une mission pour marquer des points, ou rester disponible pour protéger la formation. Le déploiement l’engage sans l’exposer; après une mission ou une interception, il devient exposé. L’orientation indique si l’Appareil peut agir, tandis que l’exposition indique s’il peut être intercepté. Le joueur gagne donc en prenant un risque, pas en mémorisant une longue chaîne d’exceptions.

## 2. Boucle centrale

1. redresser ses cartes et piocher;
2. ajouter au plus une ressource;
3. déployer ou préparer sa force;
4. accomplir des missions pour gagner de la suprématie;
5. intercepter les appareils exposés;
6. atteindre 12 points de suprématie.

Cette boucle reprend des qualités pédagogiques éprouvées dans les TCG accessibles : zones peu nombreuses, économie croissante, texte local sur les cartes et objectif positif visible.

Depuis la version 0.1.3, la Retraite empêche un espace aérien rempli de verrouiller la partie : avant un déploiement, un Appareil redressé peut céder sa place. Ce départ n’est pas une destruction et ne récompense donc pas les synergies fondées sur la perte au combat.

## 3. Types de cartes

| Type | Fonction | Limite |
| --- | --- | --- |
| Appareil | combat, mission et présence durable | 5 dans l’espace aérien |
| Équipement | améliore un appareil | 1 par appareil |
| Tactique | effet immédiat, puis défausse | aucune, résolue une à la fois |
| Soutien | effet durable de commandement ou de logistique | 2 en jeu |
| Ressource de base | paie les coûts | 1 jouée par tour |

## 4. Zones

- deck;
- main;
- ressources;
- espace aérien;
- zone de soutien;
- défausse;
- piste de suprématie de 0 à 12.

Il n’y a ni pile de réaction ni action pendant le tour adverse dans la version 0.1.3. Ce choix réduit fortement la charge cognitive et les disputes de priorité.

## 5. Identité des factions

### États-Unis — réseau, précision, flexibilité

Le deck américain crée des marqueurs Verrouillage, améliore la qualité de la main et combine Appareils, Équipements et Soutiens. Ses appareils sont efficaces mais paient une partie de leur budget pour Furtif, Agile ou des effets de déploiement. Ils gagnent lorsque plusieurs éléments modestes produisent ensemble une action précise.

Signatures :

- Réseau : condition satisfaite par un autre appareil prêt ou un soutien;
- Verrouillage : +1 dégât sur la prochaine frappe amie;
- redressement, filtrage de cartes et choix entre plusieurs modes;
- équipement technologique ciblé.

Faiblesse voulue : moins de PV bruts à coût égal et dépendance à une table organisée.

### Russie — formation, endurance, puissance de salve

Le deck russe déploie des appareils robustes, récompense la présence d’un autre appareil prêt et distribue des dégâts par Barrage. Ses effets sont plus directs et moins dépendants de l’équipement. La faction peut accepter des pertes pour conserver le rythme de déploiement.

Signatures :

- Formation : bonus lorsque le joueur contrôle un autre appareil prêt;
- Blindage et PV supérieurs;
- Barrage contre plusieurs appareils exposés;
- frappes à distance et récupération de ressources.

Faiblesse voulue : entrée en jeu plus lente, moins de sélection de main et décisions moins flexibles.

Ces identités sont des abstractions de jeu inspirées de sources publiques. Elles ne prétendent pas mesurer la valeur réelle des forces.

## 6. Modèle mathématique résumé

Pour un Appareil de coût C :

> Budget cible T(C) = 4C + 3

Sa valeur estimée est :

> V = PV + 1,5 × Puissance + 2,5 × Mission + K + E − D

où K est la valeur des mots-clés, E celle de l’effet et D la valeur des contraintes. Une carte standard vise :

> |V − T(C)| ≤ 1

Les coefficients expriment trois réalités ludiques :

- 1 PV absorbe approximativement 1 dégât;
- 1 Puissance est répétable et vaut donc plus qu’un dégât ponctuel;
- 1 Mission peut se répéter mais expose l’appareil et consomme son action.

Les cartes non Appareil utilisent une échelle distincte :

> Budget d’effet S(C) = 2,5C + 1

Le détail des évaluations, des probabilités et des garde-fous est dans 04-reference-equilibrage.md.

## 7. Construction des starters

Chaque starter contient :

- 20 ressources de base;
- 40 cartes actives;
- 26 cartes actives différentes;
- au plus 2 copies de toute carte non basique.

Avec 20 ressources dans 60 cartes, la probabilité d’en voir au moins une dans une main initiale de 7 est d’environ 95,17 %. Après dix cartes vues, la probabilité d’avoir vu au moins trois ressources est d’environ 72,24 %. La règle de nouvelle main sans ressource protège les cas restants.

## 8. Base de l’architecture du dépôt

Cette proposition s’appuie sur :

- Karl Fogel : réduire le coût d’entrée, rendre les décisions et attentes visibles;
- Jono Bacon : accueillir les contributions variées et documenter les chemins de participation;
- Nadia Eghbal : limiter la dépendance aux mainteneurs et rendre le soutien soutenable;
- Heather Meeker : choisir explicitement la licence, suivre la provenance et séparer les droits sur le code, le contenu et les images;
- Robert C. Martin et Steve McConnell : responsabilités séparées, données canoniques, tests reproductibles et suivi de configuration.

La séparation docs/, game-data/, src/ et tests/ permet d’avancer sur le jeu avant de choisir une technologie. En pratique, un bon outil en ligne de commande ou moteur de règles devient vite fragile si ses données, son affichage et sa logique sont mélangés. Ici, le futur moteur pourra être remplacé sans réécrire les cartes.

## 9. Limites du prototype

- aucune campagne de tests à grande échelle n’a encore mesuré le taux de victoire;
- la formule estime la valeur moyenne, pas toutes les combinaisons;
- les inventaires militaires russes exacts sont opaques et évolutifs;
- aucune maquette graphique ou vérification d’impression n’est incluse;
- aucun avis juridique n’a validé le nom, les marques ni la compatibilité de futures œuvres de tiers avec GPL-3.0-only;
- la durée cible est une hypothèse à confirmer;
- les 400 cartes forment un espace de conception, pas un ensemble prêt pour un tournoi.

La prochaine étape saine est de tester les deux starters, noter chaque tour et ajuster seulement les cartes qui produisent un écart répété.
