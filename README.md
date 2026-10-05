# Biblio

Une application en ligne de commande pour gérer facilement le catalogue et les emprunts d'une bibliothèque, destinée aux gestionnaires et aux lecteurs.

## Prérequis

- Python 3.12 ou plus récent. Le module `sqlite3` est déjà inclus.
- Sous Windows : `python` ou `py`. Sous Linux et macOS : `python3`.
- Aucune installation `pip` n'est nécessaire.

## Installation

```text
git clone https://github.com/Joseph-gift/biblio-groupe-jjd.git
cd biblio-groupe-jjd
python biblio.py init
```

```text
Base initialisee : 6 livres, 3 membres.
```

Sous Windows, `py biblio.py init` fait la même chose. Sous Linux et macOS : `python3 biblio.py init`.

## Utilisation

`init` remet la base de départ. Lancez-le avant les autres commandes.

```text
python biblio.py init
```

```text
Base initialisee : 6 livres, 3 membres.
```
## Tests

```text
python -m unittest
```

```text
Base initialisee : 6 livres, 3 membres.
Emprunt enregistre : livre 3, membre 1.
.Base initialisee : 6 livres, 3 membres.
Erreur : livre 42 introuvable.
.Base initialisee : 6 livres, 3 membres.
Dune, emprunte par Alice Martin : 254 jours de retard
Fondation, emprunte par Bilal Haddad : 259 jours de retard
.Base initialisee : 6 livres, 3 membres.
[2] Dune (Frank Herbert)
.
----------------------------------------------------------------------
Ran 4 tests in 0.064s

OK
```

La durée (`0.064s`) varie d'une machine à l'autre. La dernière ligne doit être `OK`.

## Structure du projet

- `biblio.py` : commandes de la bibliothèque
- `tests/test_biblio.py` : tests
- `biblio.db` : base créée par `init`, ignorée par git
- `docs/` : documentation du groupe
- `exercices/` : énoncés de séance
- `.github/` : modèles d'issues, modèle de pull request, tests automatiques
- `README.md` : installation et utilisation

## Contribuer

Aucun push direct sur `main`. Tout changement passe par une pull request relue.

1. Ouvrir une issue avec le bon modèle : bug, évolution ou question. Noter son numéro.
2. Partir de `main` à jour, puis créer une branche :
   - `fix/<n°>-mot-cle` pour un correctif
   - `docs/<n°>-readme` pour la documentation
3. Modifier uniquement le sujet de l'issue. Commit avec un message clair, par exemple `fix: la recherche accepte une apostrophe`.
4. Pousser la branche et ouvrir une pull request. Dans la description : `Closes #<n°>`, les changements, l'impact et comment tester.
5. Choisir un camarade dans Reviewers. Il lit l'onglet Files changed, commente, puis Approve.
6. Merger la pull request et supprimer la branche. `Closes #<n°>` ferme l'issue.

## Auteurs

- Joseph-gift
- Darwiks
- intox24