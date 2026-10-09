# Repolex Knowledge Graph of NousResearch/storywriter-frontend

RDF knowledge graph data for [NousResearch/storywriter-frontend](https://github.com/NousResearch/storywriter-frontend), parsed by [repolex](https://repolex.ai).

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
rlex download NousResearch/storywriter-frontend
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 81ab1a36ebcfc6babb92f979b21ccb497d3e7d0d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 81ab1a36ebcfc6babb92f979b21ccb497d3e7d0d
│           └── chunk-001.nq.gz
├── blob
│   ├── 07f122e66c05f28ad06d4524b4e0177f0fe08051.nq.gz
│   ├── 0a49c67b8c1e508dd5628f7d3497a3798ffbb684.nq.gz
│   ├── 0b08de3a2b5b7c91d8ea9497808a7791c0e4a1d2.nq.gz
│   ├── 0b872d82d9c39f70bff219b3b4b60145430f8984.nq.gz
│   ├── 1c2fda565b94d0f2b94cb65ba7cca866e7a25478.nq.gz
│   ├── 1ea132c752bea811919a81bfe50e8b524d5ff523.nq.gz
│   ├── 25b31d5723dacc4ed2f869c53cd45a3f65404d59.nq.gz
│   ├── 2a21969c5a712160e5d3e0cdae17260184a7e975.nq.gz
│   ├── 3099fd84cefc54228922c51ec8317a309832d391.nq.gz
│   ├── 3f0e5385c2346c47e381cc20ee61e8015c203126.nq.gz
│   ├── 3fe3f360e469151be63e1c659e0c4e7c60f06915.nq.gz
│   ├── 5d1f47411075ae72ffd4b90d04a6ad0bb4514b37.nq.gz
│   ├── 5ebd936998560e79a2c135fe516dac85b67700e7.nq.gz
│   ├── 5ef6a520780202a1d6addd833d800ccb1ecac0bb.nq.gz
│   ├── 61332530fc89c0d91ffc7eb1be3277b7e18bf622.nq.gz
│   ├── 6b255e9f137c621bd719c4dc674e87f7ec232c98.nq.gz
│   ├── 718d6fea4835ec2d246af9800eddb7ffb276240c.nq.gz
│   ├── 74d6d8fbc64916977514c14fc223b3578c2684c8.nq.gz
│   ├── 9661ac713428efbad557d3ba3a62216b5bb7d226.nq.gz
│   ├── 9e98a23c2b276496059ccc78a1a3792b0085904c.nq.gz
│   ├── 9ec118e3154beba18f437b45908e14c3c09f1d17.nq.gz
│   ├── 9ef1ec3fdc86d76ceb730d0c2fbef0ec798386c1.nq.gz
│   ├── a2f168d2d865753808f70b26f362f85f33935cf8.nq.gz
│   ├── a72bd82c931a3da8cdfd320c43ea2c19a2c77d2b.nq.gz
│   ├── ac9f5022a7f6b7e662276f9c59903478f13bb249.nq.gz
│   ├── c38ed2b28bc17d831740d0414a2c96558f590b6b.nq.gz
│   ├── d52d1701ece28d2c2f62cc040fae0ece1d45a66b.nq.gz
│   ├── de3406ea9be851364b388e9fe0d54113a7a85af6.nq.gz
│   ├── dfcf32d6ccf4d779c1fbd840d0830dbc7dd47207.nq.gz
│   ├── e0695befba6f49b9deeff16f861c6a2befc11f5e.nq.gz
│   ├── f035ade9a9222145d4a5cde0d28a707142c6ecdb.nq.gz
│   └── f32f822d47a83e15e8f0bea05fa52f4cc46e0412.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 81ab1a36ebcfc6babb92f979b21ccb497d3e7d0d.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 38 files
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

[NousResearch/storywriter-frontend](https://github.com/NousResearch/storywriter-frontend)

---
*Parsed on 2026-10-09 by [repolex](https://repolex.ai)*
