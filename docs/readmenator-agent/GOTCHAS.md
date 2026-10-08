# Gotchas

## God Nodes (high connectivity)

These files have the most connections. Changes here have high blast radius.

- `utils.py` (score: 8.90, imported by 1 files)
- `app.py` (score: 2.30)
- `install.sh` (score: 0.00)

## Blast Radius (change impact)

Editing these files can break the listed number of dependents. Run their tests after any change.

- `utils.py` -- 1 direct, 1 total dependents

## Hotspots (complexity + centrality)

- `utils.py` -- complexity: 1.0, centrality: 1.0, combined: 1.0
- `app.py` -- complexity: 0.0, centrality: 0.1, combined: 0.1
- `install.sh` -- complexity: 0.0, centrality: 0.0, combined: 0.0

## Dataflow Issues (INFERRED, review each lead)

- `app.py:29` `image_to_bash` [UNCHECKED_ALLOC] `img`: Result of allocator stored in `img` is never checked against NULL.
