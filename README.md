# Clinical NLP Triage (Synthetic Data) — Red-Flag Extractor

**Goal:** surface red-flag terms from clinical case notes to support tele-triage decisions.  
**Author:** Alfredo Martín Gil, MD — Emergency & Dialysis | Healthcare AI & Telemedicine | Patient Safety

## Problem
Case notes are long; telemedicine teams need a fast, safe way to spot risk signals during triage.

## Data (Privacy & Ethics)
- Synthetic notes only (no PHI).
- Public symptom/term dictionaries + handcrafted templates.
- This repo is for education/prototyping, *not* clinical deployment.

## Method (baseline)
- Simple NLP pipeline (regex/keyword lists) + optional ML baseline (bag-of-words/LogReg).
- Output: list of red-flag terms with spans + simple risk counter.

## Metrics
- Precision/Recall on a small labeled synthetic set.
- Throughput: notes/minute on typical hardware.
- Error analysis: false positives/negatives table.

## Limitations & Safety
- Not a diagnostic tool; *do not* deploy on real patients.
- Bias risks (language/age/phrasing); mitigation via lexicon review and threshold tuning.
- Requires clinician validation before any operational use.

## How to Run (Colab-ready)
1. Open the Colab notebook `clinical_nlp_triage.ipynb`.
2. Run cells top-to-bottom (no external data needed).
3. Inspect outputs; adjust lexicon/thresholds in the config section.

## Roadmap
- Add simple negation handling (e.g., "no chest pain").
- Try lightweight embeddings (optional).
- Export JSON for dashboard integration.

---
*Remote & Toronto-ready. Feedback and collaborations welcome.*
