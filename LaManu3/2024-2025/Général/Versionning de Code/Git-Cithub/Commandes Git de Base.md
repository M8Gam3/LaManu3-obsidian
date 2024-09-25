---
tags:
  - VersionningDeCode
---
### 1. Commandes de Base de Git

#### a. `git init`

- **Description** : Initialise un nouveau dépôt Git.
  
- **Utilisation** :
```bash
git init nom_du_projet
```

- **Exemple** : Crée un nouveau dépôt dans un dossier appelé `mon_projet` :
```bash
mkdir mon_projet 
cd mon_projet 
git init
```

#### b. `git add`

- **Description** : Ajoute des fichiers à la zone de transit (staging).
  
- **Utilisation** :
```bash
git add nom_du_fichier
```

- **Exemple** : Ajoute un fichier appelé `index.html` :
```bash
git add index.html
```

- **Astuce** : Pour ajouter tous les fichiers modifiés, utilisez `git add .`.

#### c. `git commit`

- **Description** : Enregistre les modifications dans l'historique du projet.
- **Utilisation** :
```bash
git commit -m "Message de commit"
```

- **Exemple** :
```
git commit -m "Ajout de la page d'accueil"
```

#### d. `git push`

- **Description** : Envoie les commits locaux vers un dépôt distant.
- **Utilisation** :
```bash
git push origin nom_de_la_branche
```

- **Exemple** : Pousse les modifications vers la branche `main` du dépôt distant :
```bash
git push origin main
```

#### e. `git pull`

- **Description** : Récupère les modifications du dépôt distant et les fusionne dans la branche locale.
- **Utilisation** :
```bash
git pull origin nom_de_la_branche
```

- **Exemple** : Met à jour la branche locale `main` avec les dernières modifications :
```bash
git pull origin main
```

### 2. Conseils pour l'Efficacité

#### a. Alias Git

Les alias permettent de raccourcir les commandes Git fréquentes. Vous pouvez définir des alias dans votre fichier de configuration Git (`.gitconfig`).

- **Exemple d'alias** :
```bash
git config --global alias.co checkout 
git config --global alias.br branch 
git config --global alias.ci commit 
git config --global alias.st status
```

- **Utilisation** : Après avoir défini ces alias, vous pouvez utiliser :
```bash
git co nom_de_branche  # Pour changer de branche
git ci -m "Message"    # Pour committer
git st                 # Pour voir le statut
```

#### b. Scripts Personnalisés

Les scripts permettent d'automatiser des séquences de commandes Git. Cela peut être particulièrement utile pour des tâches répétitives.

- **Exemple de script** : Créez un script bash appelé `git-update.sh` pour mettre à jour votre dépôt :
```bash
#!/bin/bash
git pull origin main
git add .
git commit -m "Mise à jour automatique"
git push origin main
```

- **Utilisation** : Rendez le script exécutable et exécutez-le :
```bash
chmod +x git-update.sh
./git-update.sh
```
