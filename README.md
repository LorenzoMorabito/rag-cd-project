# RAG CD Project

## Overview

This repository contains the design foundations and knowledge assets for a Retrieval-Augmented Generation (RAG) project focused on the **IQVIA ChannelDynamics** domain.

The project is organized around three distinct knowledge layers:

1. **Canonical Business Knowledge Layer**  
   The main business corpus used for document retrieval and grounded question answering.

2. **Analytical Semantic Insight Layer**  
   A semantic context layer used to enrich retrieval with analytical meaning, measure-family interpretation, dimension usage patterns, and time-behavior logic.

3. **Technical Query Grounding Layer**  
   A technical grounding layer used to support schema-aware reasoning, correct query construction, join resolution, and technical validation.

The repository is intentionally structured to keep these scopes separate, so that business meaning, analytical interpretation, and technical grounding do not get mixed into the same document layer.

---

## Project Goals

The main goals of the project are:

- build a structured RAG-ready knowledge base;
- support grounded answers over enterprise-like documentation;
- preserve clear separation between business, semantic, and technical knowledge;
- prepare the repository for future ingestion, retrieval experiments, evaluation, and demo development;
- create a portfolio-ready project that demonstrates corpus design, retrieval architecture, and evaluation thinking.

---

## Repository Structure

```text
.
├── corpus/
│   └── channeldynamics/
│       ├── 00_raw/
│       ├── 01_overview/
│       ├── 02_governance/
│       ├── 10_glossary/
│       ├── 20_channel_definitions/
│       ├── 30_attributes/
│       ├── 40_measures/
│       ├── 50_examples/
│       └── 70_registry/
│
├── semantic_context/
│   └── promo_insights/
│       ├── 00_raw/
│       ├── 01_overview/
│       ├── 02_governance/
│       ├── 10_docs/
│       ├── 60_registry/
│       └── 70_catalogs/
│
├── technical_context/
│   └── promo_metadata/
│       ├── 00_raw/
│       ├── 01_overview/
│       ├── 02_governance/
│       ├── 10_schema/
│       ├── 20_table_profiles/
│       ├── 30_quality/
│       ├── 40_appendix/
│       ├── 60_registry/
│       └── 70_catalogs/
│
├── docs/
│   ├── project/
│   └── standards/
│
├── evals/
├── src/
├── .gitignore
├── README.md
└── requirements.txt
```

---

## Layer Description

### 1. Canonical Business Knowledge Layer

Path:

```text
corpus/channeldynamics/
```

This is the primary business corpus of the project.  
It contains structured markdown knowledge objects describing:

- glossary entities;
- channel definitions;
- attribute definitions;
- measure definitions;
- examples;
- governance material;
- registry files for ingestion and review.

This layer is the main source for business-facing document retrieval.

---

### 2. Analytical Semantic Insight Layer

Path:

```text
semantic_context/promo_insights/
```

This layer enriches the system with analytical interpretation that is not always explicit in the business corpus.

It includes material such as:

- measure-family semantics;
- dimension usage patterns;
- formula patterns;
- time behavior logic;
- source traceability;
- merge guidance.

This layer is intended to improve retrieval quality and analytical understanding, especially when questions involve measure interpretation rather than only definitions.

---

### 3. Technical Query Grounding Layer

Path:

```text
technical_context/promo_metadata/
```

This layer provides technical grounding for schema-aware reasoning and future query generation.

It includes:

- schema overviews;
- relationship maps;
- table profiles;
- technical metadata catalogs;
- quality notes;
- overlap analysis;
- registry files;
- table/column/join catalogs.

This layer is not the main business corpus.  
Its purpose is to support correct technical grounding and future query generation workflows.

---

## Documentation

Project documentation is stored under:

```text
docs/
```

### `docs/project/`
Contains project-level documents such as:
- project overview;
- project exports;
- future architectural documents.

### `docs/standards/`
Contains methodological and internal guideline documents used as reference for document quality and RAG corpus preparation.

---

## Current Status

The repository is currently in a **corpus-first design phase**.

At this stage, the main focus has been:

- structuring the repository architecture;
- separating the three knowledge layers;
- organizing the available packages into coherent scopes;
- preparing the foundation for future implementation.

The following implementation layers already exist but are still intentionally minimal:

- `src/`
- `evals/`

These will be expanded in the next development steps.

---

## Planned Development Workflow

The planned workflow for the project is:

1. finalize repository architecture;
2. validate layer boundaries and naming conventions;
3. define ingestion logic;
4. implement retrieval experiments;
5. build benchmark questions and evaluation routines;
6. add demo notebooks or scripts;
7. refine documentation and make the project portfolio-ready.

---

## Intended Use of Each Layer

| Layer | Purpose | Main Use |
|------|---------|----------|
| `corpus/channeldynamics` | canonical business knowledge | grounded business retrieval |
| `semantic_context/promo_insights` | analytical semantic enrichment | interpretation and retrieval enhancement |
| `technical_context/promo_metadata` | technical grounding | schema-aware reasoning and future query generation |

---

## Design Principles

This repository follows a few explicit design principles:

- **clear separation of scopes**
- **business corpus kept distinct from technical metadata**
- **semantic interpretation treated as a dedicated layer**
- **registry files separated from descriptive markdown objects**
- **documentation-first architecture before implementation**

The goal is to avoid building a flat and ambiguous repository where business definitions, technical schema notes, and analytical logic are mixed together.

---

## Next Steps

The next concrete steps are:

- populate `src/` with ingestion and retrieval utilities;
- define benchmark queries under `evals/`;
- add implementation notebooks or scripts;
- document evaluation logic;
- refine the root README as the project becomes executable.

---

## Repository Status

This repository should currently be read as:

- a **well-structured RAG knowledge architecture**,  
- not yet a fully implemented RAG application.

The implementation phase will build on top of this directory structure.

---

## Notes

This repository is intentionally designed to support both:
- **document-oriented RAG**, and
- **future query-grounded reasoning workflows**.

That is why the project keeps separate:
- business knowledge,
- semantic analytical context,
- technical schema grounding.
