# Repolex Knowledge Graph of bestiejs/benchmark.js

RDF knowledge graph data for [bestiejs/benchmark.js](https://github.com/bestiejs/benchmark.js), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download bestiejs/benchmark.js
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a37c36c02fec8631da710de983bfd9a05586e751
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── a37c36c02fec8631da710de983bfd9a05586e751.nq.gz
│   └── repolex
│       └── a37c36c02fec8631da710de983bfd9a05586e751
│           └── chunk-001.nq.gz
├── blob
│   ├── 060329d5704814d19f1b910b3cb2464991377422.nq.gz
│   ├── 13ceba4fe4a055bb29ee78c8a92ddb27671b42f7.nq.gz
│   ├── 176a458f94e0ea5272ce67c36bf30b6be9caf623.nq.gz
│   ├── 2b78688077fcc4316cd5320269ef6f6da157fc58.nq.gz
│   ├── 414984409da106021ca34c5e4afd1dc098d22cbe.nq.gz
│   ├── 425f37a1899a3b395ebaf4517ad36e5612cf7ca6.nq.gz
│   ├── 452c8125036a11092e0ceac37a206ff3ffffdc52.nq.gz
│   ├── 59b9954847f3d634ec4eeed4bdd46eeb0e391438.nq.gz
│   ├── 65d92b588da958c26d00d32567c417368e783af3.nq.gz
│   ├── 83f903f894036473d24cb9ace214fc1a17a39f21.nq.gz
│   ├── ac395f7e4280e9d75b953fe50de3b98949794658.nq.gz
│   ├── b4306ab43fa6c64cfed4fe1c7fd858fb91f376cf.nq.gz
│   ├── c831e48555493f725cb6b6f7a09bffd223c2fe57.nq.gz
│   ├── e90ad529826541c11886ec1e1652721aa1a53e6d.nq.gz
│   ├── f372f5cf8f846438e31b7423b8b78d0b5e96816a.nq.gz
│   └── fd4d2f9aa5ce691d97859cde62b52771b4fb37c8.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── a37c36c02fec8631da710de983bfd9a05586e751.nq.gz
├── filetree
│   └── a37c36c02fec8631da710de983bfd9a05586e751.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 26 files
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

## Source repository

[bestiejs/benchmark.js](https://github.com/bestiejs/benchmark.js)

---
*Parsed on 2026-04-09 by [repolex](https://repolex.ai)*
