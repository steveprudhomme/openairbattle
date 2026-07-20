# Feuille de route d’Open Air Battle

Dernière mise à jour : 20 juillet 2026.

Cette feuille de route ordonne les améliorations de règles et de construction du prototype. Un élément « planifié » décrit une intention de conception : il ne devient une règle applicable qu’après sa mise en œuvre dans le livret, les aides de jeu, les cartes concernées, les données structurées et les tests.

## Vue d’ensemble

| Priorité | Chantier | Statut |
| --- | --- | --- |
| Critique | Réforme de l’ergonomie de l’état des cartes | Terminé dans la version 0.1.1 |
| Haute | Résolution du verrouillage de plateau — Board Lock | Terminé dans la version 0.1.3 |
| Haute | Rééquilibrage de la matrice des incitations | Terminé dans la version 0.1.4 |
| Modérée | Assouplissement de la variance du mulligan | Terminé dans la version 0.1.5 |
| Suivi | Ajout des mécaniques d’interruption absentes | Audit puis mise en œuvre |
| À décider | Amélioration de la construction de deck | Décision de format requise |

## 1. Réforme de l’ergonomie de l’état des cartes — Priorité critique

**Statut : terminé dans la version 0.1.1.**

### Problématique

La confusion entre « Engagé » et « Exposé » empêche la bonne compréhension du ciblage au premier tour.

### Action

Séparer strictement les deux états dans le lexique du jeu.

- La règle 6, « Déployer un Appareil », stipule : « L’Appareil est placé engagé dans ton espace aérien. Il n’est pas exposé. »
- La définition de Furtif stipule : « Tant que cet Appareil n’est pas exposé, l’adversaire ne peut pas le choisir avec une Tactique ou un effet de Soutien. »
- L’orientation de la carte indique si l’Appareil peut agir; un marqueur « Exposé » indique s’il peut être intercepté.

### Résultat attendu

Furtif est utile dès le déploiement. Un Appareil qui vient d’arriver ne peut pas être intercepté, même s’il est physiquement tourné sur le côté.

## 2. Résolution du verrouillage de plateau — Board Lock — Priorité haute

**Statut : terminé dans la version 0.1.3.**

### Problématique

L’impossibilité de détruire ses propres unités bloque définitivement certaines parties si l’adversaire refuse d’attaquer et que les cinq places de l’espace aérien restent occupées.

### Action

Amender la règle 6 et introduire la mécanique de **Retraite** :

> Avant de déployer un Appareil, tu peux volontairement défausser un de tes Appareils redressés présent dans ton espace aérien pour libérer une place.

L’exigence que l’Appareil soit redressé empêche d’abuser du système en sacrifiant une unité qui vient de marquer des points, car celle-ci est engagée.

### Résolution livrée

- une Retraite ne déclenche pas les effets liés à la destruction;
- l’Équipement attaché est défaussé en même temps que l’Appareil;
- une Retraite doit être suivie immédiatement du déploiement annoncé;
- une seule Retraite est permise avant chaque déploiement;
- les situations à cinq Appareils et les boucles de déploiement sont couvertes par les cas de non-régression.

## 3. Rééquilibrage de la matrice des incitations — Priorité haute

**Statut : terminé dans la version 0.1.4.**

### Problématique

Intercepter ne rapporte aucun point et ralentit sa propre victoire face au seuil actuel de 12 points de Suprématie.

### Action

- augmenter le seuil de victoire de 12 à **15 points de Suprématie**;
- introduire la règle fondamentale suivante :

> **Récompense de Domination :** Si ton Interception détruit un Appareil adverse, ajoute 1 point à ta Suprématie.

Cette modification valorise immédiatement l’interactivité et transforme le combat en une décision tactique viable plutôt qu’en une simple perte de tempo.

### Résolution livrée

