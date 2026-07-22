# Projet examen Symfony:
Nom: RASAMIMANANA
Prénom: Heritiana Hiarilala
Classe: L1C
Matricule: 399/LA-25-26
Sujet choisi: sujet1 (Gestion des Étudiants)

Démarches Techniques et Architecture du Projet:
Pour réaliser ce projet de gestion des étudiants, voici les étapes que j'ai suivies

1.Mise en place de la base de données et de l'entité :**
   -J'ai créé l'entité `Student` pour définir la structure des données d'un étudiant (nom, prénom, e-mail, filière, matricule).
   -J'ai exécuté les commandes de migration Doctrine (`make:migration` puis `doctrine:migrations:migrate`) pour générer automatiquement la table correspondante dans la base de données SQL.

2.Développement du contrôleur (StudentController) :
    J'ai mis en place les différentes méthodes du CRUD :
     -"Affichage": Récupération de la liste des étudiants depuis la base de données avec le `StudentRepository` pour les afficher dans le tableau.
     -"Ajout": Traitement du formulaire de création et enregistrement dans la base avec l'`EntityManager`.
     -"Modification": Récupération de l'étudiant sélectionné, pré-remplissage du formulaire et sauvegarde des modifications.
     -"Suppression": Suppression de l'étudiant en base selon son identifiant.

3.Intégration des vues Twig:
   -J'ai utilisé le moteur de rendu Twig dans le dossier `templates/student/`.
   -J'ai lié le fichier `base.html.twig` pour garder la même structure de page partout.
   -J'ai créé les pages `index.html.twig`, `new.html.twig`, `edit.html.twig` et `show.html.twig` en utilisant Bootstrap pour avoir des formulaires et un tableau lisibles.

4.Pour démarrer le serveur local:
     `php -S localhost:8000 -t public`