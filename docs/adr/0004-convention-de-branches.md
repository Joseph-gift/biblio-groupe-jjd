# ADR 0004 : convention de nommage des branches

- Statut : proposé
- Date : 2026-10-05
- Décideurs : @Joseph-gift, @Darwiks, @intox24

## Contexte
Plusieurs bénévoles modifient Biblio en même temps. Chacun part d'une issue, crée une branche, puis ouvre une pull request.
Sans règle commune, la liste des branches ne dit ni le type de travail ni l'issue concernée. Retrouver « qui corrige quoi » devient long, surtout pour des bénévoles qui ne travaillent pas sur le projet tous les jours.

## Options envisagées
1. Nom libre (`correction`, `joseph`, `ma-branche`).
   Pour : rien à retenir, chacun choisit un nom tout de suite.
   Contre : la liste des branches ne permet pas de retrouver l'issue, ni de distinguer un correctif d'une documentation.
2. Convention `type/<n°>-mots-cles` (`fix/1-recherche`, `docs/12-readme`).
   Pour : le type et le numéro d'issue se lisent dans le nom. On retrouve l'issue en un coup d'œil.
   Contre : il faut connaître la règle avant de créer la branche. Un nom hors format redevient illisible.

## Décision
Chaque branche de Biblio suit le modèle `type/<n°>-mots-cles`.

## Conséquences
Plus facile : lire la liste des branches, retrouver l'issue, et voir s'il s'agit d'un correctif (`fix/`) ou de documentation (`docs/`).
Plus difficile : il faut retenir la convention, et un nom libre ne suffit plus pour qu'un camarade comprenne le travail en cours.
À surveiller : si un nouveau type de travail apparaît (par exemple `feat/`), mettre à jour cette convention dans le README, section Contribuer.