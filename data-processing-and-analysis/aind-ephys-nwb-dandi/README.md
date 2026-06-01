# AIND ephys pipeline ↔ NWB / DANDI

> **Repository:** https://github.com/vncntprvst/aind-ephys-nwb-dandi
> This folder is a pointer; it will be replaced by that repo as a git submodule:
> ```bash
> git submodule add https://github.com/vncntprvst/aind-ephys-nwb-dandi.git \
>     data-processing-and-analysis/aind-ephys-nwb-dandi
> ```

Integration of the Allen Institute for Neural Dynamics (AIND) electrophysiology
processing pipeline (Kilosort4-based spike sorting via a containerized Nextflow workflow)
with NWB conversion and DANDI deposition, running on an HPC cluster (MIT Engaging / ORCD,
SLURM + Apptainer).

Key scripts in the repo: `AIND/aind_ephys_submit.sh` (SLURM submit wrapper, multi-probe,
resume, IBL-destripe + lick-masked variants), `AIND/convert_npx_rec_to_nwb.py`
(Open Ephys → DANDI-compliant NWB), `AIND/export_xp_notes_aind.py`,
`AIND/organize_data.sh`, `AIND/combine_aind_ephys.sh`, and `process_subject.sh`
(end-to-end orchestrator). Credentials are templated (`config/config.env.template`,
`AIND/utils/kachery_envs.example.sh`) and gitignored.
