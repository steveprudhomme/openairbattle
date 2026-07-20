# Architecture future

La documentation et les données précèdent l’implémentation. Une future application devrait isoler cinq composants :

1. catalogue immuable des cartes;
2. état de partie;
3. moteur de commandes et de validation;
4. journal d’événements reproductible;
5. interfaces locales, web ou réseau.

Le moteur ne doit dépendre ni du navigateur ni d’un moteur graphique. Cette séparation rend possibles les tests automatiques, l’intelligence artificielle, le jeu local et plusieurs interfaces sans dupliquer les règles.

