# Drivenlabs — Claude Code plugins

Marketplace centrale des plugins Drivenlabs pour Claude Code.

## Install

```
/plugin marketplace add drivenlabs-ai/plugins
```

Puis installe les plugins que tu veux :

```
/plugin install driven@drivenlabs-ai
/plugin install batch-cep@drivenlabs-ai
```

## Plugins

| Plugin | Repo | Description |
|---|---|---|
| `driven` | [drivenlabs-ai/driven](https://github.com/drivenlabs-ai/driven) | Compagnon de workspaces collaboratifs Claude. Capture mémoire, cross-author, propagation. |
| `batch-cep` | [drivenlabs-ai/batch-cep](https://github.com/drivenlabs-ai/batch-cep) | Orchestration Batch.com (CEP + MEP) en langage naturel. 60 commandes wrappées. |

> Cette marketplace ne référence que les plugins publics. Les plugins internes Drivenlabs (`outreach`, `phantombuster`) vivent dans des repos privés et sont distribués séparément aux collaborateurs autorisés.

## Architecture

Hub-and-spoke : ce repo héberge la marketplace ; chaque plugin vit dans son propre repo. Cadence et visibilité indépendantes par plugin. Pas de version pinning dans la marketplace — les users récupèrent toujours la dernière version (always-latest by design).

## Cowork upload (fallback)

Pour les orgs Claude Cowork qui veulent uploader un plugin via ZIP plutôt que d'ajouter la marketplace : chaque repo plugin contient `scripts/gen-cowork-zip.sh` qui génère un ZIP au format attendu.
