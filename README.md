# EEG-tGAT: Temporal Graph Attention Framework for EEG Classification

## Overview

This repository implements EEG-tGAT, a spatiotemporal graph attention framework designed for EEG-based binary classification. The model explicitly captures:

- Intra-channel temporal dynamics
- Inter-channel spatial dependencies
- Attention-based feature aggregation
- Subject-independent generalization

The architecture integrates temporal feature extraction with graph attention mechanisms to model structured EEG signals as dynamic relational data.

This work was accepted in [GCON 2026](https://arxiv.org/abs/2604.10149) (IEEE Guwahati Subsection)

---

## Methodology

### 1. Temporal Modeling
EEG signals are segmented into fixed-duration windows to capture localized temporal dynamics.

### 2. Graph Construction
Each EEG channel is treated as a node in a graph. Edges are constructed to model spatial or signal-based relationships between channels.

### 3. Graph Attention Layers
GATv2 layers are applied to learn adaptive attention weights between connected channels, enabling selective information propagation.

### 4. Classification
Graph-level representations are obtained through global pooling and passed to a fully connected classifier for binary prediction.

---

## Experimental Setup

- Cross-validation: Subject-independent strategy
- Evaluation Metrics:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Cohen’s Kappa

---

## Repository Structure

```
EEG-tGAT-Framework/
│
├── notebooks/        # Experimental pipeline
├── src/              # (Future modular implementation)
├── results/          # Saved outputs and visualizations
├── requirements.txt  # Project dependencies
└── README.md
```

---

## Reproducibility

Clone the repository and install dependencies:

```bash
pip install -r requirements.txt
```

Then execute the notebook in the `notebooks/` directory.

---



