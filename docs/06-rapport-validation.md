# Rapport de validation du prototype 0.1.0

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
- validation juridique du nom, de la licence et des illustrations.

## Conclusion

La structure et les comptes sont conformes au cahier des charges. L’équilibrage est mathématiquement cohérent au premier ordre, mais il n’est pas encore démontré empiriquement. La version 0.1.0 doit être considérée comme un prototype de test.

