# Référence d’équilibrage

## 1. Objectifs mesurables

- partie médiane : 8 à 11 tours par personne;
- durée : 25 à 35 minutes;
- premier point de suprématie : tours 2 à 4;
- taux de victoire des starters : 45 % à 55 % sur un échantillon d’au moins 100 parties;
- moins de 10 % des mains initiales injouables après la règle de nouvelle main.

## 2. Appareils

Budget cible :

> T(C) = 4C + 3

Valeur :

> V = PV + 1,5P + 2,5M + K + E − D

avec :

- C : coût;
- P : Puissance;
- M : Mission;
- K : mots-clés;
- E : effet;
- D : contraintes ou risques.

Tolérance standard : |V − T(C)| ≤ 1. Une carte vedette peut aller jusqu’à 1,5 si son deck comporte une vraie contrainte.

## 3. Barème initial

| Élément | Valeur |
| --- | ---: |
| Agile | 1,0 |
| Blindage 1 | 1,5 |
| Blindage 2 | 3,5 |
| Décollage rapide | 2,0 |
| Furtif | 2,0 |
| Barrage 1 | 1,5 |
| Barrage 2 | 3,0 |
| placer un Verrouillage | 1,5 |
| piocher puis défausser | 1,0 |
| piocher une carte nette | 2,5 |
| redresser un autre Appareil avec restriction | 2,0 à 3,0 |
| arriver engagé un tour supplémentaire | contrainte de 2,0 |

Les mots-clés ne sont pas purement additifs. Furtif et Mission 3, par exemple, se renforcent mutuellement; ajouter 0,5 à 1,0 de prime de synergie.

Depuis la version 0.1.1, Furtif dépend de l’exposition et non de l’orientation : il protège donc aussi un Appareil engagé mais non exposé, notamment juste après son déploiement. Sa valeur de 2,0 est conservée provisoirement; elle doit être contrôlée en partie avant toute hausse, car cette protection commence désormais un tour plus tôt.

## 4. Cartes non Appareil

Budget cible :

> S(C) = 2,5C + 1

Repères :

| Effet ponctuel | Valeur |
| --- | ---: |
| 1 dégât ciblé | 1,0 |
| 1 dégât à deux cibles conditionnelles | 1,5 |
| +1 Puissance pour un combat | 1,0 |
| +1 Mission pour une action | 2,0 |
| piocher une carte nette | 2,5 |
| filtrer deux cartes sans gain net | 1,5 |
| économiser une ressource ce tour | 1,5 |
| détruire un Équipement | 2,5 |
| redresser une ressource | 1,0 |

Pour un effet permanent, multiplier la partie répétable par 1,5, puis ajouter la valeur immédiate. Une condition qui se réalise environ une fois sur deux réduit la portion conditionnelle de moitié.

## 5. Courbe des starters

Chaque deck possède 20 ressources. Les 40 autres cartes visent :

| Coût | Nombre cible |
| ---: | ---: |
| 1 | 4 à 6 |
| 2 | 7 à 9 |
| 3 | 9 à 11 |
| 4 | 7 à 9 |
| 5 | 4 à 6 |
| 6 ou plus | 3 à 5 |

Les probabilités hypergéométriques avec 20 ressources sur 60 sont :

| Cartes vues | au moins 1 ressource | au moins 2 | au moins 3 |
| ---: | ---: | ---: | ---: |
| 7 | 95,17 % | 75,30 % | 42,92 % |
| 8 | 96,99 % | 82,42 % | 53,92 % |
| 9 | 98,15 % | 87,75 % | 63,78 % |
| 10 | 98,88 % | 91,62 % | 72,24 % |

## 6. Tests à enregistrer

Pour chaque partie :

- faction et première personne;
- main conservée ou repiochée;
- ressources aux tours 1 à 5;
- suprématie à chaque tour;
- cartes jamais jouables;
- résultat et tour final;
- règle relue;
- impression qualitative.

## 7. Signaux d’alerte

- une carte jouée automatiquement dès qu’elle est disponible;
- une carte jamais gardée ni jouée;
- une partie décidée par une seule ressource manquée;
- une boucle de redressement produisant plus de 4 points en un tour;
- un verrouillage sans contre-jeu;
- plus de 6 dégâts hors combat en un tour;
- une différence de taux de victoire supérieure à 10 points après 100 parties.

La formule sert à détecter, pas à prouver. Toute modification doit être suivie de parties réelles.
