# Spécification technique — v0.1

## Objectif

Construire progressivement un orchestrateur multi-agents capable de contribuer à plusieurs projets de jeux vidéo, sans dépendre d'un moteur unique.

## Exigences fonctionnelles

- Enregistrer un brief de jeu versionné.
- Décomposer un objectif en tâches courtes et vérifiables.
- Affecter chaque tâche à un agent adapté.
- Exiger des résultats structurés.
- Vérifier les critères d'acceptation.
- Limiter le nombre de tentatives automatiques.
- Conserver un journal des actions et décisions.
- Détecter les tâches bloquées et demander une intervention.
- Utiliser des adaptateurs distincts pour chaque moteur.

## Exigences non fonctionnelles

- Fonctionnement local au départ.
- Aucun abonnement ou appel API requis pour le premier prototype.
- Configuration séparée du code.
- Gestion claire des erreurs.
- Tests automatisés.
- Aucune clé API ou donnée sensible dans Git.

## Objets de données

### Project
- `id`
- `name`
- `description`
- `engine`
- `constraints`
- `status`

### Task
- `id`
- `project_id`
- `title`
- `description`
- `assigned_agent`
- `acceptance_criteria`
- `status`
- `attempts`

### AgentResult
- `task_id`
- `status`
- `summary`
- `artifacts`
- `issues`
- `next_steps`

### AuditEvent
- `timestamp`
- `actor`
- `action`
- `target`
- `result`

## Première preuve de concept

Avant d'appeler de vrais modèles, créer un prototype avec des agents simulés. Il doit démontrer la création de tâches, leur attribution, le retour de résultats, la revue du Manager et la journalisation.

## Critères d'acceptation du prototype

- Une demande simple produit plusieurs tâches.
- Chaque tâche reçoit un agent compétent.
- Un résultat incomplet est refusé ou renvoyé en correction.
- Les tentatives sont plafonnées.
- Chaque transition de statut est journalisée.
