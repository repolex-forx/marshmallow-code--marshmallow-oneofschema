# Repolex Knowledge Graph of marshmallow-code/marshmallow-oneofschema

RDF knowledge graph data for [marshmallow-code/marshmallow-oneofschema](https://github.com/marshmallow-code/marshmallow-oneofschema), parsed by [repolex](https://repolex.ai).

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
rlex download marshmallow-code/marshmallow-oneofschema
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6b25e361b7efa1992583a22f2e02178b1424d073
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 6b25e361b7efa1992583a22f2e02178b1424d073
│           └── chunk-001.nq.gz
├── blob
│   ├── 12d47065bcae744cff14aa7b5e0b5a4f73bbca18.nq.gz
│   ├── 1488cbed7b41a3fcc7234a5f437294e97276fd6b.nq.gz
│   ├── 29cee121fca37812003814714472cbc0c782ab44.nq.gz
│   ├── 385ba6e739af9076c5a7fff34b6d60d2c80690f2.nq.gz
│   ├── 394d6c260fc3196b66e37bfff9abeb709ed1596a.nq.gz
│   ├── 4243505b31e668ca5290d3f5020708d3d86225e3.nq.gz
│   ├── 62413dd848750d4bd2593b1e71d833c030282981.nq.gz
│   ├── 74db1e74f17cd6c85e4801c4c93a2490a9b2d8bd.nq.gz
│   ├── 92ec2bb600a1e1f3ad8666d355b485b696332790.nq.gz
│   ├── 96d1cfdc462e2e5497bf63ae96ce7a9113042833.nq.gz
│   ├── c1cdc56b8d0af008a8a821b2cc8d287c12c712c8.nq.gz
│   ├── cc8247581a736d34e05d17410001a359b2593aae.nq.gz
│   ├── d0c0544cb6d322582669ce6d64cc8758a747d9e0.nq.gz
│   ├── db456ff33a0b07356702c43817604a7c79df6502.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f40ce91be5fa3ae6afbf5457462f0d87000e4f1b.nq.gz
│   └── fcd7f04dfef03b1ec7377f9707d448f9ff8bbf9a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6b25e361b7efa1992583a22f2e02178b1424d073.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 25 files
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

[marshmallow-code/marshmallow-oneofschema](https://github.com/marshmallow-code/marshmallow-oneofschema)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
