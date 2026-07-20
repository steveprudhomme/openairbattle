# Rapport de validation du prototype 0.1.5

Date : 20 juillet 2026.

## Résultats structurels

| Contrôle | États-Unis | Russie | Résultat |
| --- | ---: | ---: | --- |
| cartes d’extension | 200 | 200 | conforme |
| identifiants uniques | 200 | 200 | conforme |
| noms uniques | 200 | 200 | conforme |
| Appareils | 80 | 80 | conforme |
| Équipements | 40 | 40 | conforme |
| Tactiques | 40 | 40 | conforme |
| Soutiens | 39 | 39 | conforme |
| Ressources de base uniques | 1 | 1 | conforme |

Chaque fichier CSV comporte une ligne d’en-tête et 200 lignes de données.

## Starters

| Contrôle | Starter USA | Starter Russie |
| --- | ---: | ---: |
| cartes physiques | 60 | 60 |
| ressources basiques | 20 | 20 |
| cartes actives | 40 | 40 |
| noms actifs différents | 26 | 26 |
| maximum non basique | 2 | 2 |
| cartes inconnues de l’extension | 0 | 0 |

Courbe des 40 cartes actives :

| Coût | USA | Russie |
| ---: | ---: | ---: |
| 1 | 2 | 2 |
| 2 | 9 | 9 |
| 3 | 12 | 10 |
| 4 | 8 | 6 |
| 5 | 7 | 7 |
| 6 | 2 | 6 |

Coût moyen : 3,38 pour les États-Unis et 3,62 pour la Russie. La Russie paie une courbe plus lourde en échange de davantage de PV et de Blindage; cette hypothèse doit être testée en partie.

## Validation des états et du ciblage

| Situation | Orientation | Exposition | Interception adverse | Résultat |
| --- | --- | --- | --- | --- |
| déploiement normal | engagé | non exposé | interdite | conforme |
| Décollage rapide avant action | redressé | non exposé | interdite | conforme |
| après une Mission | engagé | exposé | autorisée | conforme |
| après une Interception | engagé | exposé | autorisée | conforme |
| redressement par un effet | redressé | exposition inchangée | selon l’exposition | conforme |

Le lexique, la règle 6, le guide rapide et les cas de test séparent désormais l’orientation de la carte et son exposition. Furtif vérifie seulement l’exposition. Les effets d’AGM-154 JSOW et de Legion Pod ont été reformulés dans le catalogue Markdown et dans le CSV afin de rester fonctionnels avec cette règle.

## Validation de la Retraite

| Cas | Résultat attendu | Résultat |
| --- | --- | --- |
| espace aérien rempli avec un Appareil redressé | une place peut être libérée avant le déploiement | conforme |
| Appareil engagé | Retraite interdite | conforme |
| Appareil avec un Équipement | les deux cartes sont défaussées simultanément | conforme |
| effet déclenché par « détruit » | aucun déclenchement | conforme |
| Retraite sans Appareil déployable | interdite | conforme |
| deux Appareils retirés avant un seul déploiement | seconde Retraite interdite | conforme |

Les effets de cartes qui réagissent à une destruction restent inchangés : la règle générale distingue explicitement Retraite, défausse et destruction. Les catalogues Markdown et CSV ne nécessitent donc aucune réécriture pour cette mécanique.

## Validation de la Récompense de Domination

| Cas | Gain de la personne qui intercepte | Gain de l’adversaire | Résultat |
| --- | ---: | ---: | --- |
| cible détruite, intercepteur survivant | 1 | 0 | conforme |
| cible et intercepteur détruits simultanément | 1 | 0 | conforme |
| cible survivante | 0 | 0 | conforme |
| autre Appareil détruit par Barrage | 0 point supplémentaire | 0 | conforme |
| plusieurs destructions liées à une Interception | 1 maximum | 0 | conforme |
| passage de 14 à 15 par la récompense | victoire immédiate | — | conforme |

Le seuil de victoire, le matériel, le résumé, la boucle de jeu et les conditions de victoire indiquent désormais 15 points. Les textes des cartes restent inchangés : aucun ne contient un seuil de victoire ni n’accorde directement cette récompense.

## Validation du mulligan

| Cas | Résultat attendu | Résultat |
| --- | --- | --- |
| main initiale sans Ressource | mulligan autorisé | conforme |
| main initiale avec une ou plusieurs Ressources | mulligan autorisé | conforme |
| utilisation du mulligan | main montrée puis remélangée dans le deck | conforme |
| taille de la main de remplacement | 6 cartes | conforme |
| nouvelle main sans Ressource ou non synergique | elle doit être conservée | conforme |
| tentative de second mulligan | interdite | conforme |

La règle 3.4 et le guide rapide ne conditionnent plus le mulligan au contenu de la main. Avec 20 Ressources dans 60 cartes, une nouvelle main de 6 cartes contient au moins une Ressource dans environ 92,33 % des cas. Les catalogues et les starters restent inchangés, car cette règle ne modifie ni les cartes ni la construction des decks.

## Licence et feuille de route

| Contrôle | Résultat |
| --- | --- |
| texte intégral de la GNU GPL version 3 dans `LICENSE` | conforme |
| identifiant SPDX déclaré | `GPL-3.0-only` |
| badge et déclaration du README alignés | conforme |
| licence des contributions documentée | conforme |
| feuille de route présente à la racine | conforme |

La feuille de route marque comme terminés la réforme des états en 0.1.1, le verrouillage de plateau en 0.1.3, la matrice des incitations en 0.1.4 et l’assouplissement du mulligan en 0.1.5. Aucun autre chantier planifié n’est traité comme une règle active dans cette version.

## Budget des Appareils

Les 80 Appareils de chaque faction respectent un écart maximal absolu de 0,5 par rapport à T(C) = 4C + 3, avant prise en compte des synergies de deck. La tolérance documentée est de 1.

Plages observées :

| Mesure | USA | Russie |
| --- | --- | --- |
| coût | 3 à 8 | 2 à 8 |
| PV | 6 à 15 | 4 à 17 |
| Puissance | 1 à 9 | 1 à 10 |
| Mission | 1 à 3 | 1 à 3 |

## Contrôles encore humains

- compatibilité thématique exacte de chaque Équipement avec chaque plateforme;
- clarté du texte auprès d’enfants de 9 à 12 ans;
- interactions imprévues entre les 200 cartes d’une faction;
- durée et rythme réels;
- taux de victoire;
- mise en page et taille de police des futures cartes;
- validation juridique du nom, des marques, des illustrations et de la compatibilité des futures œuvres de tiers avec GPL-3.0-only.

## Conclusion

La structure et les comptes sont conformes au cahier des charges. L’équilibrage est mathématiquement cohérent au premier ordre, mais il n’est pas encore démontré empiriquement. La version 0.1.5 doit être considérée comme un prototype de test. Furtif, la fréquence des Retraites, la répartition des points entre Mission et Domination ainsi que l’usage du mulligan doivent faire l’objet de parties de non-régression.
