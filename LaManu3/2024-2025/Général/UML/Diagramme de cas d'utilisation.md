Voici un développement plus approfondi de la section concernant le **diagramme de cas d'utilisation** :

---

### Diagramme de Cas d'Utilisation

#### Objectif
Le **diagramme de cas d'utilisation** est un outil fondamental pour comprendre les besoins fonctionnels d'un système logiciel. Il permet de capturer les exigences du point de vue des utilisateurs et autres entités qui interagissent avec le système. Ce diagramme aide à élaborer un **cahier des charges fonctionnel**, qui décrit de manière détaillée les fonctionnalités du système du point de vue de ses utilisateurs finaux.

#### Questions Clés :
Pour définir un cas d'utilisation, trois questions principales doivent être posées :
1. **Utilisation** : À quoi sert le système ? Quelles sont ses utilisations principales ?
   - Il s'agit d'identifier les actions ou les services que le système doit fournir à ses utilisateurs, en fonction de leurs besoins.
2. **Acteurs** : Qui va utiliser ou interagir avec le système ?
   - Les acteurs sont les entités externes qui interagissent avec le système. Il peut s'agir d'utilisateurs humains, d'autres systèmes, ou même de dispositifs matériels.
3. **Limites** : Où s’arrête la responsabilité du système ?
   - Les limites du système permettent de définir ce qui fait partie du système et ce qui en est extérieur. Cela permet de clarifier les responsabilités du système vis-à-vis de son environnement.

#### Définition
- Un **cas d'utilisation** est un ensemble de **scénarios** décrivant la manière dont un utilisateur interagit avec le système pour atteindre un **objectif précis**.
- Il donne une **vue extérieure** du système, en se concentrant sur ce qu'il fait, plutôt que sur comment il le fait.
  
##### Acteur
- Un **acteur** représente toute entité externe (personne, système, objet) qui interagit avec le système.
- **Types d'acteurs** :
  - **Acteur principal** : Celui qui déclenche un cas d'utilisation.
  - **Acteur secondaire** : Celui qui soutient ou interagit indirectement avec le cas d'utilisation.
- Un acteur peut être un humain, un système externe ou un autre matériel interagissant avec le logiciel.
  
##### Association
- L'**association** est le lien entre un acteur et un cas d'utilisation. Elle représente la **capacité** d'un acteur à déclencher une action dans le système.

#### Relations entre Cas d'Utilisation
Dans les diagrammes de cas d’utilisation, des relations spécifiques entre les cas peuvent être modélisées pour refléter la **dépendance** ou la **réutilisation** de scénarios entre eux.

1. **Généralisation** :
   - Il s'agit d'une relation hiérarchique où un cas d'utilisation **spécifique** hérite des caractéristiques d'un cas d'utilisation **plus général**.
   - **Exemple** : Le cas d'utilisation "Réserver un vol international" peut être un cas particulier du cas "Réserver un vol", qui est plus général.
   - Le cas d'utilisation spécifique (sous-cas) hérite de toutes les étapes du cas général, mais peut aussi ajouter des étapes ou des variantes spécifiques à son contexte.

2. **Extension** :
   - Cette relation signifie qu'un cas d'utilisation **X** peut être **optionnellement déclenché** au cours du scénario d'un autre cas d'utilisation **Y**.
   - **Exemple** : Le cas "Payer par carte" peut étendre "Acheter un produit", car le paiement par carte est une étape optionnelle dans le processus d'achat.
   - Cette relation permet de modéliser des **scénarios alternatifs** ou des actions qui ne sont pas systématiquement exécutées.

3. **Inclusion** :
   - Le cas d'utilisation **Y** est **inclus** dans un autre cas d'utilisation **X** lorsqu'il s'agit d'une étape récurrente ou nécessaire au sein d'un autre scénario.
   - **Exemple** : "Se connecter" peut être inclus dans "Acheter un produit", car l'utilisateur doit se connecter avant de procéder à un achat.
   - Cette relation permet de réutiliser un **même ensemble d'étapes** dans plusieurs cas d'utilisation, facilitant la gestion des scénarios communs.

#### Conseils pour les Diagrammes de Cas d'Utilisation

- **Limiter le nombre de cas par diagramme** :
  - Il est conseillé de ne pas inclure plus de **6 à 8 cas d’utilisation** dans un même diagramme. Un nombre trop important peut rendre le diagramme **illisible** et difficile à interpréter.
  
- **Créer plusieurs diagrammes si nécessaire** :
  - Si le système comporte de nombreux cas d'utilisation, ou si différents acteurs interviennent dans des parties distinctes du système, il est préférable de diviser les cas en **plusieurs diagrammes** pour assurer une **meilleure lisibilité**.
  - Par exemple, un diagramme spécifique pour les **actions des clients** et un autre pour les **actions des administrateurs** du système.

- **Relations uniquement si nécessaire** :
  - Utilisez les relations (**généralisation**, **inclusion**, **extension**) uniquement si elles apportent une valeur supplémentaire à la compréhension du diagramme.
  - Trop de relations complexes peuvent rendre le diagramme **lourd et confus**. Il est important de rester simple et de modéliser uniquement les interactions nécessaires.

![[use_case_1.png]]![[use_case_2.png]]![[use_case_3.png]]![[use_case_4.png]]![[use_case_5.png]]![[use_case_6.png]]![[use_case_7.png]]![[use_case_8.png]]![[use_case_9.png]]![[use_case_10.png]]![[use_case_11.png]]![[use_case_12.png]]![[use_case_13.png]]![[use_case_13.png]]![[use_case_13.png]]![[use_case_14.png]]![[use_case_15.png]]