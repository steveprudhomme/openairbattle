# Contribuer à Open Air Battle

Merci de consacrer du temps au projet. Les contributions techniques et non techniques ont la même valeur : règles, tests de parties, accessibilité, illustrations originales, traduction, documentation, tri des tickets et animation communautaire sont toutes utiles.

## Avant de commencer

1. Lire CODE_OF_CONDUCT.md et GOVERNANCE.md.
2. Rechercher un ticket existant.
3. Pour un changement important de règles ou de format, ouvrir d’abord une proposition.
4. Ne jamais joindre de document classifié, restreint, divulgué illégalement ou contenant des données personnelles.

## Préparer une copie locale

~~~sh
git clone [URL_DU_DEPOT]
cd open-air-battle
git switch -c type/description-courte
~~~

Le dépôt est agnostique au langage. Lorsqu’une implémentation sera choisie, ses commandes reproductibles devront être ajoutées ici. En attendant, vérifier au minimum les fichiers Markdown, les liens relatifs et les invariants décrits dans tests/README.md.

Si le futur code nécessite des dépendances, utiliser un environnement local isolé et un fichier de verrouillage propre à l’écosystème retenu. Ne jamais installer globalement une dépendance seulement pour contribuer.

## Branches

- main : état intégrable et documenté;
- feature/nom-court : nouvelle capacité;
- fix/nom-court : correction;
- docs/nom-court : documentation;
- balance/nom-court : ajustement de cartes.

Une branche doit rester courte et centrée sur un seul objectif.

## Qualité attendue

- noms explicites et cohérents;
- petits modules à responsabilité claire;
- aucune duplication évitable;
- commentaires réservés au pourquoi, pas à la répétition du code;
- comportement public documenté;
- tests ajoutés ou adaptés avec chaque fonctionnalité;
- aucune baisse de couverture sans justification;
- données de cartes modifiées dans leur source canonique et dans les vues générées;
- texte compréhensible par une personne de 9 ans pour les règles de base.

## Validation locale

Avant une demande de fusion :

1. exécuter la future commande de tests indiquée dans tests/README.md;
2. confirmer 200 identifiants uniques par extension;
3. confirmer 60 cartes par deck et au plus 2 copies de toute carte non basique;
4. vérifier que chaque carte de deck existe dans son extension;
5. vérifier les liens et l’orthographe;
6. expliquer tout écart d’équilibrage supérieur à la tolérance.

## Commits

Utiliser Conventional Commits :

~~~text
type(portée): description à l’impératif

Corps facultatif expliquant le pourquoi.

Signed-off-by: Prénom Nom <adresse@example.org>
~~~

Types usuels : feat, fix, docs, test, refactor, chore, balance.

## Developer Certificate of Origin

Chaque commit doit être signé avec l’option -s :

~~~sh
git commit -s -m "docs(regles): clarifier l’interception"
~~~

La mention Signed-off-by certifie que vous avez créé la contribution ou que vous avez le droit de la soumettre sous la licence du projet, conformément au Developer Certificate of Origin 1.1. Ce mécanisme évite un CLA corporatif tout en protégeant la provenance juridique des apports. Ne signez jamais au nom d’une autre personne.

## Demande de fusion

Décrire :

- le problème;
- la solution;
- les fichiers et règles touchés;
- les validations effectuées;
- l’effet attendu sur l’équilibrage;
- les sources publiques utilisées pour tout nouveau matériel réel.

Un changement de puissance n’est pas « petit » : fournir au moins trois parties de test ou une justification probabiliste.

