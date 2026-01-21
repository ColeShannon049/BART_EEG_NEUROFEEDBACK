# BART EEG & Neurofeedback Project

This repository contains task and analysis code developed during undergraduate research training in a neurotechnology laboratory at Queen’s University.  
The project combines a Balloon Analogue Risk Task (BART) with EEG-based measures to investigate brain–behavior relationships during risk-based decision-making.

---

## Repository Structure

BART_EEG_NEUROFEEDBACK/
├── Task/ # BART task implementation (PsychoPy)
├── Analysis/ # Behavioral and EEG analysis pipelines
│ ├── behavior/ # Behavioral summary & output generation
│ └── eeg/ # EEG analysis (single- and multi-XDF pipelines)
├── Config/ # Configuration files (example manifest)
├── README.md
└── .gitignore

yaml
Copy code

---

## Task: Balloon Analogue Risk Task (BART)

The BART task is implemented in **PsychoPy** and is designed to measure risk-taking behaviour under uncertainty.  
Participants make repeated decisions to inflate a virtual balloon to increase reward, with the risk of explosion increasing over time.

The task supports:
- Condition-dependent logic (e.g., neurofeedback vs sham)
- Trial-level event marking suitable for EEG analysis
- Integration with downstream behavioural and neural pipelines

---

## Behavioural Analysis

Behavioural analysis scripts process task output files to generate:
- Trial-level and subject-level summaries
- Risk-taking metrics derived from pump behaviour
- Condition- and group-based comparisons

These outputs are designed to align directly with EEG analyses and experimental grouping defined in the manifest.

---

## EEG Analysis

EEG pipelines are implemented in Python and Jupyter notebooks and support both **single-subject** and **batch (multi-subject)** workflows.

Analyses include:
- **Event-Related Potentials (ERP)**, including P300-focused metrics
- **Spectral band power** extraction
- **Neurofeedback-related task logic and features**
- Preprocessing, organization, and quality-control steps to support downstream analysis

This repository demonstrates analysis structure and methodology only; no raw EEG data are included.

---

## Manifest File (Condition & Group Assignment)

An example manifest file is provided in `Config/` to demonstrate how participants are programmatically assigned to experimental conditions and behavioural groups.

### Purpose of the manifest
The manifest enables:
- Automatic assignment of task condition (e.g., **NF** vs **SHAM**)
- Grouping based on gambling or risk-related behavioural profiles (e.g., **High / Low**)
- Consistent splitting of participants across task execution and analysis pipelines

### Ethics note
- The file included in this repository is an **example/template only**
- Subject identifiers and group labels are **synthetic**
- **No real participant metadata** are included or tracked
- Real manifests used during data collection are excluded and ignored via `.gitignore`

This approach reflects standard research practice for balancing **reproducibility** and **ethical data handling**.

---

## Data Policy

This repository contains **code only**.

- No raw EEG data (`.xdf`, `.edf`, etc.)
- No identifiable behavioral data
- No real participant manifests

All data-related files are excluded using `.gitignore`.

---

##  Tools & Methods

- Python
- PsychoPy (task implementation)
- Google Colab Notebooks
- EEG analysis workflows compatible with MNE-style pipelines
- ERP, band power, and neurofeedback-related feature extraction

---

## Author

**Cole Shannon**  
Queen’s University  
MSc applicant – Cognitive / Systems Neuroscience  
GitHub: https://github.com/ColeShannon049
