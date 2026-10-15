# Repolex Knowledge Graph of scrapy-plugins/scrapy-streamitem

RDF knowledge graph data for [scrapy-plugins/scrapy-streamitem](https://github.com/scrapy-plugins/scrapy-streamitem), parsed by [repolex](https://repolex.ai).

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
rlex download scrapy-plugins/scrapy-streamitem
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 78ecb9db7109d7b85cbe292413eaca8b78003476
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 78ecb9db7109d7b85cbe292413eaca8b78003476
│           └── chunk-001.nq.gz
├── blob
│   ├── 083e673b4c3270f50aef3b65723ae4bbaf021efa.nq.gz
│   ├── 17764ffa48b9781ed9370bc16a0e29772aba5206.nq.gz
│   ├── 3d027f4cbc594c068572a8d2e96239c3b6111625.nq.gz
│   ├── 3fa1593f66e6102ab001336e6456760b956d8eb2.nq.gz
│   ├── 51978ed022e4aa5a80d4a0d1979b4d05738098a5.nq.gz
│   ├── 541f859dc9ea238cf66986b5b7ccd3189c4c74dc.nq.gz
│   ├── 729966c4919f1b65a0d4c2193efaea7ad314388e.nq.gz
│   ├── 9839379e3584f3e59ef06488ab3d4c924e4992e8.nq.gz
│   ├── b9cfc55f4e57cb163300610888fbd8c0c992e950.nq.gz
│   ├── cc10d4c8c80a8d6f7b0b4009858ab411b736c712.nq.gz
│   ├── db4561eaa1d4f3ed01af114a315a0053776ffed0.nq.gz
│   └── e7b4d6076a51e1a921341d8059b34cfe85d7a2e4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 78ecb9db7109d7b85cbe292413eaca8b78003476.nq.gz
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

[scrapy-plugins/scrapy-streamitem](https://github.com/scrapy-plugins/scrapy-streamitem)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
