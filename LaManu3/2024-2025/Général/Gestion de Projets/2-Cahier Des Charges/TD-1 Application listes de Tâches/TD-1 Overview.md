### Cahier des Charges pour l'Application de Gestion de Tâches  
  
---  
  
#### **1. Contexte**  
L'objectif de ce projet est de développer une application de gestion de tâches permettant aux utilisateurs de créer des listes de tâches, d'ajouter des tâches, de les marquer comme terminées et de les supprimer. Le projet doit être réalisé dans un délai de 2 semaines par une équipe composée de 2 développeurs et d'un chef de projet. Cette application doit être simple, fonctionnelle et adaptée aux besoins des utilisateurs.  
  
---  
  
#### **2. Objectifs du Projet**  
L'application doit répondre aux besoins suivants :  
- Gestion des utilisateurs (création de compte, connexion/déconnexion).  
- Gestion de projets (création, modification, suppression, duplication).  
- Gestion de groupes de tâches et de tâches.  
- Attribution de ressources humaines aux projets, groupes de tâches et tâches.  
- Gestion des états des tâches.  
- Collaboration en temps réel et gestion des autorisations.  
  
---  
  
#### **3. Fonctionnalités de l'Application**  
  
##### **3.1. Authentification et Gestion des Utilisateurs**  
- **Créer un compte** : Les utilisateurs peuvent créer un compte en fournissant leur nom, prénom, adresse e-mail et un mot de passe sécurisé.  
- **Connexion/Déconnexion** : Les utilisateurs peuvent se connecter et se déconnecter de l'application en utilisant leur adresse e-mail et leur mot de passe (crypté).  
- **Voir les informations de son compte** : Chaque utilisateur peut visualiser ses informations personnelles, telles que son nom, prénom et e-mail.  
  
##### **3.2. Gestion des Projets**  
- **Créer un projet** : Un utilisateur peut créer un projet en lui attribuant un nom, une description et un état (actif, inactif, terminé).  
- **Modifier un projet** : Les utilisateurs peuvent modifier les informations d’un projet.  
- **Supprimer un projet** : Les utilisateurs peuvent supprimer un projet s'ils en sont le propriétaire.  
- **Dupliquer un projet** : Un utilisateur peut dupliquer un projet existant pour en créer une copie avec les mêmes paramètres de base.  
- **Inviter des membres** : Un propriétaire de projet peut inviter d'autres utilisateurs à rejoindre le projet avec des permissions (lecteur/éditeur).  
  
##### **3.3. Gestion des Groupes de Tâches**  
- **Créer un groupe de tâches** : Un utilisateur peut créer un groupe de tâches dans un projet donné avec un nom, une description et un état (à faire, en cours, en attente, terminé).  
- **Modifier un groupe de tâches** : Les informations du groupe de tâches peuvent être modifiées.  
- **Supprimer un groupe de tâches** : Un utilisateur peut supprimer un groupe de tâches du projet.  
- **Attribution des ressources humaines** : Un utilisateur peut affecter des membres à un groupe de tâches.  
  
##### **3.4. Gestion des Tâches**  
- **Créer une tâche** : Une tâche peut être créée au sein d’un groupe de tâches, avec un nom, une description et un état.  
- **Modifier une tâche** : Un utilisateur peut modifier les informations d'une tâche.  
- **Supprimer une tâche** : Un utilisateur peut supprimer une tâche.  
- **Attribuer des ressources humaines à une tâche** : Les membres d’un projet peuvent être affectés à une tâche spécifique pour gérer sa réalisation.  
  
##### **3.5. Gestion des États**  
- **Créer un état** : L’application permet de créer de nouveaux états pour les tâches (ex. : En cours, À faire, Terminé, etc.).  
- **Modifier un état** : Les états existants peuvent être modifiés.  
- **Supprimer un état** : Les utilisateurs peuvent supprimer des états inutilisés.  
  
##### **3.6. Feuille Blanche**  
- **Création d’une feuille blanche** : Chaque projet dispose d'une feuille blanche où les utilisateurs peuvent ajouter du texte libre.  
- **Modifier/Supprimer la feuille blanche** : Le texte dans la feuille blanche peut être modifié ou supprimé à tout moment.  
  
---  
  
