# Plan de test

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

## Tableau de tests

| ID du test | Type de test  | Description                              | Ressources | Résultat attendu                             | Priorité |
| ---------- | ------------- | ---------------------------------------- | ---------- | -------------------------------------------- | -------- |
| T1         | Test unitaire | Vérifier la participation à un événement | PHPUnit    | L’utilisateur est bien inscrit à l’événement | Moyenne  |

## Critères d'acceptation

- Aucun test critique ne doit échouer.
- Les tests E2E doivent refléter les parcours utilisateurs principaux sans interruption.
- Les tests doivent être reproductibles dans tous les environnements.
- Les données sensibles doivent être protégées.
