# Repolex Knowledge Graph of pytest-dev/pytest-sqlalchemy

RDF knowledge graph data for [pytest-dev/pytest-sqlalchemy](https://github.com/pytest-dev/pytest-sqlalchemy), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download pytest-dev/pytest-sqlalchemy
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 61db51b09446d4fe3f69cae3147ab7a559c72b94
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 61db51b09446d4fe3f69cae3147ab7a559c72b94
│           └── chunk-001.nq.gz
├── blob
│   ├── 03792bd1911998b18274801cf660238e80abe68a.nq.gz
│   ├── 14ff18fa78974091a00382362c951c7912383bd0.nq.gz
│   ├── 18b95cd04c6a3f0b21311ad8954ea5e378043e27.nq.gz
│   ├── 19a63291a212878944c6f7e43104b6e6088cfde0.nq.gz
│   ├── 1b8c30d5b857bd4fd6adcf1c5565cad6861c242c.nq.gz
│   ├── 1f6d02e30cee63378dfcb8486e8f1cffec5c7e8f.nq.gz
│   ├── 24ee5b1be9961e38a503c8e764b7385dbb6ba124.nq.gz
│   ├── 3fb41af694613a9acb26c74dc4f064839dfe8d5a.nq.gz
│   ├── 4c15dbb812ec844b6a2fac69c10dd6fa7f4ac316.nq.gz
│   ├── 51d7d0a9ce748db36e1addd1104285ead3a3dc89.nq.gz
│   ├── 5ace6d5242ff14734766855ed866be29dcebe6f1.nq.gz
│   ├── 7affe5cc18578431078ea3d444d32bac359871a1.nq.gz
│   ├── 830deabc3e84a2ac6469964242e745983b1250bf.nq.gz
│   ├── 8f59112860519f44f200b853b0f51c54e9986036.nq.gz
│   ├── 942e29bdbb0d73a068c6c07dc43726950367ee35.nq.gz
│   ├── 9575fb97ba9355984e73395d2aee3dad4f0c087e.nq.gz
│   ├── 9f0a7f00e7f0ff1f5fa8b20b55c44c5f23971046.nq.gz
│   ├── b20aca4c94e559dac16bf2e46874d78c5b40dd67.nq.gz
│   ├── b396392e0f6c4c68793e2de0b8a692ae24cbb580.nq.gz
│   ├── b957a32a1ba1704d6b036413ddc677b72c341e5b.nq.gz
│   ├── bc5a0f2f13b45966130545365f1d455dafd8fc94.nq.gz
│   ├── d30c94ce1de32250ef9dad16e732585517893d75.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 61db51b09446d4fe3f69cae3147ab7a559c72b94.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[pytest-dev/pytest-sqlalchemy](https://github.com/pytest-dev/pytest-sqlalchemy)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
