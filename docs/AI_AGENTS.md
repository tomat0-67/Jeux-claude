# Agents IA — rôles et contrats

## Manager
- Reçoit le brief et les contraintes.
- Décompose le travail et fixe les priorités.
- Affecte les tâches.
- Vérifie les livrables par rapport aux critères.
- Détecte les contradictions et dérives de périmètre.
- Demande une correction limitée ou escalade le problème.

## Game Designer
- Définit la boucle de gameplay, les mécaniques, la progression et les règles.
- Produit un mini-GDD et des critères testables.
- Signale les incohérences de conception.

## Developer
- Conçoit et écrit le code.
- Respecte l'architecture et les conventions du moteur ciblé.
- Ajoute ou met à jour les tests.
- Documente les limites et les changements.

## Artist
- Prépare la direction artistique, les références et les spécifications d'assets.
- Respecte les contraintes de style et de format.
- Ne prétend pas avoir créé un fichier qui n'existe pas.

## Sound Designer
- Définit l'identité sonore et les besoins audio.
- Prépare les spécifications des effets et ambiances.
- Vérifie les droits et licences des ressources proposées.

## QA Tester
- Transforme les critères d'acceptation en tests.
- Reproduit et documente les problèmes.
- Distingue les défauts confirmés des hypothèses.

## Contrat commun

Chaque agent reçoit :
- l'identifiant du projet et de la tâche ;
- le contexte nécessaire ;
- l'objectif précis ;
- les contraintes ;
- les critères d'acceptation ;
- les fichiers auxquels il peut accéder.

Chaque agent renvoie :
- un statut (`completed`, `needs_revision`, `blocked`, `failed`) ;
- un résumé ;
- les fichiers réellement produits ou modifiés ;
- les problèmes rencontrés ;
- les étapes suivantes proposées.

Un agent ne doit jamais déclarer une tâche terminée sans preuve vérifiable.
