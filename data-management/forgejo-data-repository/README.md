# Forgejo data repository (NAS-based project metadata)

A lightweight, on-site approach to versioned **project metadata**: a private
[Forgejo](https://forgejo.org/) Git server runs on the performance-center NAS, and each
project pushes its per-subject and per-session metadata (as JSON) to a repository there.

This complements — it does not replace — the public DANDI archive:

- **DANDI** holds the converted, published datasets (NWB) for public sharing.
- **The Forgejo repo** holds the live, versioned metadata *while a project is ongoing*,
  on storage the lab controls, with full Git history. It feeds the DataJoint ingestion
  pipeline and is the working source of truth before deposition.

## How it works

1. Metadata is maintained as small JSON files, one per subject and one per session
   (see [`example/`](example/)).
2. A push step (manual today; to be automated) commits and pushes updated JSON to the
   project's Forgejo repository on the NAS, e.g.
   `http://<nas-host>:<port>/<user>/<project>-metadata.git`.
3. Downstream, the DataJoint ingestion reads these files to register subjects, sessions,
   recordings, and processing status.

## Reference implementation

First implemented for the **Tongue–Jaw Oscillators (TJO)** project, whose metadata repo
lives on the performance-center NAS. See the TJO ingestion plan for the full data
workflow (acquisition → transfer → preprocessing → backup → ingestion → sharing).

## Status

- ✅ Metadata JSON schema in use; consumed by DataJoint ingestion.
- ⏳ Automated push to the Forgejo repo (currently a manual `git` step).
- ⏳ Generalization beyond TJO to additional projects / performance centers.

> **Note:** the example files below are synthetic and illustrate the schema only. Real
> project repos live on the private NAS Forgejo server.
