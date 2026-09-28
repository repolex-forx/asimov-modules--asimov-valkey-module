# Repolex Knowledge Graph of asimov-modules/asimov-valkey-module

RDF knowledge graph data for [asimov-modules/asimov-valkey-module](https://github.com/asimov-modules/asimov-valkey-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-valkey-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 381597e02648ab4fb97069d3c33968f7e1c21574
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 381597e02648ab4fb97069d3c33968f7e1c21574.nq.gz
│   └── repolex
│       └── 381597e02648ab4fb97069d3c33968f7e1c21574
│           └── chunk-001.nq.gz
├── blob
│   ├── 00a103096f508464c1106ff66d924974810a05ff.nq.gz
│   ├── 0a5a5302352351d284faeae5cfa00e64de71251d.nq.gz
│   ├── 0faf320ab61483f47f7040f2f4132d61b2b0e756.nq.gz
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 2536bb1fa05b95f771f7bfd03f9bd24e8e011a9d.nq.gz
│   ├── 2b0c788e2596d934456a7ce78cc4e7f3fe40e217.nq.gz
│   ├── 32e25f2c75797b7bed510402469541a1344915ab.nq.gz
│   ├── 380d4e82acf58bfb38e9f0bffcdea03ee87bbcb8.nq.gz
│   ├── 50ecb092f6849d15ebc5c6e6d583368fe99e2a3e.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 6e8bf73aa550d4c57f6f35830f1bcdc7a4a62f38.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a4583350d8fac2bd0bd9f5808fd21c2bd1317b93.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── e0e95a50e52c14fece53ce85e58fc91520a03cd0.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   └── f6e365db313ac91c1ae827f0472bebdd6867459b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 381597e02648ab4fb97069d3c33968f7e1c21574.nq.gz
├── filetree
│   └── 381597e02648ab4fb97069d3c33968f7e1c21574.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 29 files
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

[asimov-modules/asimov-valkey-module](https://github.com/asimov-modules/asimov-valkey-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
