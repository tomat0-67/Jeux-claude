# Architecture

## Principe

Le système est organisé autour d'un noyau indépendant des moteurs de jeu. Le Manager transforme un objectif en tâches, les attribue aux agents, contrôle leurs livrables et décide de la suite.

## Composants

1. **Manager** — planification, priorités, suivi, revue et arbitrage.
2. **File de tâches** — tâches en attente, en cours, terminées ou bloquées.
3. **Agents spécialisés** — conception, programmation, graphismes, son et tests.
4. **Contrats de données** — formats communs pour les entrées, sorties et comptes rendus.
5. **Adaptateurs de moteur** — fonctions propres à Roblox, Unreal, Godot ou d'autres moteurs.
6. **Journalisation** — historique horodaté des tâches, résultats, erreurs et décisions.
7. **Contrôle des permissions** — blocage des opérations nécessitant une approbation humaine.

## Flux général

1. L'utilisateur définit le jeu et ses contraintes.
2. Le Manager crée un plan et des tâches atomiques.
3. Les agents reçoivent des tâches avec un objectif et des critères d'acceptation.
4. Chaque agent renvoie un résultat structuré et les fichiers produits.
5. Le Manager vérifie le résultat, demande une correction limitée ou valide la tâche.
6. Les tâches terminées alimentent les étapes suivantes.

## Architecture multi-moteurs

Le noyau ne doit pas contenir de logique spécifique à un moteur. Chaque adaptateur annonce les capacités qu'il prend en charge. Une opération non prise en charge doit produire un statut explicite, jamais un faux succès.

## Limites de sécurité

Les agents peuvent modifier les fichiers du projet et exécuter les tests autorisés dans un espace de travail dédié. La publication, les achats, les changements de comptes externes, l'accès aux secrets et les suppressions irréversibles nécessitent une approbation humaine.