#### **4. Cas d'Utilisation**  
| Cas d'Utilisation                | Description                                                                                   | Acteurs     |     |
| -------------------------------- | --------------------------------------------------------------------------------------------- | ----------- | --- |
| Inscription                      | Un utilisateur s'inscrit avec son email et un mot de passe.                                   | Utilisateur |     |
| Connexion                        | Un utilisateur se connecte pour accéder à ses projets.                                        | Utilisateur |     |
| Créer un projet                  | Un utilisateur peut créer un projet avec des informations basiques.                           | Utilisateur |     |
| Ajouter un groupe de tâches      | Un groupe de tâches peut être ajouté à un projet.                                             | Utilisateur |     |
| Ajouter une tâche                | Un utilisateur peut ajouter une tâche à un groupe de tâches.                                  | Utilisateur |     |
| Marquer une tâche comme terminée | L'utilisateur peut marquer une tâche comme terminée ou la faire passer à un autre état.       | Utilisateur |     |
| Inviter des membres              | Le propriétaire d'un projet peut inviter d'autres utilisateurs avec des permissions définies. | Utilisateur |     |
| Dupliquer un projet              | Un utilisateur peut dupliquer un projet existant.                                             | Utilisateur |     |
| Supprimer une tâche              | Un utilisateur peut supprimer une tâche d’un groupe.                                          | Utilisateur |     |
  
---  
  
#### **5. Spécifications Techniques**  
  
##### **5.1. Langage et Environnement**  
- **Langage de programmation** : L’application peut être développée en **JavaScript** (utilisant **Node.js** pour le backend et **React** pour le frontend).  
- **Framework** : Utilisation du Framework **Express.js** pour le backend.  
- **Base de données** : Base de données **MySQL** ou **PostgreSQL** pour stocker les informations des utilisateurs, projets, tâches, etc.  
- **Système de gestion de versions** : Utilisation de **Git** et de **GitHub** pour la gestion du code source et le versionnement du projet.  
  
##### **5.2. Sécurité**  
- **Authentification** : Utilisation de **JWT (JSON Web Token)** pour l’authentification des utilisateurs.  
- **Cryptage des mots de passe** : Utilisation de la bibliothèque **bcrypt** pour chiffrer les mots de passe avant de les stocker dans la base de données.  
- **Gestion des permissions** : Le propriétaire d'un projet peut attribuer des permissions (lecteur, éditeur) aux membres invités.  
  
##### **5.3. Synchronisation**  
- La synchronisation des données entre utilisateurs et projets sera assurée via des **API RESTful** et le protocole **WebSocket** pour des mises à jour en temps réel.  
- Une prise en charge de la synchronisation entre les utilisateurs dans le cadre d'un projet collaboratif sera mise en place.  
  
---  
  
#### **6. Sécurité et Gestion des Autorisations**  
- **Gestion des droits** : Seul le propriétaire d'un projet peut le modifier ou y ajouter des membres.  
- **Sécurisation des données** : Toutes les données des utilisateurs (projets, tâches, membres) seront protégées par des mécanismes de sécurité standard, y compris SSL pour les communications réseau et le stockage sécurisé des informations sensibles.  
  
---  
  
#### **[[TD-1 Gestion du Temps, Comment les 2 Semaines Sont Gérées et Utilisées|7. Délais et Livrables]]**
- **Durée** : Le développement de l’application doit être finalisé en **2 semaines**.  
- **Livrables** :  
- Cahier des charges (ce document).  
- Code source de l'application.  
- Documentation utilisateur.  
- Tests et validation des fonctionnalités.  
  
#### **Planification Globale sur 2 Semaines**

Pour garantir l'efficacité, le projet sera divisé en plusieurs phases avec des objectifs clairs pour chaque étape. Voici une proposition de répartition du temps :

- **Semaine 1** : Phase de conception et début du développement
    - **Jour 1-2** : Finalisation des spécifications fonctionnelles et techniques
    - **Jour 3-5** : Développement des fonctionnalités principales (gestion des projets et des tâches)
- **Semaine 2** : Finalisation du développement, tests et ajustements
    - **Jour 6-9** : Implémentation des fonctionnalités secondaires (sécurité, synchronisation)
    - **Jour 10-12** : Tests fonctionnels, ajustements, et correction de bugs
    - **Jour 13-14** : Révisions finales, validation et livraison du projet


---  

### [[TD-1 Estimation des Couts du Projet|8. Estimation du coût du projet]]

| Rôle                 | Taux Journalier | Jours | Coût Total  |
|----------------------|------------------|-------|-------------|
| Chef de Projet       | 400 €            | 10    | 4000 €      |
| Développeur Full-Stack 1 | 300 €        | 10    | 3000 €      |
| Développeur Full-Stack 2 | 300 €        | 10    | 3000 €      |
| **Total sans charges**     |                  |       | **10000 €** |
| **Charges (30%)**          |                  |       | **3000 €**  |
| **Total avec charges**     |                  |       | **13000 €** |

---

#### **9. Conclusion**  
Ce cahier des charges fournit un cadre détaillé pour le développement de l'application de gestion de tâches, couvrant à la fois les aspects fonctionnels et techniques. Il définit les fonctionnalités, les cas d’utilisation, les spécifications techniques et les mesures de sécurité pour assurer le succès du projet.
