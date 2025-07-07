# Plan de test

## Environnement de test

- Base de données
- API
- Client
- Navigateurs : Brave, Google Chrome, Mozilla Firefox, Microsoft Edge

## Fonctionnalités testés

- Opérations CRUD
- Authentification : Connexion et inscription
- Composants métiers
- Aspects de sécurité
- Persistance de données
- Gestion des routes

## Stratégie de test

| Type de Test        | Fonctionnalités                                                                |
| ------------------- | ------------------------------------------------------------------------------ |
| Tests unitaires     | Opérations CRUD, logique métier, sécurité, repository, service                 |
| Tests d’intégration | Opérations CRUD, logique métier, authentification, repository, service         |
| Tests E2E           | Parcours utilisateur : navigation + inscription + participation à un événement |

## Critères d'acceptation

- Aucun test critique ne doit échouer.
- Les tests E2E doivent refléter les parcours utilisateurs principaux sans interruption.
- Les tests doivent être reproductibles dans tous les environnements.
- Les données sensibles doivent être protégées.

## Tableau de tests

| ID du test | Type de test       | Description                                                                                                                     | Résultat attendu                                                                        | Ressources | Priorité |
| ---------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | ---------- | -------- |
| TU-01      | Test Unitaire      | Création d'un article                                                                                                           | L'article est bien crée contenant les mes informations entrés                           | PHPUnit    | Moyenne  |
| TI-01      | Test d'Intégration | Création d'un compte utilisateur                                                                                                | Le compte crée à bien comme rôle utilisateur et contient toutes les informations entrés | PHPUnit    | Élevé    |
| TE2E-01    | Test End to End    | Depuis la page d'accueil naviguer vers la page login, se login(redirection vers l'accueil) puis naviguer vers sa page de profil | Chargement des pages et parcours utilisateur fonctionnel                                | PHPUnit    | Élevé    |
