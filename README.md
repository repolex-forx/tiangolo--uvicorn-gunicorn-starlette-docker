# Repolex Knowledge Graph of tiangolo/uvicorn-gunicorn-starlette-docker

RDF knowledge graph data for [tiangolo/uvicorn-gunicorn-starlette-docker](https://github.com/tiangolo/uvicorn-gunicorn-starlette-docker), parsed by [repolex](https://repolex.ai).

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
rlex download tiangolo/uvicorn-gunicorn-starlette-docker
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3c5484c58218774ad47f1ad7aae681d5b2156056
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 3c5484c58218774ad47f1ad7aae681d5b2156056
│           └── chunk-001.nq.gz
├── blob
│   ├── 00185a99afe5f1d5e9554af4a4f802e9d25dcc77.nq.gz
│   ├── 236a646ecff2caf37d6743a6dbb5324583ba0dc8.nq.gz
│   ├── 2811ded3331f0482bdee78628f167c7668741729.nq.gz
│   ├── 2b75d7cfd7c050117d260ffa70e207ea1821a208.nq.gz
│   ├── 40ce173f1a1d2ee11543d4c436a4a28f81d0031d.nq.gz
│   ├── 53dd60afa903ec0b511cc9ec7cc14c19308fad84.nq.gz
│   ├── 55eec6eb458d17b0a36c90625488d8fafbda90d5.nq.gz
│   ├── 5fc5f542be61a8ec27f104a4685be273a6350ebd.nq.gz
│   ├── 6828efae6e06bae6838575d437f44157776c6ed9.nq.gz
│   ├── 7640fd5f71d83ee12db0977b8db4cfc1d55bae6d.nq.gz
│   ├── 90a7812c30567e6e7737e937875d9aaf945376f1.nq.gz
│   ├── 99784d68337bae260a66a51e87fb9adfc8850d9a.nq.gz
│   ├── 998071656835cf5dba2084ebea25d827c6610266.nq.gz
│   ├── acde30b8f263d82585f584e01cb4be745eaf4745.nq.gz
│   ├── b1b5f68cfa87a6ae6e62f8a5bd84e06086a14b59.nq.gz
│   ├── c94d562277a586c63f96f5e08e85cef15d9b1a4f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ec967e98a4831519d3747165d04d2d96cd7ec51b.nq.gz
│   └── feec529f1e6a2c68172ce4c39dca6419764cdbfa.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3c5484c58218774ad47f1ad7aae681d5b2156056.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 27 files
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

[tiangolo/uvicorn-gunicorn-starlette-docker](https://github.com/tiangolo/uvicorn-gunicorn-starlette-docker)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
