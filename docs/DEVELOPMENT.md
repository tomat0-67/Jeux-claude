# Développement local

## État actuel

Cette archive contient le cadrage et la structure documentaire. Elle ne contient pas encore l'orchestrateur exécutable.

## Prérequis envisagés

- Un ordinateur sous Windows, Linux ou macOS.
- Git pour versionner le projet.
- Python pourra être évalué comme langage de l'orchestrateur, mais ce choix n'est pas encore définitif.

## Première étape

Le premier prototype doit fonctionner sans clé API : tâches et agents simulés, validation des résultats, journalisation et tests. Cela permettra de tester l'architecture avant d'ajouter des coûts ou des dépendances externes.

## Règles Git

- Ne jamais committer de clé API, mot de passe ou jeton.
- Utiliser un fichier `.env` local ignoré par Git si des secrets deviennent nécessaires.
- Garder les journaux volumineux et fichiers temporaires hors du dépôt.
- Faire des commits petits et descriptifs.
