# Code source

Ce dossier accueillera les modules de production lorsque la communauté aura choisi une pile technique. La structure reste volontairement agnostique.

Principes :

- séparer moteur de règles, données, interface et persistance;
- faire du moteur une fonction déterministe testable;
- conserver les catalogues dans un format ouvert;
- ne jamais coder le texte d’une carte directement dans l’interface;
- rendre chaque aléa reproductible par une graine pour les tests;
- prévoir localisation, clavier, lecteur d’écran et contraste dès l’architecture.

