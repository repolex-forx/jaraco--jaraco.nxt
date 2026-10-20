# Repolex Knowledge Graph of jaraco/jaraco.nxt

RDF knowledge graph data for [jaraco/jaraco.nxt](https://github.com/jaraco/jaraco.nxt), parsed by [repolex](https://repolex.ai).

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
rlex download jaraco/jaraco.nxt
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 853d1468913f7b0b3161723ea068c91fb8660868
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 853d1468913f7b0b3161723ea068c91fb8660868
│           └── chunk-001.nq.gz
├── blob
│   ├── 1f2aa7533b0423a8eb943f6f4ec02498e39581a0.nq.gz
│   ├── 2e3f4dd791a6372b427d618eb0baa8c4dc58e5f0.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 362466c01d3f46046ba6a2b5f4b950ac5fda9992.nq.gz
│   ├── 4f0f30ee65edbc32dec2eb9e586d04aa3e954668.nq.gz
│   ├── 54c9000ec94341dd65c2053251b85b124017b9b5.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 575a3057a1b27141a092e46d76c8aab48b614657.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 59a599eeedadcccb9e0b43d7dc41a57b24622ece.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 5c05f9e27d57a4b7a3c3a9fdfecf8cddb8be499f.nq.gz
│   ├── 5deef4803b17ac6cd08a0a08248da5e3b58b9f4b.nq.gz
│   ├── 623402d29e173bf4f4aceb7b830c18a89ccca06e.nq.gz
│   ├── 6592fd5f1592a5b11e4b17444cde5cb5c4e7c8fa.nq.gz
│   ├── 69eceb2334d4cca3e48eb1a578b8ae52de888fe6.nq.gz
│   ├── 6a021ad1e53cdfbc06afd15d9a421ecfed16bfd4.nq.gz
│   ├── 6dfb99ddaa3db2b782ecc65dac6786b7e59deb0a.nq.gz
│   ├── 6f4fa7477cd7e96543d67c2fe1074878b592373f.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── 73055b49cae0f19c81e3c6c051075cf9da0fb1d6.nq.gz
│   ├── 756621094ed5c0d110edd192229fa5c4dd1a7108.nq.gz
│   ├── 854f749b510d729051a5d18c70a13b81227bc5bb.nq.gz
│   ├── 87af18233e234d5940a8b72da707ab5f5b4dce36.nq.gz
│   ├── 8e6bab12f742ffb3e4883044c6d91603fce657ff.nq.gz
│   ├── 965dc838b78faefff43e59553911a80624d0a103.nq.gz
│   ├── 9a0f3bce1395ae3819030b822e5d9076c85068ea.nq.gz
│   ├── 9b5110bcc5f3843797d528172b8f561cb358dc85.nq.gz
│   ├── aea3991c725d090c5581f7c525905e4959146ff2.nq.gz
│   ├── af6cca5753e68fd62799824202d6051cd265dcb1.nq.gz
│   ├── b4506f2a74423afc2cbfb109f92c76c94c5bb26b.nq.gz
│   ├── c3f29b424a7c7ec13da967efd87ba5825e8526f8.nq.gz
│   ├── cfbbec257214d0c22f88046622eaa216daa9e804.nq.gz
│   ├── d36fa49b9265f54551077198d8c8c78f7d652c9c.nq.gz
│   ├── d46dce0dba58bd2896356b882e467209ffa4f28b.nq.gz
│   ├── dcab614ae4ce377921cd9a904d87bb8dd236a8f2.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── e8a995329bfda8c6f526d2d356c7f993ac4495fc.nq.gz
│   └── efcb8cbc2043faa7caf4f92fc7488bd6914c934c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 853d1468913f7b0b3161723ea068c91fb8660868.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 48 files
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

[jaraco/jaraco.nxt](https://github.com/jaraco/jaraco.nxt)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
