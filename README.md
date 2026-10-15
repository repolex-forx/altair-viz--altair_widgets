# Repolex Knowledge Graph of altair-viz/altair_widgets

RDF knowledge graph data for [altair-viz/altair_widgets](https://github.com/altair-viz/altair_widgets), parsed by [repolex](https://repolex.ai).

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
rlex download altair-viz/altair_widgets
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 20f66597532626a17456f58a3bc3e3a9d4d24c82
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 20f66597532626a17456f58a3bc3e3a9d4d24c82
│           └── chunk-001.nq.gz
├── blob
│   ├── 1abc546f9bc66050fcc6974abef2ef48ada2c3ab.nq.gz
│   ├── 1b22df8c81d5326572d8fbf15fa185d28befa932.nq.gz
│   ├── 1ffaaaf2b4be6044db40778bac1732cbe5889c43.nq.gz
│   ├── 2ff5ee78d44dba24a03598d5d5b906024b1c7427.nq.gz
│   ├── 4747c2ba36bae3c223e340096211c3549b1f5d44.nq.gz
│   ├── 5f671f5a87c7832652f1abb2dbeb61063d472e65.nq.gz
│   ├── 619271f3f4dadf906cf5a9c563f684f91b5af79c.nq.gz
│   ├── 84d7fd2fa862f71850b024be0475001f5463a10a.nq.gz
│   ├── 949e3c1fb819e65cb363bd374c122fa6efec2d97.nq.gz
│   ├── 951b7d8481cd4d7ada28c7f690d8b85f0a19a7e0.nq.gz
│   ├── 99d38f614bc8ac93c8afafd30fc68bf760e0160e.nq.gz
│   ├── b581463bc29a94e0db33148d8e6702ecb5409104.nq.gz
│   ├── c4e00122e391fd61c6c30fa63f2289517847f8cf.nq.gz
│   ├── cd9ec71b9b37721057fec865c70baef4ee74f001.nq.gz
│   ├── e00f71067a1c7a5d141a5721661e737bee6ca8ba.nq.gz
│   └── f6e17542bb9ad25e2552383159d3c95bd2ee6f37.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 20f66597532626a17456f58a3bc3e3a9d4d24c82.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 24 files
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

[altair-viz/altair_widgets](https://github.com/altair-viz/altair_widgets)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
