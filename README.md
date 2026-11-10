# Repolex Knowledge Graph of rust-num/num-traits

RDF knowledge graph data for [rust-num/num-traits](https://github.com/rust-num/num-traits), parsed by [repolex](https://repolex.ai).

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
rlex download rust-num/num-traits
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1166177ec398601d6dd4d88891cf7674f3978888
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1166177ec398601d6dd4d88891cf7674f3978888
│           └── chunk-001.nq.gz
├── blob
│   ├── 0a198a1f33055d8774664d95b7bffd1df092df6a.nq.gz
│   ├── 16a0045767ac9520534cfacd7dd26246b5f01db3.nq.gz
│   ├── 16fe87b06e802f094b3fbb0894b137bca2b16ef1.nq.gz
│   ├── 194427d22da4235784bdfc1156112ab4c235aec5.nq.gz
│   ├── 2128d86a2dab38c786e7571ba32a64e01d5594f2.nq.gz
│   ├── 25ec873258ece9e7ecaa6f143a689b1a5f396685.nq.gz
│   ├── 39d4bdb5acd313c1a92dbeaa1c379aaf0596a315.nq.gz
│   ├── 3a8b3311675310ca28bea4df516e352ab20b94ac.nq.gz
│   ├── 4124e92ceb8ed5b8b21546ea5b41fedfcc505879.nq.gz
│   ├── 43212c77e3470bb8ef7937e317135df8dcdc7fc1.nq.gz
│   ├── 49e67552480c7b4ea60483db7c82ef51a6165eb1.nq.gz
│   ├── 4c91817014fc5ebe711edadc6ef23c0425c34f2f.nq.gz
│   ├── 51beb5572681f4fdcc4dc6bfdae994c28f770689.nq.gz
│   ├── 553b28be1421c800866d1a0e3419d65ee59f3a3c.nq.gz
│   ├── 5f23f56ad53ba5340442eb1b40c7e45dce6258d1.nq.gz
│   ├── 7087d09d0162dc15935d2fccfb9864412d8b254d.nq.gz
│   ├── 785d760efcd45a4385c1f955c1188e2b70bc1c14.nq.gz
│   ├── 7da75312ab1b758f283cfc8c7397a3d63ab07275.nq.gz
│   ├── 7e5fd3a223b4fa160a1ff823089e14bf2b0dcdd8.nq.gz
│   ├── 821a7fdc772da0ec3ea466a5cdce58d2dae761eb.nq.gz
│   ├── a0d6b0fd6c0b174c81f1ca4d2efa0719cfca130b.nq.gz
│   ├── ac27bc453bf051460a06bfb31e18b590c06396ce.nq.gz
│   ├── b0ddbe27adbd78287a872bb07ee107ab837f771b.nq.gz
│   ├── b97758e42c7354de4c20ca685c489588461ecc53.nq.gz
│   ├── c6284bf4e807563b23af37f2a926b58b966578c7.nq.gz
│   ├── c7a35a51c1228ff72c40adbd7286b1097b27b196.nq.gz
│   ├── d916436ff9c49f677313bde2a5c30fde7878ebd7.nq.gz
│   ├── e2679409f1148fb33b149e63e19939c5f9af034f.nq.gz
│   ├── e580e2c5e606c6184395dbf87b9072ef5cb4956e.nq.gz
│   ├── ef51c954d7b9705196d10fb04ae6fecc69a28eb0.nq.gz
│   ├── f6a8030a2b58a052d672b448eef4d07c65fea137.nq.gz
│   └── fa8d85ac52f19959d6fc9942c265708b4b3c2b04.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1166177ec398601d6dd4d88891cf7674f3978888.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 40 files
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

[rust-num/num-traits](https://github.com/rust-num/num-traits)

---
*Parsed on 2026-11-10 by [repolex](https://repolex.ai)*
