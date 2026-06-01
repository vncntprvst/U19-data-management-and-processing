# U19 Data Management and Processing

Umbrella repository for the **Data Science Core (Core 1)** of the U19 BRAIN Circuit
Program *"High- and low-level computations for coordination of orofacial motor actions."*
It lists and documents the complementary tools the Core provides for managing, processing,
and sharing neurophysiology data. Each tool lives in its own repository (added here as a
**submodule**) or, where a full repo isn't warranted, as a folder.

To clone with all submodules:

```bash
git clone --recurse-submodules https://github.com/vncntprvst/U19-data-management-and-processing.git
# or, after a plain clone:
git submodule update --init --recursive
```

## Data management

Complementary approaches to organizing, storing, and annotating data.

| Tool | What it does | Location |
|---|---|---|
| **[Dataset manager](data-management/dataset-manager)** | Guided app that generates a custom metadata template + NWB conversion script per project. | submodule → `vncntprvst/dataset-manager` |
| **[Backup and processing](data-management/backup_and_processing)** | Acquisition→NAS backup, metadata consolidation, and remote-trigger of cluster processing. | submodule → `vncntprvst/backup_and_processing` |
| **[Forgejo data repository](data-management/forgejo-data-repository)** | On-site, versioned project-metadata store on the NAS (with example schema). | folder (README + example) |
| **[BrainSTEM integration](data-management/brainstem-integration)** | Programmatic sync of notes/metadata with brainstem.org via its API. | *repo to be created* |

## Data processing and analysis

Pipelines and examples for turning raw data into shareable, analyzable products.

| Tool | What it does | Location |
|---|---|---|
| **[AIND ephys ↔ NWB / DANDI](data-processing-and-analysis/aind-nwb-dandi)** | AIND Kilosort4 spike-sorting pipeline integrated with NWB conversion + DANDI, on an HPC cluster. | *repo to be created* |
| **[Ingestion scripts](data-processing-and-analysis/ingestion_scripts)** | Reference library of modality/language conversion examples and guidelines. | submodule → `Rhythm-n-Rodents/ingestion_scripts` |
| **[NWB conversion examples](data-processing-and-analysis/nwb-conversion-examples)** | Complete published conversion→deposition walkthroughs (e.g. Peri-head distance PrV, DANDI 001687). | *repo to be created* |

## Datasets on DANDI

- **001687** — Peri-head distance PrV (in press; embargoed until publication)
- **001472** — Separating cognitive and motor processes in the behaving mouse
- **001604** — Brainstem circuits generating/coordinating tongue & jaw rhythmic movements
- **001696** — Rodent bilateral whisker coordination
- **001619** — A brainstem map of orofacial rhythms (collaboration)

## Status

This repository is being assembled. Three tools (BrainSTEM integration, AIND↔NWB/DANDI,
NWB conversion examples) currently live inside project repositories and will be extracted
into dedicated public repositories — with credentials scrubbed — then added here as
submodules.
