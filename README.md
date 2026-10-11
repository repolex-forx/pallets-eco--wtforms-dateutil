# Repolex Knowledge Graph of pallets-eco/wtforms-dateutil

RDF knowledge graph data for [pallets-eco/wtforms-dateutil](https://github.com/pallets-eco/wtforms-dateutil), parsed by [repolex](https://repolex.ai).

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
rlex download pallets-eco/wtforms-dateutil
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fbd183d4fc51f520b0b7a16900060beea9c9b57e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── fbd183d4fc51f520b0b7a16900060beea9c9b57e
│           └── chunk-001.nq.gz
├── blob
│   ├── 03fb64641a72f727f36810f2dc95d28af13ca934.nq.gz
│   ├── 19b243360c85e75dca09559d4d465ddf2de12a13.nq.gz
│   ├── 585310614bcee55273fc891e467c5783b1123a92.nq.gz
│   ├── 66574c235510466448def7ac301ef6a3d1386573.nq.gz
│   ├── 77a44ba684eade19892ec8c147826c40c4681403.nq.gz
│   ├── 80811a2849111b865d42f58d71d91efe1e74d7c5.nq.gz
│   ├── 9dc69eb1653ab477eca8bc51de9106057e89757d.nq.gz
│   ├── a66b70f80a4ed31ee23e108adf73d8ad60e34ae8.nq.gz
│   ├── b6e47617de110dea7ca47e087ff1347cc2646eda.nq.gz
│   ├── c82334553632d12caf96bd3d3d332d9683d2635c.nq.gz
│   ├── c8d28a0f34803d1ddfe6beb2e3ade4a03396a855.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── fbd183d4fc51f520b0b7a16900060beea9c9b57e.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 18 files
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

[pallets-eco/wtforms-dateutil](https://github.com/pallets-eco/wtforms-dateutil)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
