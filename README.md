[![Statut](https://img.shields.io/badge/statut-prototype%20jouable-orange)](CHANGELOG.md) [![Version](https://img.shields.io/badge/version-0.1.3-blue)](CHANGELOG.md) [![Licence](https://img.shields.io/badge/licence-GPL--3.0--only-blue)](LICENSE)

**Open Air Battle est un jeu libre, gratuit et communautaire. Les éléments originaux du projet sont distribués sous la GNU General Public License version 3 uniquement (`GPL-3.0-only`). Voir [LICENSE](LICENSE).**

# Open Air Battle

Open Air Battle est un jeu de cartes à collectionner sur l’aviation militaire moderne, conçu pour les personnes de 9 ans et plus. Sa boucle de jeu tient en trois verbes : déployer, accomplir une mission, intercepter. Sous cette surface simple, les deux factions proposent des décisions différentes :

- les États-Unis coordonnent capteurs, désignations et frappes précises;
- la Russie construit des formations résistantes et produit de fortes poussées de puissance.

Le prototype 0.1.3 contient :

- un système de jeu complet et une méthode d’équilibrage chiffrée;
- une extension États-Unis de 200 cartes uniques;
- une extension Russie de 200 cartes uniques;
- deux decks de départ de 60 cartes exactement;
- un livret de règles pédagogique pour 9 ans et plus;
- une mécanique de Retraite qui empêche le verrouillage d’un espace aérien rempli;
- des catalogues CSV destinés à une future application ou à la mise en page papier.

## Démarrage rapide

1. Lire docs/03-guide-demarrage-rapide.md.
2. Préparer un deck de 60 cartes par personne à partir de docs/decks/.
3. Utiliser des cartes imprimées glissées devant des cartes ordinaires dans des protège-cartes opaques.
4. Prévoir des marqueurs de dégâts, des marqueurs Exposé, deux marqueurs Verrouillage et de quoi compter jusqu’à 12.
5. Jouer une première partie avec les aides de tour du livret.

Le dépôt ne contient encore ni illustrations militaires ni logiciel exécutable. Le dossier src/ est réservé à une future implémentation, sans imposer de langage.

## Documentation

- docs/01-note-intention-et-ingenierie.md : vision, mécaniques et identité des factions;
- docs/00-arborescence.md : carte complète du dépôt;
- docs/02-regles-9-plus.md : règles complètes;
- docs/04-reference-equilibrage.md : formules, barèmes et garde-fous;
- docs/05-sources-et-hypotheses-2026.md : sources publiques et exclusions;
- docs/extensions/ : catalogues complets;
- docs/decks/ : listes détaillées des decks de départ;
- ROADMAP.md : priorités, problèmes de conception et actions envisagées;
- game-data/ : données tabulaires.

## État du projet

Le contenu est un prototype de conception, pas une simulation militaire. Les noms d’appareils, d’armements et de doctrines sont fondés sur des sources publiques consultées en juillet 2026. Les coûts, PV, puissances et effets sont des abstractions ludiques originales.

## Canaux officiels

Les adresses suivantes sont des espaces réservés à configurer avant la publication :

- forum : [URL_DU_FORUM_COMMUNAUTAIRE];
- discussion en direct : [URL_DU_SALON_COMMUNAUTAIRE];
- annonces : [URL_DE_LA_LISTE_DE_DIFFUSION];
- sécurité : [ADRESSE_SECURITE_PRIVEE].

Ne publiez pas d’adresse réelle tant qu’une équipe n’est pas prête à en assurer le suivi.

## Participer

Les contributions de code, de règles, d’équilibrage, de documentation, de traduction, d’accessibilité, de mise en page et de test sont bienvenues. Lire CONTRIBUTING.md, CODE_OF_CONDUCT.md et GOVERNANCE.md avant de proposer un changement.

## Indépendance

Open Air Battle est un projet indépendant. Il n’est ni affilié, ni approuvé, ni commandité par un gouvernement, une force armée ou un fabricant. Aucune image officielle ou marque graphique n’est incluse.

Les noms, marques, faits et futures œuvres de tiers ne sont pas automatiquement couverts par la licence du projet; leurs droits propres doivent être respectés.
