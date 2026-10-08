# Concepts

Nouns map atomically to file sets (EXTRACTED); verbs aggregate structural edges (INFERRED).

- `list` | files=2 | mentions=36 | `app.py`, `utils.py`
- `files` | files=2 | mentions=13 | `app.py`, `utils.py`
- `framework` | files=2 | mentions=9 | `app.py`, `utils.py`
- `archivo` | files=2 | mentions=8 | `app.py`, `utils.py`
- `com` | files=2 | mentions=8 | `app.py`, `utils.py`
- `lazy` | files=2 | mentions=8 | `app.py`, `utils.py`
- `own` | files=2 | mentions=8 | `app.py`, `utils.py`
- `banner` | files=2 | mentions=6 | `app.py`, `utils.py`
- `red` | files=2 | mentions=4 | `app.py`, `utils.py`
- `dot` | files=2 | mentions=3 | `app.py`, `utils.py`
- `team` | files=2 | mentions=3 | `app.py`, `utils.py`
- `autor` | files=2 | mentions=2 | `app.py`, `utils.py`
- `bash` | files=2 | mentions=2 | `app.py`, `utils.py`
- `contiene` | files=2 | mentions=2 | `app.py`, `utils.py`
- `correo` | files=2 | mentions=2 | `app.py`, `utils.py`
- `creaci` | files=2 | mentions=2 | `app.py`, `utils.py`
- `definici` | files=2 | mentions=2 | `app.py`, `utils.py`
- `descripci` | files=2 | mentions=2 | `app.py`, `utils.py`
- `electr` | files=2 | mentions=2 | `app.py`, `utils.py`
- `este` | files=2 | mentions=2 | `app.py`, `utils.py`
- `fecha` | files=2 | mentions=2 | `app.py`, `utils.py`
- `gica` | files=2 | mentions=2 | `app.py`, `utils.py`
- `gmail` | files=2 | mentions=2 | `app.py`, `utils.py`
- `gpl` | files=2 | mentions=2 | `app.py`, `utils.py`
- `gris` | files=2 | mentions=2 | `app.py`, `utils.py`
- `grisiscomeback` | files=2 | mentions=2 | `app.py`, `utils.py`
- `iscomeback` | files=2 | mentions=2 | `app.py`, `utils.py`
- `licencia` | files=2 | mentions=2 | `app.py`, `utils.py`
- `nico` | files=2 | mentions=2 | `app.py`, `utils.py`

## Verb Edges

- `archivo` --depends_on--> `autor` (strength 1.00)
- `archivo` --depends_on--> `banner` (strength 1.00)
- `archivo` --depends_on--> `bash` (strength 1.00)
- `archivo` --depends_on--> `com` (strength 1.00)
- `archivo` --depends_on--> `contiene` (strength 1.00)
- `archivo` --depends_on--> `correo` (strength 1.00)
- `archivo` --depends_on--> `creaci` (strength 1.00)
- `archivo` --depends_on--> `definici` (strength 1.00)
- `archivo` --depends_on--> `descripci` (strength 1.00)
- `archivo` --depends_on--> `dot` (strength 1.00)
- `archivo` --depends_on--> `electr` (strength 1.00)
- `archivo` --depends_on--> `este` (strength 1.00)
- `archivo` --depends_on--> `fecha` (strength 1.00)
- `archivo` --depends_on--> `files` (strength 1.00)
- `archivo` --depends_on--> `framework` (strength 1.00)
- `archivo` --depends_on--> `gica` (strength 1.00)
- `archivo` --depends_on--> `gmail` (strength 1.00)
- `archivo` --depends_on--> `gpl` (strength 1.00)
- `archivo` --depends_on--> `gris` (strength 1.00)
- `archivo` --depends_on--> `grisiscomeback` (strength 1.00)
- `archivo` --depends_on--> `iscomeback` (strength 1.00)
- `archivo` --depends_on--> `lazy` (strength 1.00)
- `archivo` --depends_on--> `licencia` (strength 1.00)
- `archivo` --depends_on--> `list` (strength 1.00)
- `archivo` --depends_on--> `nico` (strength 1.00)
- `archivo` --depends_on--> `own` (strength 1.00)
- `archivo` --depends_on--> `red` (strength 1.00)
- `archivo` --depends_on--> `team` (strength 1.00)
- `autor` --depends_on--> `archivo` (strength 1.00)
- `autor` --depends_on--> `banner` (strength 1.00)
- `autor` --depends_on--> `bash` (strength 1.00)
- `autor` --depends_on--> `com` (strength 1.00)
- `autor` --depends_on--> `contiene` (strength 1.00)
- `autor` --depends_on--> `correo` (strength 1.00)
- `autor` --depends_on--> `creaci` (strength 1.00)
- `autor` --depends_on--> `definici` (strength 1.00)
- `autor` --depends_on--> `descripci` (strength 1.00)
- `autor` --depends_on--> `dot` (strength 1.00)
- `autor` --depends_on--> `electr` (strength 1.00)
- `autor` --depends_on--> `este` (strength 1.00)
- `autor` --depends_on--> `fecha` (strength 1.00)
- `autor` --depends_on--> `files` (strength 1.00)
- `autor` --depends_on--> `framework` (strength 1.00)
- `autor` --depends_on--> `gica` (strength 1.00)
- `autor` --depends_on--> `gmail` (strength 1.00)
- `autor` --depends_on--> `gpl` (strength 1.00)
- `autor` --depends_on--> `gris` (strength 1.00)
- `autor` --depends_on--> `grisiscomeback` (strength 1.00)
- `autor` --depends_on--> `iscomeback` (strength 1.00)
- `autor` --depends_on--> `lazy` (strength 1.00)

## Dialectic

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
