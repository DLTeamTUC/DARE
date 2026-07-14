# DARE: Drift-Aware Robust Explanations in Unsupervised Intrusion Detection

This repository contains the research code for the paper:

**DARE: A Framework for Drift-Aware Robust Explanations in Unsupervised Intrusion Detection**  
Beny Nugraha and Thomas Bauschert  
IEEE International Conference on Cyber Security and Resilience (IEEE CSR 2026)

## Overview

DARE is an unsupervised intrusion detection framework designed for network environments where benign traffic changes over time. The framework combines:

- Variational Autoencoder based anomaly detection
- MAD-Robust Gradients for fast and stable explanations
- Dual-Gate Drift Detection using statistical and explanation-based signals
- Anomaly-Filtered Buffer for safer unsupervised adaptation
- Decoder-only fine-tuning to adapt to benign drift while preserving the learned latent structure

The goal is to maintain detection stability under benign concept drift, provide efficient explanations, and reduce the risk that malicious traffic contaminates the retraining buffer.

## Repository Status

This repository currently provides the main experimental notebook used for the DARE paper.

The code is released as research code. It is intended to support reproducibility and further experimentation, not as a production-ready IDS implementation.

## Repository Structure

```text
DARE/
├── README.md
├── LICENSE
├── requirements.txt
├── notebooks/
│   └── 01_dare_framework.ipynb
├── data/
│   └── .gitkeep
├── results/
│   └── .gitkeep
└── figures/
    └── .gitkeep
```

## Datasets

The datasets are not included in this repository.

The experiments in the paper use:

- CIC-DDoS2019
- CICIoT2023

Please download the datasets from their official sources and place the required files in the `data/` directory. The notebook assumes that the datasets are available locally.

## Main Experiments

The notebook covers the main components of DARE, including:

- Preprocessing and feature selection
- VAE training on benign traffic
- Reconstruction-error based anomaly detection
- MAD-Robust Gradient explanations
- Drift detection using statistical and explanation-based signals
- Buffer poisoning evaluation
- Safe adaptation with anomaly-filtered buffering and decoder-only fine-tuning
- Cross-subset detection evaluation

## Installation

Create a Python environment and install the required packages:

```bash
pip install -r requirements.txt
```

Then open the notebook:

```bash
jupyter notebook notebooks/01_dare_framework.ipynb
```

## Citation

If you use this repository, please cite the DARE paper:

```bibtex
@inproceedings{nugraha2026dare,
  author    = {Beny Nugraha and Thomas Bauschert},
  title     = {DARE: A Framework for Drift-Aware Robust Explanations in Unsupervised Intrusion Detection},
  booktitle = {Proceedings of the IEEE International Conference on Cyber Security and Resilience (IEEE CSR)},
  year      = {2026}
}
```

The final BibTeX entry will be updated once the official IEEE proceedings entry is available.

## License

This code is released under the MIT License.

## Contact

Beny Nugraha  
Chair of Communication Networks  
Chemnitz University of Technology  
beny.nugraha@etit.tu-chemnitz.de
