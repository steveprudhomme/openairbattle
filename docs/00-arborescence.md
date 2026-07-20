# Arborescence du dépôt

~~~text
open-air-battle/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md
│   │   └── feature_request.md
│   ├── workflows/
│   │   └── ci-cd-pipeline.yml.example
│   └── PULL_REQUEST_TEMPLATE.md
├── LICENSES/
│   └── README.md
├── docs/
│   ├── architecture/
│   │   └── README.md
│   ├── decks/
│   │   ├── starter-russie-60.md
│   │   └── starter-usa-60.md
│   ├── extensions/
│   │   ├── extension-russie-200.md
│   │   └── extension-usa-200.md
│   ├── legal/
│   │   └── NOTICE-IMAGES.md
│   ├── 00-arborescence.md
│   ├── 01-note-intention-et-ingenierie.md
│   ├── 02-regles-9-plus.md
│   ├── 03-guide-demarrage-rapide.md
│   ├── 04-reference-equilibrage.md
│   ├── 05-sources-et-hypotheses-2026.md
│   ├── 06-rapport-validation.md
│   └── index.md
├── game-data/
│   ├── decks/
│   │   ├── starter-russia.csv
│   │   └── starter-usa.csv
│   ├── cards-russia.csv
│   ├── cards-usa.csv
│   └── README.md
├── src/
│   └── README.md
├── tests/
│   └── README.md
├── .gitignore
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── GOVERNANCE.md
├── LICENSE
├── README.md
├── SECURITY.md
└── SUPPORT.md
~~~

docs/ contient les textes de référence; game-data/ contient les vues structurées; src/ accueillera le futur moteur; tests/ demeure isolé du code de production. Les fichiers communautaires et juridiques restent visibles à la racine pour réduire le coût d’entrée.
