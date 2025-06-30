# Plan de test

## Environnement de test

- Base de données
- API
- Client
- Navigateurs : Brave, Google Chrome, Mozilla Firefox

## Fonctionnalités testés

- Opérations CRUD
- Authentification : Connexion et inscription
- Composants métier
- Aspects de sécurité
- Persistance de données
- Gestion des routes

## Stratégie de test

| Type de Test        | Fonctionnalités                                                   |
| ------------------- | ----------------------------------------------------------------- |
| Tests unitaires     | Opérations CRUD, logique métier                                   |
| Tests d’intégration | Authentification (login/register), navigation                     |
| Tests E2E           | Parcours utilisateur : inscription + participation à un événement |

## Critères d'acceptation

- Aucun test critique ne doit échouer.
- Les tests E2E doivent refléter les parcours utilisateurs principaux sans interruption.
- Les tests doivent être reproductibles dans tous les environnements.
- Les données sensibles doivent être protégées.

## Tableau de tests

| ID du test | Type de test  | Description                              | Résultat attendu                             | Ressources | Priorité |
| ---------- | ------------- | ---------------------------------------- | -------------------------------------------- | ---------- | -------- |
| T1         | Test unitaire | Vérifier la participation à un événement | L’utilisateur est bien inscrit à l’événement | PHPUnit    | Moyenne  |
