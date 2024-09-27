### Diagramme de Séquence

#### Objectif
Le **diagramme de séquence** fait partie des diagrammes comportementaux de l'UML. Son objectif est de modéliser les **interactions temporelles** entre les objets et les acteurs d'un système. Il représente la **chronologie des échanges de messages**, c’est-à-dire la manière dont les objets communiquent entre eux et avec les acteurs au fil du temps pour réaliser un cas d'utilisation spécifique ou une fonctionnalité donnée.

- Il est utilisé pour décrire **le comportement dynamique** du système.
- Il aide à comprendre comment un scénario particulier se déroule en mettant en évidence l’ordre des interactions.

#### Éléments Clés du Diagramme de Séquence

1. **Acteurs et Objets (Instances)** :
   - Les **acteurs** représentent les entités externes qui interagissent avec le système (utilisateurs, systèmes externes, appareils).
   - Les **objets** sont des instances des classes du système qui participent à l’interaction. Un objet est une **instance d’une classe** modélisée dans le **diagramme de classes**.
   - Les objets et les acteurs sont disposés horizontalement en haut du diagramme sous forme de **rectangles**. Chacun possède une **ligne de vie** verticale qui montre l'existence de l'objet pendant la durée de l'interaction.

2. **Messages** :
   - Les messages sont les **interactions** entre les objets et les acteurs, qui peuvent représenter des **appels de méthodes** ou des **demandes d'information**.
   - Les messages sont représentés par des flèches horizontales entre les lignes de vie des objets/acteurs.
   
   Il existe deux types de messages :
   
   - **Message synchrone** : L'émetteur est bloqué tant qu'il n'a pas reçu de réponse. Il est représenté par une flèche pleine avec une pointe solide. Cela signifie que l'émetteur attend que le destinataire exécute une opération avant de continuer.
   - **Message asynchrone** : L'émetteur envoie un message sans attendre de réponse et continue son exécution. Ce type de message est représenté par une flèche avec une pointe ouverte.
   
   Chaque message est envoyé **chronologiquement**, de haut en bas sur le diagramme.

3. **Création et Destruction d'Objets** :
   - La **création** d'un objet est souvent déclenchée par un message particulier. Elle est représentée par une flèche dirigée vers l'objet, et sa ligne de vie commence à ce moment-là.
   - La **destruction** d’un objet est montrée par une croix à la fin de sa ligne de vie, indiquant que l'objet cesse d'exister après cette interaction.

4. **Boucles** :
   - Une **boucle** modélise une répétition d’interactions. Elle est utilisée pour montrer qu’un ensemble de messages est envoyé plusieurs fois.
   - La boucle est représentée par un **bloc de boucle** (marqué "loop") qui encadre les messages répétés, avec une condition de répétition indiquée (par exemple : "pour chaque client").

5. **Alternatives (alt)** :
   - Une alternative est utilisée pour modéliser des **choix conditionnels** dans l'envoi de messages. Cela permet de représenter différents scénarios qui peuvent se dérouler en fonction d'une condition.
   - Elle est représentée par un **bloc "alt"** qui divise le diagramme en plusieurs sections, chacune représentant un chemin alternatif d'exécution en fonction des conditions.

6. **Références** :
   - Il est possible de faire référence à d'autres diagrammes de séquence pour éviter de surcharger un diagramme. Cette référence est représentée par un bloc "ref".

#### Règles

1. **Messages avec Acteurs** :
   - Les messages échangés entre les **acteurs** (entités externes) et le système représentent généralement des **opérations simulées** ou **superficielles**. Ces messages sont liés aux **cas d’utilisation**, et leur contenu est souvent simple (par exemple : entrée de texte, sélection d’une option).
   - Ce type de message ne décrit pas la logique interne du système, mais plutôt les interactions à son interface externe.

2. **Messages Internes (Objets du Système)** :
   - Les messages échangés entre les **objets internes** du système correspondent à des **opérations réelles** définies dans le **diagramme de classes**. Ces opérations décrivent la manière dont les objets collaborent pour réaliser une fonctionnalité spécifique.
   - Si un objet A envoie un message à un objet B, alors le **diagramme de classes** doit définir une **opération** dans la classe de B qui correspond à ce message.

#### Exemples de Notation

- **Message synchrone** :  
   - Objet A → [Message synchrone] → Objet B  
   - L’émetteur attend la fin de l'opération sur l'objet B avant de continuer son exécution.

- **Message asynchrone** :  
   - Acteur → [Message asynchrone] → Objet C  
   - L’acteur continue son exécution sans attendre que l’opération sur C se termine.

- **Création d'objet** :  
   - Acteur → [Message créant un objet] → Nouvel Objet  
   - La ligne de vie du nouvel objet démarre à partir de ce message.

- **Boucle** :  
   - Bloc "loop" englobant plusieurs messages pour représenter la répétition d'une séquence.

- **Alternative (alt)** :  
   - Bloc "alt" divisant les messages selon des conditions pour illustrer les différents scénarios possibles.

#### Utilisation en Conception
Le **diagramme de séquence** est particulièrement utile en phase de conception pour décrire **comment les cas d'utilisation** sont réalisés en interne. Il permet aux développeurs de visualiser comment les objets communiquent entre eux à travers des messages, et il aide à clarifier l'ordre exact des interactions pour résoudre des problèmes complexes comme les dépendances, les conditions ou les répétitions.

![[sequence_1.png]]![[sequence_2.png]]![[sequence_3.png]]![[sequence_4.png]]![[sequence_5.png]]![[sequence_6.png]]![[sequence_7.png]]![[sequence_8.png]]![[sequence_9.png]]![[sequence_10.png]]![[sequence_11.png]]![[sequence_12.png]]![[sequence_13.png]]