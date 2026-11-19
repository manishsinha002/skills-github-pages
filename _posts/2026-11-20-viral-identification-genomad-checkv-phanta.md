---
layout: post
title: "Starter Methods Overview: geNomad, CheckV, and Phanta"
date: 2026-11-20
categories: methods benchmarks
---

Our initial release features three foundational tools covering viral identification, quality control, and abundance profiling: **geNomad**, **CheckV**, and **Phanta**.

## Method Comparison

| Method | Primary Task | Input Type | Key Output | Reference |
| :--- | :--- | :--- | :--- | :--- |
| **geNomad** | Virus & plasmid identification | Assembled contigs | Classification scores, marker annotations | Camargo et al., *Nat Biotechnol* (2024) |
| **CheckV** | Viral genome quality & completeness | Viral contigs | Completeness %, contamination, provirus boundaries | Nayfach et al., *Nat Biotechnol* (2021) |
| **Phanta** | Joint prokaryotic & viral profiling | Short-read metagenomes | Relative abundance tables (species/vOTU level) | Pinto et al., *Nat Biotechnol* (2024) |

## When to Use Which Tool
* **Use geNomad** when mining assembled metagenomes or metatranscriptomes for novel viral sequences and mobile genetic elements.
* **Use CheckV** immediately after viral contig identification to filter out host contamination and estimate genome completeness.
* **Use Phanta** when you need fast, read-level taxonomic quantification of both bacteria and viruses from bulk shotgun sequencing without prior assembly.

## Benchmark & Schema Notes
All three entries are validated against our **Method Comparison Data Model** and linked to primary benchmark datasets in the repository's `data/` directory.
