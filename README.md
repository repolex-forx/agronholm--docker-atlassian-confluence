# Repolex Knowledge Graph of agronholm/docker-atlassian-confluence

RDF knowledge graph data for [agronholm/docker-atlassian-confluence](https://github.com/agronholm/docker-atlassian-confluence), parsed by [repolex](https://repolex.ai).

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
rlex download agronholm/docker-atlassian-confluence
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 573b616b9a2de79b21545ae7f57845456f82f4e0
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 573b616b9a2de79b21545ae7f57845456f82f4e0
│           └── chunk-001.nq.gz
├── blob
│   ├── 027ee4628d67a025a37f16fc3172f8bb809d1152.nq.gz
│   ├── 0ddff6d7e44f3ebcfd81c83c8d78f6be2df286e2.nq.gz
│   ├── 0debf2e9613a53797b1a01057282efe0e4259ff8.nq.gz
│   ├── 177f4fb99176a38812d5f36d999434668a7ef0e2.nq.gz
│   ├── 2206a0c700f85bca19a3b3f3bd4d7e6f6e125110.nq.gz
│   ├── 23582a80f7b0c769aae4e63ac478029d0d03826c.nq.gz
│   ├── 25adf625313c220cbdf538f6c3af67450f75a67d.nq.gz
│   ├── 28de2f5435b45d6fe22b5c6f682da57faae71b88.nq.gz
│   ├── 2a666868d6afab6d4e92840408df623a225badcb.nq.gz
│   ├── 35610a1208a575b14810bac31b96e745786ab638.nq.gz
│   ├── 464effa6b90273ce360b8b28b7729b92223ded22.nq.gz
│   ├── 4e4ef9ff844bfb8210fa636dad9b16ed6102a729.nq.gz
│   ├── 50b8f71dd1078086002ca5194ff421f17750df30.nq.gz
│   ├── 585940699b5b99df6541c819a773ef738985a956.nq.gz
│   ├── 5e12f76db14a2b535c34335920691e4b33d5b466.nq.gz
│   ├── 6b85859ad9a4c44ed3dcbc470a26c727d287713f.nq.gz
│   ├── 71466b258fca396514dda5f1c98d3a45f9e146bf.nq.gz
│   ├── 72dac8b43a1b23305b516d60d88251bd2299c64b.nq.gz
│   ├── 7a60e11de94b030d8de40429a35879ddaa8240d1.nq.gz
│   ├── 8706d1453f1902c27f95f1c887ecddd1876db392.nq.gz
│   ├── 87a06fa74576deffe3363f2c41c8fb66507bcef0.nq.gz
│   ├── 882cd07f7c20778c072642e35937e2418ba684d1.nq.gz
│   ├── 8948e112e6fc769b78709f305e3bec98f75d239f.nq.gz
│   ├── 94c1d695060f17017e07c127c32ed9e1e586ada0.nq.gz
│   ├── 95b9167e5128237645230c9e58a8c1f8f6ecb4bf.nq.gz
│   ├── 9ab4ff516d7d3970d51029ebce84d7c62e2c96c8.nq.gz
│   ├── 9c43d0671538c58f50dfdab5c16844ceb0c7f9ee.nq.gz
│   ├── 9e620aff0e26005edf9e6ce1c9f27257d7251cd5.nq.gz
│   ├── aa4773eccfa544ac9164441a48c69ca5b0a8abd9.nq.gz
│   ├── bce9d0b476d4710cd55b939e8ee3e858e4c2c9ca.nq.gz
│   ├── bfdb08a4738f7cfa0ce836c76954ad9391204af7.nq.gz
│   ├── cbee5695b8e13f98d8162c2c69edc95818139f8b.nq.gz
│   ├── d2385006f875f97aee9399b7a071a943c71b9681.nq.gz
│   ├── e071a04b83eb361338208a449b5a1469f71a61b9.nq.gz
│   ├── e338edd8f49f89f1ca13e8422fcfde5c103a4146.nq.gz
│   ├── e638a24c97d9c075008f52db7b325a653c18934a.nq.gz
│   ├── e67fa637b7446dbd6931afc6dac6f21ad30ca29b.nq.gz
│   ├── e894441c0f6c9d6c22adfd407ae5dd4048126977.nq.gz
│   └── eabfa5f7af0a111c51df76e54bd7766d0a248826.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 573b616b9a2de79b21545ae7f57845456f82f4e0.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 45 files
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

[agronholm/docker-atlassian-confluence](https://github.com/agronholm/docker-atlassian-confluence)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
