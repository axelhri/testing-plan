# Fondamentaux des Tests et Plan de Test

## 1. Importance des Tests dans le Cycle de Vie Logiciel

- Garantir la **qualité** du logiciel.
- Détecter les **bugs tôt** pour réduire les coûts.
- Faciliter la **maintenance** et les refactorings.
- Renforcer la **confiance** lors des mises en production.

---

## 2. La Pyramide des Tests

Un modèle pour équilibrer les différents types de tests :

```js
     End-to-End (E2E)
        ↑ Moins nombreux
   Tests d’intégration
        ↑
   Tests unitaires
        ↑ Très nombreux

```

- **Tests Unitaires** : testent une fonction/méthode isolée.
- **Tests d’Intégration** : testent la communication entre modules.
- **Tests End-to-End (E2E)** : testent le comportement complet de l'application via l'interface utilisateur.

---

## 3. Vocabulaire Essentiel

- **Test Case** : un scénario de test (input + action + résultat attendu).
- **Test Suite** : un groupe de cas de test.
- **Test Runner** : outil pour exécuter les tests (ex : Jest, PyTest, JUnit).
- **Assertion** : vérifie qu'une condition est vraie (ex : `assert result == expected`).
- **Fixture** : ensemble de données/états préparés avant l’exécution d’un test.
- **Mock** : objet simulé pour isoler le SUT (System Under Test).
- **Stub** : version simplifiée d’un composant externe (retourne des valeurs fixes).
- **SUT (System Under Test)** : la partie du logiciel qu’on est en train de tester.

---

## 4. Bonnes Pratiques de Test

### Structure d’un test

- **Arrange – Act – Assert** :

  1. **Arrange** : préparer les données/états.
  2. **Act** : exécuter l’action à tester.
  3. **Assert** : vérifier le résultat.

- **Given – When – Then** (BDD) :
  - _Given_ un état initial,
  - _When_ une action est effectuée,
  - _Then_ un résultat est attendu.

### Tests de Qualité

- **Isolés** : ne dépendent pas d’autres tests ou de ressources externes.
- **Indépendants** : leur ordre d’exécution ne doit pas affecter les résultats.
- **Reproductibles** : doivent produire le même résultat à chaque exécution.
