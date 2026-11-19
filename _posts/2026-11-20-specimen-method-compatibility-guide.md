---
layout: post
title: "Specimen–Method Compatibility Guide for Human Virome Studies"
date: 2026-11-20
categories: guides specimens
---

Selecting the right bioinformatic pipeline depends heavily on the biological sample type, viral biomass, and wet-lab enrichment strategy used prior to sequencing.

## Specimen Compatibility Matrix

| Specimen Type | Typical Viral Biomass | Key Wet-Lab / Bioinformatic Challenge | Recommended Workflow Focus |
| :--- | :--- | :--- | :--- |
| **Stool / Gut** | High | High bacterial background in bulk metagenomes; complex phage diversity | Read-level profiling (e.g., **Phanta**) or assembly + **geNomad** / **CheckV** |
| **Saliva / Oral** | Moderate | High host DNA contamination; high strain-level variation | Aggressive host-read removal prior to contig assembly and **geNomad** classification |
| **Plasma / Blood** | Very Low | Low viral nucleic acid yield; reagent/kit contamination ("kitome") | Strict negative-control filtering; sensitive marker + neural net detection (**geNomad**) |
| **Respiratory Swabs** | Low to Moderate | Dominated by host and bacterial reads; RNA viruses often targeted | Metatranscriptomic assembly + host depletion + quality filtering (**CheckV**) |

## Best Practices Before Running Virome Tools
1. **Host Depletion:** Always remove human reads (`GRCh38` / `T2T-CHM13`) before assembly or read-based profiling to prevent false-positive viral calls.
2. **Enrichment Awareness:** Distinguish between **VLP-enriched (virus-like particle)** viromes and **bulk shotgun metagenomes**, as VLP prep biases abundance estimates toward free virions over integrated prophages.
3. **Contig Quality Thresholds:** Filter assembled viral contigs with **CheckV** (e.g., retaining medium-quality, high-quality, or complete genomes) before downstream ecological comparisons.

## Contributing Specimen Data
If you have benchmarked a pipeline on an under-represented human tissue or biofluid, submit an update via our **Specimen–Method Compatibility** CSV template.
