# Repolex Knowledge Graph of datasette/datasette-llm-limits

RDF knowledge graph data for [datasette/datasette-llm-limits](https://github.com/datasette/datasette-llm-limits), parsed by [repolex](https://repolex.ai).

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
rlex download datasette/datasette-llm-limits
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c083b1d9fa5a714f2ac7942591fc917a3b82f2f1
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c083b1d9fa5a714f2ac7942591fc917a3b82f2f1
│           └── chunk-001.nq.gz
├── blob
│   ├── 0aa785b93f85f3b1ef8ec5fe31d50a3cd8e706dc.nq.gz
│   ├── 12ab34ebec94e84e10bde3f5cb5d75b314d996bd.nq.gz
│   ├── 22b1e9a3398ce5c49b6540814f443bf5dcbed908.nq.gz
│   ├── 23f753e0e0f7b5481ab801ffc2ab79f0670c0773.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 30b60bf5f7d527de0e3833a69f2c83a4f5e523f3.nq.gz
│   ├── 40db6cf66bbae03bc587772e0346cccdf7f2273e.nq.gz
│   ├── 45bd26c3e31dec2e331d3d3c3947b6c61f50d622.nq.gz
│   ├── 4c6fd22fcac137fdabf0a001655f105e7f3d3618.nq.gz
│   ├── 66435a4bc6224b355fe2ff8a97c4cdad7408a0a4.nq.gz
│   ├── 78c93c459ddc7a7d253f23fb501e18e5ee178a27.nq.gz
│   ├── 7ae3fe97e80d8db843bea5820cd4b79e6a397666.nq.gz
│   ├── 7ea95fc567d1fdee6ec59f3b05bde501ec4ed1d8.nq.gz
│   ├── 8d566402c449453a5f63c9d52cfd70ef891cd550.nq.gz
│   ├── 9b8cfe953edf04e8261f0939e12e7910adb079c1.nq.gz
│   ├── b341e30daed5559fcc8ad73a7b8e6540b4e7a052.nq.gz
│   ├── b7932437e182a8728962158dc90f035935c1d160.nq.gz
│   ├── c5746feefb85a4b4135a8884293e59a86de7ec70.nq.gz
│   ├── c7a90eb4f1035fa0a8a1ca007b5fbdef24ba07c1.nq.gz
│   ├── e95006545e4f64c5a10dddd812d1a49358adc527.nq.gz
│   ├── eb22e74eaaaf0edc4aa2c0f8900a55750d1660f9.nq.gz
│   └── f367054d038c0f4200ab9be72917e5704a037c7d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c083b1d9fa5a714f2ac7942591fc917a3b82f2f1.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[datasette/datasette-llm-limits](https://github.com/datasette/datasette-llm-limits)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
