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
/plugin install outreach@drivenlabs-ai          # accès privé requis
/plugin install phantombuster@drivenlabs-ai     # accès privé requis
```

## Plugins

| Plugin | Statut | Repo | Description |
|---|---|---|---|
| `driven` | Public | [drivenlabs-ai/driven](https://github.com/drivenlabs-ai/driven) | Compagnon de workspaces collaboratifs Claude. Capture mémoire, cross-author, propagation. |
| `batch-cep` | À venir | drivenlabs-ai/batch-cep | Orchestration Batch.com (CEP + MEP) en langage naturel. |
| `outreach` | À venir (privé) | drivenlabs-ai/outreach | Outbound productisé : sourcing Lemlist → scoring → CRM Attio. |
| `phantombuster` | À venir (privé) | drivenlabs-ai/phantombuster | CLI bas niveau pour l'API Phantombuster v2. |

## Architecture

Hub-and-spoke : ce repo héberge la marketplace ; chaque plugin vit dans son propre repo. Cadence et visibilité indépendantes par plugin.

## Cowork upload (fallback)

Pour les orgs Claude Cowork qui veulent uploader un plugin via ZIP plutôt que d'ajouter la marketplace : chaque repo plugin contient un `scripts/gen-cowork-zip.sh` qui génère le ZIP au format attendu.
