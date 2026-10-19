# Repolex Knowledge Graph of florimondmanca/msgpack-asgi

RDF knowledge graph data for [florimondmanca/msgpack-asgi](https://github.com/florimondmanca/msgpack-asgi), parsed by [repolex](https://repolex.ai).

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
rlex download florimondmanca/msgpack-asgi
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2875e1f0a0d96b7c2281c8903f1184589016e706
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2875e1f0a0d96b7c2281c8903f1184589016e706
│           └── chunk-001.nq.gz
├── blob
│   ├── 05e6f770362bdd888365c9d99285b70041672930.nq.gz
│   ├── 09bffe5b765dcdb86be1b5d9be0f2b8011b17650.nq.gz
│   ├── 0cd42f0837f98b7f5a1138e213c5226d9d99ab3b.nq.gz
│   ├── 17d2f08e89927816c90b689403e2de74d56a9c38.nq.gz
│   ├── 22a5feb42e77ed3abaf33b060aa93ba02af28596.nq.gz
│   ├── 274cdf93d76b0fda75f1b760e061ffcc0470d954.nq.gz
│   ├── 2b831ff3ddb984138afd96a53e859ed10ba0e7df.nq.gz
│   ├── 2d5f90aad7e7cee6749a2acbfd44e772e44c9b17.nq.gz
│   ├── 38f38b101b9de4bb3017493dfd0b15752e91f1f9.nq.gz
│   ├── 405f33e98e0e5cfd13d7acd8a88dd467687779a5.nq.gz
│   ├── 41ed33bf71f7e1ec48d44cb40ed3919a9fd70947.nq.gz
│   ├── 51d2f7eda54d5abaf0fee4a1ea139f1481b1020b.nq.gz
│   ├── 6831c49139c14925ca3a82a4bf2143c98ea771e0.nq.gz
│   ├── a0fb3d75c5f70ab12fab876eeefb4622277aaa45.nq.gz
│   ├── b9ba97a219dd3ca89e49548a00a8f228af4d7937.nq.gz
│   ├── ba0b39ddcd10fa8812e528e4137dcb7e1b1a6e5d.nq.gz
│   ├── bd33b5cf1a2a124793f9125b3ff458480ee6ae56.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2875e1f0a0d96b7c2281c8903f1184589016e706.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 26 files
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

[florimondmanca/msgpack-asgi](https://github.com/florimondmanca/msgpack-asgi)

---
*Parsed on 2026-10-19 by [repolex](https://repolex.ai)*
