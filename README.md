# Repolex Knowledge Graph of jupyterhub/jupyterhub-python-repo-template

RDF knowledge graph data for [jupyterhub/jupyterhub-python-repo-template](https://github.com/jupyterhub/jupyterhub-python-repo-template), parsed by [repolex](https://repolex.ai).

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
rlex download jupyterhub/jupyterhub-python-repo-template
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3bcbc805517686a33b8dfc5bff6e1e15f8afb2b7
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 3bcbc805517686a33b8dfc5bff6e1e15f8afb2b7
│           └── chunk-001.nq.gz
├── blob
│   ├── 026f658e0faa3d03e275117dd7cc47615c5a82a4.nq.gz
│   ├── 0d97af9c92c204499a240b8cebae2ca9da906b6e.nq.gz
│   ├── 10d32e23ce10e9a30a80d12f62b5dedc0469c785.nq.gz
│   ├── 12d406b7a7136a1fceb1a2a71076871a119d5b95.nq.gz
│   ├── 13dd9f14ab870ae044e67a7ce70379c9fd9fa9c0.nq.gz
│   ├── 356dca6642994cef8061b8af057ff8cc0f8fea43.nq.gz
│   ├── 3f4c87ee3faafb533777fc4efa956d3eb36ce82f.nq.gz
│   ├── 66d02a3c3f9b1b59b1b359d7ff8d847cf85f779e.nq.gz
│   ├── 673efdb52e98e6a21083e3a2f5d54992ebc20b25.nq.gz
│   ├── 698ad83bf585ee8b8df0e7eeb52b70bc53555d73.nq.gz
│   ├── 6b94e9df221db99f6d1a44f1389ca78da302a44e.nq.gz
│   ├── 7ec182e1f928274af87e908454f7a94f5d163ec8.nq.gz
│   ├── 7fbd4031eb68e7fe8429d6a22b67c104e4c50b5d.nq.gz
│   ├── 8d34bf0659e125f777c98cf96b58f11b755c5bef.nq.gz
│   ├── 8fa2dbf144831043e26c153964e5a0ee6d5dd304.nq.gz
│   ├── 97a835b58354e7c75c8085deced4bb3100650d91.nq.gz
│   ├── a7889d97cc6b80f72218bad592c69ece6d3ed240.nq.gz
│   ├── abe5933be6bf6e2ce272cb67051368091a8dd879.nq.gz
│   ├── bb16b2c62328f1fb3d87839f7c5ac16e9e89b05a.nq.gz
│   ├── c304cbc7956f0b16864921d35a718fd071998daa.nq.gz
│   ├── c43b5e22e714cccc5a1ab85c5ef0c4343661e30d.nq.gz
│   ├── e1b50ea0c08af19e74c00b3c4d8b3511d54919f8.nq.gz
│   ├── e64bd338e0a3ea1f2970e33a23cb524c0fdc4519.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f6d299f06c9360f34368a123a857216e9edd7da3.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3bcbc805517686a33b8dfc5bff6e1e15f8afb2b7.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 33 files
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

[jupyterhub/jupyterhub-python-repo-template](https://github.com/jupyterhub/jupyterhub-python-repo-template)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
