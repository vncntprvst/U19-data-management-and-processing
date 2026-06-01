# NWB conversion examples for DANDI deposition *(dedicated repository to be created)*

> **Placeholder.** A dedicated public repository will be created for this tool and added
> here as a submodule, replacing this folder.

Worked, end-to-end examples of converting raw experimental data to NWB and depositing the
result on the [DANDI Archive](https://dandiarchive.org), drawn from real published U19
datasets. Intended as copy-and-adapt references for trainees and collaborators.

## Planned contents

- **Peri-head distance PrV** — full conversion + deposition example
  (DANDI **001687**; manuscript: *2026 Xiao–Severson, Peri-head distance*).
  Source today: `wanglab_nwb` repo → `projects/Peri-head distance PrV`.
- Additional per-modality examples as further datasets are deposited.

## Relationship to other tools

- **`dataset-manager`** generates a *custom* conversion script per project.
- **`ingestion_scripts`** is the broad library of modality/language examples.
- This repo collects *complete, published* conversion→deposition walkthroughs tied to
  specific dandisets.

## To do before extraction to this repo

- Extract the Peri-head distance conversion from `wanglab_nwb` (code + minimal/synthetic
  sample data, not full datasets).
- ⚠️ Remove any DANDI API tokens / credentials; use environment variables + templates.