- le seuil de victoire est fixé à 15 points de Suprématie;
- la cible principale détruite rapporte 1 point, même en cas de destruction simultanée de l’intercepteur;
- seule la personne qui initie l’Interception reçoit la récompense;
- chaque Interception rapporte au plus 1 point, sans récompense supplémentaire pour Barrage ou un effet postérieur;
- la durée des parties et la répartition des points entre Mission et Domination restent à mesurer en non-régression.

## 4. Assouplissement de la variance du mulligan — Priorité modérée

**Statut : terminé dans la version 0.1.5.**

### Problématique

Le mulligan n’est autorisé que pour une main contenant zéro Ressource, ce qui force parfois des parties non viables ou non synergiques.

### Action

Standardiser la règle 3.4 :

> Une seule fois au début de la partie, tu peux montrer ta main, la remélanger dans le deck, et piocher 6 nouvelles cartes (au lieu de 7), indépendamment de son contenu.

La perte d’une carte punit l’abus tout en garantissant une échappatoire face à une main non viable.

### Résolution livrée

- toute main initiale peut être remplacée, même si elle contient une ou plusieurs Ressources;
- la main initiale est montrée puis entièrement remélangée dans le deck;
- la main de remplacement contient 6 cartes et doit être conservée;
- chaque personne ne peut effectuer ce mulligan qu’une seule fois;
- les tests suivent son utilisation, son motif et le nombre de Ressources avant et après.

## 5. Ajout des mécaniques d’interruption absentes — Priorité de suivi

**Statut : audit puis mise en œuvre.**

### Problématique

La règle précise ce qui arrive « si l’Équipement quitte le jeu », mais le retrait ciblé d’un Équipement n’est pas présenté comme une mécanique explicite du livret. Plusieurs Équipements peuvent déjà se défausser eux-mêmes; le manque à traiter concerne surtout l’interaction adverse avec les Équipements en jeu.

### Action

S’assurer que le set de cartes imprimées contient explicitement des Tactiques portant un effet tel que :

> Détruisez un Équipement cible.

Si aucun retrait d’Équipement indépendant de l’Appareil porteur n’est finalement conservé, réécrire la règle pour ne décrire que les cas réellement possibles. La suppression de la mention générique ne doit toutefois être envisagée qu’après l’audit des effets d’auto-défausse déjà présents.

### Validation attendue

- inventorier les effets qui défaussent ou détruisent un Équipement;
- garantir au moins une réponse clairement identifiable dans le set imprimé si le retrait ciblé est retenu;
- synchroniser chaque texte modifié entre le catalogue Markdown et le CSV.

## 6. Amélioration de la construction de deck

**Statut : décision de format requise.**

### Problématique

La limite de 2 copies pour un deck de 60 cartes génère une variance importante et rend les synergies autour de Formation et Réseau moins fiables.

### Options proposées

1. réduire la taille du deck à **40 cartes** tout en réévaluant le nombre de Ressources et les starters;
2. conserver 60 cartes et autoriser un maximum de **3 ou 4 copies** d’une même carte non basique.

Chaque option doit améliorer la régularité des synergies et réduire la frustration liée aux tirages aléatoires sans rendre les parties trop répétitives.

### Décision attendue

Comparer les probabilités de tirage, la diversité des listes, le risque de combinaisons répétitives et le coût matériel des deux formats avant de modifier la règle de construction.

## Décision de licence

À compter de la version 0.1.2, les éléments originaux du projet sont distribués sous la **GNU General Public License version 3 uniquement**, identifiant SPDX `GPL-3.0-only`. Le texte complet figure dans [LICENSE](LICENSE). Les œuvres et marques de tiers restent soumises à leurs droits propres.

## Définition de terminé

Un chantier de règles n’est terminé que lorsque les éléments suivants sont alignés :

- le livret de règles et le guide de démarrage rapide;
- les cartes concernées dans les catalogues Markdown et CSV;
- les deux starters, si leur composition ou leur texte change;
- la référence d’équilibrage et les cas de non-régression;
- le rapport de validation et le journal des changements.
