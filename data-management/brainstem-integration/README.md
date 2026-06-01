# BrainSTEM integration *(dedicated repository to be created)*

> **Placeholder.** A dedicated public repository will be created for this tool and added
> here as a submodule, replacing this folder.

Programmatic synchronization of experimental **notes and metadata** with
[BrainSTEM](https://brainstem.org) (the collaborative lab notebook developed by Team BCP
Oxytocin) via its API. Lets researchers maintain notes in BrainSTEM and
push/pull subject, session, and recording metadata to/from the data pipeline, while
remaining compatible with the spreadsheet-based workflow.

## Current state (reference implementation)

Implemented and in use within the **Tongue–Jaw Oscillators (TJO)** project
(`processing/brainstem_api/`):

- `push_subject.py` — POST/PATCH subjects and sessions/recordings to BrainSTEM
  (all TJO subjects and recording sessions synced).
- `fetch_subject.py` — retrieve subject metadata by UUID (used for control subjects).
- Token-based (JWT) auth, dry-run mode, task→assay mapping.

## To do before extraction to this repo

- ⚠️ **Scrub credentials.** The TJO implementation reads a JWT token file
  (`brainstem-api-workstation-access.txt`). Move code only; replace secrets with a
  template + `.gitignore`, and verify no tokens enter Git history.
- Generalize hard-coded TJO setup/assay UUIDs into configuration.
- Add behavior links (Session–Subject–Setup–Assay) once the new assay is approved.
