# Alpana Spec Slice

This directory contains a repo-ready Alpana specification slice built around prompt surfaces,
governance layers, bounded bubble packs, runtime profiles, and executable contracts.

## Structure

- `kernel/` — canonical meaning and ontology attachment rules
- `governance/` — decision classes, review defaults, promotion paths
- `domains/` — domain charters
- `agents/roles/` — role cards for bounded agent types
- `runtime/profiles/` — execution-mode profiles kept separate from doctrine
- `contracts/` — tool, retrieval, and output contracts
- `bubbles/` — local bounded realities assembled from the above
- `runs/` — ephemeral run manifests
- `schemas/` — JSON Schemas for the YAML shapes

## Principles

1. Keep the core prompt small.
2. Put behavior in profiles, contracts, tool surfaces, and checks.
3. Separate kernel meaning from governance movement.
4. Treat bubble packs as the minimum complete capability set for local reality.
5. Never promote local runtime truth into canon without governance.
6. Keep provider-specific behavior at the adapter edge.

## Validation

A lightweight validator is provided at:

```bash
node scripts/validate-alpana-spec.mjs
```

The validator checks:
- YAML parseability
- required `schema_id` and `schema_version`
- known schema IDs
- existence of local `profile_ref` and `retrieval.profile_ref` paths when used

## Current included examples

- `bubbles/delivery/repo-delivery-default/bubble.pack.yaml`
- `bubbles/delivery/docs-rewrite-default/bubble.pack.yaml`
- `runs/examples/repo-delivery-readme-rewrite.run.yaml`
- `runs/examples/docs-rewrite-entrypoints.run.yaml`
