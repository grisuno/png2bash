# Concepts

Second-brain semantic layer: nouns map atomically to file sets (EXTRACTED); verbs aggregate structural edges (INFERRED).

| Concept | Files | Mentions | Top Files |
|---------|-------|----------|-----------|
| `list` | 2 | 36 | `app.py`, `utils.py` |
| `files` | 2 | 13 | `app.py`, `utils.py` |
| `framework` | 2 | 9 | `app.py`, `utils.py` |
| `archivo` | 2 | 8 | `app.py`, `utils.py` |
| `com` | 2 | 8 | `app.py`, `utils.py` |
| `lazy` | 2 | 8 | `app.py`, `utils.py` |
| `own` | 2 | 8 | `app.py`, `utils.py` |
| `banner` | 2 | 6 | `app.py`, `utils.py` |
| `red` | 2 | 4 | `app.py`, `utils.py` |
| `dot` | 2 | 3 | `app.py`, `utils.py` |
| `team` | 2 | 3 | `app.py`, `utils.py` |
| `autor` | 2 | 2 | `app.py`, `utils.py` |
| `bash` | 2 | 2 | `app.py`, `utils.py` |
| `contiene` | 2 | 2 | `app.py`, `utils.py` |
| `correo` | 2 | 2 | `app.py`, `utils.py` |
| `creaci` | 2 | 2 | `app.py`, `utils.py` |
| `definici` | 2 | 2 | `app.py`, `utils.py` |
| `descripci` | 2 | 2 | `app.py`, `utils.py` |
| `electr` | 2 | 2 | `app.py`, `utils.py` |
| `este` | 2 | 2 | `app.py`, `utils.py` |
| `fecha` | 2 | 2 | `app.py`, `utils.py` |
| `gica` | 2 | 2 | `app.py`, `utils.py` |
| `gmail` | 2 | 2 | `app.py`, `utils.py` |
| `gpl` | 2 | 2 | `app.py`, `utils.py` |
| `gris` | 2 | 2 | `app.py`, `utils.py` |
| `grisiscomeback` | 2 | 2 | `app.py`, `utils.py` |
| `iscomeback` | 2 | 2 | `app.py`, `utils.py` |
| `licencia` | 2 | 2 | `app.py`, `utils.py` |
| `nico` | 2 | 2 | `app.py`, `utils.py` |

## Verb Edges

