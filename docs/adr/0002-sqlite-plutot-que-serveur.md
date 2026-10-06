# ADR 0000 : titre de la décision

- Statut : proposé
- Date : 2026-10-06
- Décideurs : Darwiks, Joseph-gift, intox24

## Contexte
<!-- La situation et la contrainte qui imposent de choisir. -->
Le projet Biblio doit être évalué et testé par d'autres étudiants sur des machines et des systèmes d'exploitation différents (Windows, macOS, Linux), sans imposer l'installation de services tiers ou d'environnements complexes.

## Options envisagées
1. Pour : Gestion parfaite des accès concurrents multi-utilisateurs et performances optimales pour de très gros volumes de données.
2. Contre : Nécessite d'installer, configurer et maintenir un serveur de base de données dédié ainsi que des dépendances Python supplémentaires via pip.

## Décision
<!-- L'option retenue, formulée clairement. -->
Nous choisissons SQLite pour stocker les données du projet Biblio dans un fichier local unique, sans dépendance externe.

## Conséquences
<!-- Ce que la décision rend plus facile, et ce qu'elle rend plus difficile. -->
Ce qui devient plus facile : L'installation pour un nouvel utilisateur.
Ce qui devient plus difficile : La consultation directe des données sans outil dédié.