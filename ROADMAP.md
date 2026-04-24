# Roadmap - PROTOCOLE CLAUDE

> Backlog de référence du projet.
> Mis à jour à chaque chantier terminé ou réorienté.

Dernière mise à jour : 2026-04-24

---

## Contexte

Le repo porte la version générique du protocole, avec une intégration
Claude Code et l'outil `show_context.ps1`. Le cap actuel est de garder
le protocole canonique, l'onboarding Claude et les outils annexes alignés.

## Hypothèses retenues

- `README.md` sert de document maître opératif du repo.
- `PROTOCOLE.md` reste la source canonique à réinjecter dans Claude.
- `show_context.ps1` reste Windows / PowerShell tant qu'aucun portage n'est validé.

## État courant

- 2026-04-24 : cadrage de `gh` ajouté dans le protocole et l'intégration Claude.
- 2026-04-09 : auto-monitoring du contexte ajouté avec `show_context.ps1`.

## Priorités hautes

Format : `[ ]` à faire, `[~]` partiellement fait, `[x]` fait.

### [~] HP1 - Stabiliser l'intégration Claude

**Objectif** :
- Garder le protocole canonique, le README et `integrations/claude-code.md`
  strictement synchronisés.

**Actions** :
- Maintenir les règles d'usage des outils locaux (`show_context.ps1`, `gh`).
- Vérifier que l'intégration reste lisible pour un utilisateur non-développeur.

**Livrables** :
- `PROTOCOLE.md`, `README.md`, `integrations/claude-code.md`, `CHANGELOG.md`.

**Critère de fin** :
- Un utilisateur peut installer Claude + le protocole + `gh` sans exposer
  de token ni confondre workflow GitHub et sources de vérité du projet.

## Priorités moyennes

### [ ] MP1 - Porter le monitoring hors Windows

**Objectif** :
- Étendre `show_context.ps1` ou fournir un équivalent pour macOS / Linux.

**Actions** :
- Étudier l'emplacement des `.jsonl` et la surface d'exécution côté Claude.

**Livrables** :
- Script ou doc d'alternative cross-platform.

**Critère de fin** :
- Un utilisateur non-Windows peut contrôler le contexte sans bricolage manuel.

## Priorités basses

### [ ] BP1 - Ajouter un exemple d'installation propre

**Objectif** :
- Montrer un cas minimal d'installation globale et hybride.

**Actions** :
- Rédiger un exemple court reproductible.

**Livrables** :
- Exemple documenté dans `README.md` ou `integrations/claude-code.md`.

**Critère de fin** :
- L'installation type peut être suivie sans interprétation implicite.

## Ordre recommandé d'exécution

1. Stabiliser la doc Claude et ses règles d'usage.
2. Porter ou remplacer l'outil de monitoring hors Windows.
3. Ajouter un exemple d'installation minimale validé.

## Definition of done pour le prochain cap

Le projet franchit un cap solide quand :
- le protocole et l'intégration Claude décrivent les mêmes règles ;
- les outils annexes et leur auth sont cadrés sans fuite de secrets.

## Prochaine action recommandée

Tester l'installation sur une session Claude neuve et consigner le résultat
dans la doc ou un futur journal de validation.