| Source | Verb | Target | Strength |
|--------|------|--------|----------|
| `archivo` | `depends_on` | `autor` | 1.00 |
| `archivo` | `depends_on` | `banner` | 1.00 |
| `archivo` | `depends_on` | `bash` | 1.00 |
| `archivo` | `depends_on` | `com` | 1.00 |
| `archivo` | `depends_on` | `contiene` | 1.00 |
| `archivo` | `depends_on` | `correo` | 1.00 |
| `archivo` | `depends_on` | `creaci` | 1.00 |
| `archivo` | `depends_on` | `definici` | 1.00 |
| `archivo` | `depends_on` | `descripci` | 1.00 |
| `archivo` | `depends_on` | `dot` | 1.00 |
| `archivo` | `depends_on` | `electr` | 1.00 |
| `archivo` | `depends_on` | `este` | 1.00 |
| `archivo` | `depends_on` | `fecha` | 1.00 |
| `archivo` | `depends_on` | `files` | 1.00 |
| `archivo` | `depends_on` | `framework` | 1.00 |
| `archivo` | `depends_on` | `gica` | 1.00 |
| `archivo` | `depends_on` | `gmail` | 1.00 |
| `archivo` | `depends_on` | `gpl` | 1.00 |
| `archivo` | `depends_on` | `gris` | 1.00 |
| `archivo` | `depends_on` | `grisiscomeback` | 1.00 |
| `archivo` | `depends_on` | `iscomeback` | 1.00 |
| `archivo` | `depends_on` | `lazy` | 1.00 |
| `archivo` | `depends_on` | `licencia` | 1.00 |
| `archivo` | `depends_on` | `list` | 1.00 |
| `archivo` | `depends_on` | `nico` | 1.00 |
| `archivo` | `depends_on` | `own` | 1.00 |
| `archivo` | `depends_on` | `red` | 1.00 |
| `archivo` | `depends_on` | `team` | 1.00 |
| `autor` | `depends_on` | `archivo` | 1.00 |
| `autor` | `depends_on` | `banner` | 1.00 |
| `autor` | `depends_on` | `bash` | 1.00 |
| `autor` | `depends_on` | `com` | 1.00 |
| `autor` | `depends_on` | `contiene` | 1.00 |
| `autor` | `depends_on` | `correo` | 1.00 |
| `autor` | `depends_on` | `creaci` | 1.00 |
| `autor` | `depends_on` | `definici` | 1.00 |
| `autor` | `depends_on` | `descripci` | 1.00 |
| `autor` | `depends_on` | `dot` | 1.00 |
| `autor` | `depends_on` | `electr` | 1.00 |
| `autor` | `depends_on` | `este` | 1.00 |
| `autor` | `depends_on` | `fecha` | 1.00 |
| `autor` | `depends_on` | `files` | 1.00 |
| `autor` | `depends_on` | `framework` | 1.00 |
| `autor` | `depends_on` | `gica` | 1.00 |
| `autor` | `depends_on` | `gmail` | 1.00 |
| `autor` | `depends_on` | `gpl` | 1.00 |
| `autor` | `depends_on` | `gris` | 1.00 |
| `autor` | `depends_on` | `grisiscomeback` | 1.00 |
| `autor` | `depends_on` | `iscomeback` | 1.00 |
| `autor` | `depends_on` | `lazy` | 1.00 |

## Dialectic Prompts

- Thesis: `archivo` centralizes 2 files; Antithesis: `autor` pulls 2 files with 2 shared (Jaccard 1.00); Synthesis: should they merge, split by layer, or keep `depends_on` explicit?
- Thesis: `archivo` centralizes 2 files; Antithesis: `banner` pulls 2 files with 2 shared (Jaccard 1.00); Synthesis: should they merge, split by layer, or keep `depends_on` explicit?
- Thesis: `archivo` centralizes 2 files; Antithesis: `bash` pulls 2 files with 2 shared (Jaccard 1.00); Synthesis: should they merge, split by layer, or keep `depends_on` explicit?
- Thesis: `archivo` centralizes 2 files; Antithesis: `com` pulls 2 files with 2 shared (Jaccard 1.00); Synthesis: should they merge, split by layer, or keep `depends_on` explicit?
- Thesis: `archivo` centralizes 2 files; Antithesis: `contiene` pulls 2 files with 2 shared (Jaccard 1.00); Synthesis: should they merge, split by layer, or keep `depends_on` explicit?
- Thesis: `archivo` centralizes 2 files; Antithesis: `correo` pulls 2 files with 2 shared (Jaccard 1.00); Synthesis: should they merge, split by layer, or keep `depends_on` explicit?
- Thesis: `archivo` centralizes 2 files; Antithesis: `creaci` pulls 2 files with 2 shared (Jaccard 1.00); Synthesis: should they merge, split by layer, or keep `depends_on` explicit?
- Thesis: `archivo` centralizes 2 files; Antithesis: `definici` pulls 2 files with 2 shared (Jaccard 1.00); Synthesis: should they merge, split by layer, or keep `depends_on` explicit?
- Thesis: `archivo` centralizes 2 files; Antithesis: `descripci` pulls 2 files with 2 shared (Jaccard 1.00); Synthesis: should they merge, split by layer, or keep `depends_on` explicit?
- Thesis: `archivo` centralizes 2 files; Antithesis: `dot` pulls 2 files with 2 shared (Jaccard 1.00); Synthesis: should they merge, split by layer, or keep `depends_on` explicit?
