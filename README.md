# Repolex Knowledge Graph of pyeve/eve-requests

RDF knowledge graph data for [pyeve/eve-requests](https://github.com/pyeve/eve-requests), parsed by [repolex](https://repolex.ai).

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
rlex download pyeve/eve-requests
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f04c8aa62c7f50cdde9da6ae26eeb5bae360cb3f
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f04c8aa62c7f50cdde9da6ae26eeb5bae360cb3f
│           └── chunk-001.nq.gz
├── blob
│   ├── 1e6fd5aa3d20722d2a76578c3f54b6c8ce330209.nq.gz
│   ├── 2960128a723cc16f8d2c253d8a9707fb3423bcd8.nq.gz
│   ├── 2c2496473397a81c02fd8bfecfad7a859b8b5aa0.nq.gz
│   ├── 33a2a9850711c1fd379ed19c78150309ba507a02.nq.gz
│   ├── 42ec41857be8e4ad7f57e49c2ff7acb553d3f972.nq.gz
│   ├── 4ee8f58f259b9efa166d689b96e1f209c7f81b37.nq.gz
│   ├── 6be2ecb56fed0b7c78f34bc2d14d469514330049.nq.gz
│   ├── 77b0273f097256156b87fd9063f598bf721e3941.nq.gz
│   ├── 8a4b4e17b4d43caecce76f49c24aa0e4db1ab59a.nq.gz
│   ├── 918deba65f803a5743ffa6a2daa016d55c6123f6.nq.gz
│   ├── a73d98f8d1c74d32c8b116af48cb69d26480237c.nq.gz
│   ├── a76592b866377fa098047ab121af9aa521a59d7d.nq.gz
│   ├── b3a3ac866153bad2936f10581385b4bb0294937d.nq.gz
│   ├── bb76b293ce11bf147ac3d20f6279d4e92410efca.nq.gz
│   ├── cb814431ce1d048f729ce7fe8d9d1b8afa793cc0.nq.gz
│   ├── d777389042d8cc089147e636a117a27f08a9fa55.nq.gz
│   ├── dffdd5d99fe681fafe8bed95b57204d346cdadbf.nq.gz
│   ├── e72f8a32afd8d278f9ee1c12813e3ee658697d03.nq.gz
│   ├── f2293605cf1b01dca72aad0a15c45b72ed5429a2.nq.gz
│   └── f4a551ec5ef464684dea2094b8c7e82d90ae6092.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f04c8aa62c7f50cdde9da6ae26eeb5bae360cb3f.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 26 files
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

[pyeve/eve-requests](https://github.com/pyeve/eve-requests)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
