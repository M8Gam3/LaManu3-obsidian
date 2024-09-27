## UML - Unified Modeling Language

### Définition
UML (Unified Modeling Language) est un langage de modélisation graphique standardisé, principalement utilisé en conception orientée objet. Il permet de visualiser la conception d'un système via des pictogrammes.

### Version actuelle
- **UML 2.5**

### Types de Diagrammes
UML comporte 14 types de diagrammes, répartis en deux catégories principales :
- **7 Diagrammes Structurels** :
  - Diagramme de classes
  - Diagramme d'objets
  - Diagramme de composants
  - Diagramme de déploiement
  - Diagramme des paquets
  - Diagramme de structure composite
  - Diagramme de profils
- **7 Diagrammes Comportementaux** :
  - Diagramme des cas d'utilisation
  - Diagramme états-transitions
  - Diagramme d'activité
  - Diagramme de séquence
  - Diagramme de communication
  - Diagramme global d'interaction
  - Diagramme de temps

---
### Diagrammes les plus utilisés
1. [[Diagramme de cas d'utilisation|Diagramme des cas d'utilisation]]
2. [[Diagramme de Séquence|Diagramme de séquence]]
3. [[Diagramme de Classes|Diagramme de classes]]
4. [[Diagramme de Déploiement|Diagramme de déploiement]]

---
### [[Diagramme de cas d'utilisation|Diagramme de cas d'utilisation]]
#### Objectif
Comprendre les besoins du client pour rédiger un cahier des charges fonctionnel.

#### Questions Clés :
1. **Utilisation** : À quoi sert-il ?
2. **Acteurs** : Qui va l'utiliser ou interagir avec lui ?
3. **Limites** : Où s’arrête sa responsabilité ?

#### Définition
- Ensemble de scénarios visant un objectif utilisateur.
- Vue extérieure des fonctionnalités principales.
- **Acteur** : Entité (personne, logiciel, objet) interagissant avec le système.
- **Association** : Relation entre acteur et cas d’utilisation.

#### Relations entre cas d’utilisation :
- **Généralisation** : X est un cas particulier de Y.
- **Extension** : X peut être déclenché pendant Y (optionnel).
- **Inclusion** : Y est inclus dans le scénario de X.

#### Conseils pour les diagrammes de cas d’utilisation :
- Ne pas inclure plus de 6 à 8 cas dans un diagramme.
- Diviser en plusieurs diagrammes si nécessaire.

---
### [[Diagramme de Séquence|Diagramme de Séquence]]
#### Objectif
Représenter les communications temporelles entre les objets et les acteurs, montrant la chronologie des messages.

#### Éléments clés :
- **Acteurs** et **objets (instances)**.
- **Messages** synchrones et asynchrones.
- Création/destruction d'objets, boucles, alternatives.

#### Règles
- Messages avec acteurs = opérations simulées.
- Messages internes = opérations définies dans le diagramme de classes.

---
### [[Diagramme de Classes|Diagramme de Classes]]
#### Objectif
Représenter la structure interne d’un logiciel, modéliser les objets et leurs relations.

#### Concepts :
- **Classe** : Regroupement d’objets partageant des attributs et opérations.
- **Objet** : Instance concrète ou abstraite avec identité, état, comportement.

#### Relations :
- **Association** : Relation entre deux classes (souvent binaire).
- **Hiérarchie** : Organisation en arborescence via spécialisation/généralisation.

#### Types de relations :
- **Agrégation faible** : Composants indépendants du composite.
- **Composition** : Composants dépendants du composite.

#### Contraintes
- **Attributs**, **Associations**, **Multiplicités** peuvent être contraints selon les besoins du cahier des charges.

---

### [[Diagramme de Déploiement|Diagramme de Déploiement]]

Le diagramme de déploiement est un **diagramme structurel** qui représente la disposition physique des ressources matérielles dans un système. Il montre comment les composants logiciels sont distribués sur ces ressources matérielles.

#### Objectifs
- Représenter la **disposition physique** des ressources matérielles (serveurs, ordinateurs, etc.) du système.
- Montrer la **répartition des composants logiciels** sur les différentes ressources matérielles.
- Décrire les **connexions de communication** entre ces ressources matérielles.

#### Éléments du Diagramme de Déploiement

1. **Nœuds** :
   - Un nœud représente une ressource matérielle du système, telle qu'un serveur ou une machine.
   - Chaque nœud possède généralement de la **mémoire** et parfois des **capacités de calcul**.
   - Représenté par un parallélépipède rectangle contenant son nom.
   - Un nœud peut avoir des **attributs** (comme la puissance de calcul ou la mémoire disponible).
   - Les composants logiciels sont associés aux nœuds, soit **placés à l'intérieur**, soit reliés par une **relation de dépendance** (flèche en pointillés).

2. **Chemins de Communication** :
   - Les nœuds sont connectés entre eux par des **lignes** représentant les supports de communication (réseaux, connexions filaires, etc.).

3. **Artefacts** :
   - Un artefact est un **élément concret** (document, fichier, exécutable, base de données) qui est déployé sur un nœud.
   - Il désigne tout élément produit au cours du développement (ex. : fichier exécutable, scripts, fichiers de configuration).

#### Exemple de Diagramme de Déploiement
Le diagramme de déploiement représente généralement un système distribué avec plusieurs nœuds (serveurs, bases de données) et leurs composants logiciels déployés (artefacts). Les connexions entre nœuds montrent les communications possibles entre ces entités.
