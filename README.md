# Care-Voice AI

## Overview
Care-Voice AI is a voice-based patient request classification and prioritisation project. This repository contains the Phase 1–4 implementation and evaluation.

## Phase 1–4 Implementation
- Medical speech dataset preparation and validation
- Audio manifest creation and dataset splits
- TF-IDF + Logistic Regression baseline
- Class-balanced TF-IDF experiment
- ClinicalBERT text classification
- Validation, test evaluation, and error analysis
- Whisper speech transcription experiment
- Model performance comparison and visualisation

## Request Classes
- Emergency
- Pain
- Assistance
- General

## Validation Results

| Metric | TF-IDF | ClinicalBERT |
|---|---:|---:|
| Accuracy | 80.06% | 92.89% |
| Macro-F1 | 78.04% | 93.16% |
| Emergency Recall | 67.55% | 88.08% |
| Assistance Recall | 65.57% | 100.00% |

**Selected text classifier:** ClinicalBERT, based on validation performance.

ClinicalBERT achieved 85.18% macro-F1 on the held-out test set. Refer to the saved test report for complete results.

## Repository Structure
- `notebooks/` — Phase 1–4 implementation notebook
- `source_code/` — Project source modules
- `results/` — Evaluation reports and generated outputs
- `Final Scores.png` — Visual comparison of validation metrics

## How to Run
1. Open the notebook in Kaggle or Jupyter.
2. Attach the required medical speech dataset.
3. Install the notebook's required Python dependencies.
4. Update dataset paths if necessary.
5. Execute the cells in order.

## Data and Model
The original dataset and trained model weights may be stored separately from this repository. Follow the team's agreed sharing method to access them.

## Scope of This Handover
This repository covers **Phases 1–4 only**. The acoustic branch, multimodal integration, priority rules, and dashboard are outside this handover.

## Evaluation Notes
Validation and held-out test results are reported separately. The Whisper transcript-classification experiment uses a 50-clip sample and should be interpreted as a small-sample evaluation, not a guarantee of real-world clinical performance.
