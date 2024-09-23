### 1. Composants de Git

#### Répertoire de travail

- **Définition** : Le répertoire de travail est l'espace sur votre disque où se trouvent tous les fichiers du projet. C'est l'endroit où vous effectuez vos modifications et tests.
- **État des fichiers** :
    - **Modifiés** : Fichiers qui ont été modifiés depuis le dernier commit.
    - **Non suivis** : Nouveaux fichiers qui ne sont pas encore sous contrôle de version.
    - **Suivis** : Fichiers qui sont déjà suivis par Git et qui peuvent avoir des modifications.
- **Interactions** : Lorsque vous modifiez un fichier, il passe de l'état "suivi" à "modifié". Git permet de garder une trace de ces changements avant qu'ils ne soient validés dans l'historique du projet.

#### Zone de transit (staging)

- **Rôle** : La zone de transit sert d'espace intermédiaire entre le répertoire de travail et le dépôt local. Elle permet de préparer les modifications que vous souhaitez inclure dans le prochain commit.
- **Fonctionnement** :
    - Lorsque vous exécutez la commande `git add <fichier>`, vous déplacez le fichier de l'état "modifié" à "staging". Cela signifie qu'il est prêt à être enregistré dans l'historique du projet.
    - Vous pouvez sélectionner spécifiquement les fichiers ou les modifications à inclure dans le commit, ce qui vous donne un contrôle précis sur ce que vous validez.

#### Dépôt local

- **Importance** : Le dépôt local contient l'historique complet des versions de votre projet, avec chaque commit enregistré. Cela vous permet de revenir à des versions précédentes, d'analyser les changements et de collaborer efficacement.
- **Fonctionnalités** :
    - **Historique** : Chaque commit est lié à un identifiant unique (hash) et contient des métadonnées, comme l'auteur, la date, et un message descriptif.
    - **Branches** : Le dépôt local permet également de créer et de gérer des branches, facilitant le développement parallèle et la gestion des fonctionnalités.

### 2. Processus de Commit

#### Étapes d’un commit

1. **Ajout** (`git add`):
    
    - Vous sélectionnez les fichiers que vous souhaitez inclure dans le prochain commit. Cela peut être fait pour un fichier unique, plusieurs fichiers ou même tous les fichiers modifiés (en utilisant `git add .`).
    - Cette étape prépare les fichiers pour l'enregistrement, en les déplaçant de l'état "modifié" à "staging".
2. **Validation** (`git commit`):
    
    - Une fois que vous avez ajouté les fichiers à la zone de transit, vous exécutez `git commit -m "Votre message de commit"` pour enregistrer les modifications dans le dépôt local.
    - Il est important d'écrire un message de commit clair et concis, décrivant les changements effectués. Cela aide à maintenir un historique de projet compréhensible.
3. **Suivi des modifications** :
    
    - Après un commit, Git enregistre un instantané de votre projet. Vous pouvez vérifier l'historique des commits à tout moment en utilisant `git log`, ce qui vous permet de visualiser les changements apportés au fil du temps.
    - Vous pouvez également revenir à des versions antérieures avec des commandes comme `git checkout <commit_hash>` pour explorer ou restaurer un état précédent.