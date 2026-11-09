# Jeux Claude

Projet de système multi-agents destiné à concevoir, développer et tester plusieurs jeux vidéo avec l'aide d'agents d'intelligence artificielle spécialisés.

## Objectif

Construire une architecture indépendante du moteur de jeu, capable de coordonner plusieurs agents spécialisés sous la supervision d'un agent Manager.

Le projet vise une forte autonomie pour les tâches internes de développement, avec journalisation des actions et validation des résultats.

## Principes

- Un agent Manager planifie le travail, distribue les tâches et contrôle les résultats.
- Des agents spécialisés prennent en charge la conception, le développement, les graphismes, le son et les tests.
- Le cœur du système reste indépendant des moteurs de jeu.
- Des adaptateurs dédiés assurent la communication avec chaque moteur pris en charge.
- Les tâches, décisions, erreurs et révisions sont journalisées.
- Les tentatives automatiques sont limitées et les erreurs non résolues sont remontées.

## Limites d'autonomie

Les agents peuvent travailler de manière autonome dans l'espace de travail du projet : créer et modifier des fichiers, lancer des tests autorisés, corriger leur travail et documenter leurs résultats.

Une validation humaine reste nécessaire avant toute publication, dépense, modification de compte externe, utilisation de secrets ou identifiants, suppression irréversible, ou modification importante du périmètre du projet.

## État actuel

Le projet est au stade de cadrage. Le langage principal et le premier moteur à intégrer ne sont pas encore définis.

La première étape technique sera un prototype d'orchestration avec des agents simulés, avant de connecter des modèles d'IA et des moteurs de jeu.

## Documentation

- [Architecture](docs/ARCHITECTURE.md)
- [Spécification technique](docs/TECHNICAL_SPEC.md)
- [Rôles des agents](docs/AI_AGENTS.md)
- [Feuille de route](ROADMAP.md)

## Démarrage

La première version sera un prototype local, sans clé API ni service payant. Voir `docs/DEVELOPMENT.md`.
