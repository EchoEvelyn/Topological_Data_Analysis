# Topological Data Analysis of Protein Structures via Persistent Homology

## Overview

This project systematically applies **persistent homology**, a tool from topological data analysis (TDA), to compare and characterize the three-dimensional structures of three representative proteins:
- Hemoglobin (4HHB)
- Creatine Kinase (1CRK)
- Protein Kinase A (1ATP)

By extracting atomic point clouds from PDB structures and analyzing their topological features across multiple scales, the project uncovers both shared and distinct structural fingerprints that are robust to noise and geometric perturbations.

## Background & Motivation

Traditional geometric and statistical tools capture local motifs or global folding patterns of proteins, but often miss higher-order connectivity and multiscale cavities/loops. Persistent homology enables the quantification of such features (connected components, loops, voids) and provides **topological fingerprints** for robust protein comparison.

## Key Features

- Automated point cloud extraction from PDB files using Bio.PDB
- Vietoris-Rips persistent homology (via ripser/gtda) up to dimension 2
- Visualization:
    - 3D point clouds
    - Barcode plots
    - Persistence diagrams
    - Betti curves
    - Feature lifetime histograms
    - Spatial mapping of persistent features
- Quantitative metrics:
    - Persistence entropy
    - Wasserstein distance for topological similarity assessment

## File Structure

```
DSC214/
├── 1ATP.pdb                   # Protein structure: Protein Kinase A
├── 1CRK.pdb                   # Protein structure: Creatine Kinase
├── 4hhb.pdb                   # Protein structure: Hemoglobin
│
├── images/                    # All generated images/figures for report
│   └── ... (plots, diagrams, etc.)
│
├── Project.ipynb              # Main Jupyter notebook for all analysis
├── TDA_statistics.txt         # Summary statistics (loops, persistences, etc.)
├── Wasserstein_distances.txt  # Wasserstein distance results (topological similarity)
├── requirements.txt           # Required Dependencis
│
└── ... (other files or folders as needed)
```

## Quick Start

1. Clone the repository and install dependencies:
    ```bash
    git clone https://github.com/yourusername/Topological_Data_Analysis.git
    cd Topological_Data_Analysis/DSC214
    pip install -r requirements.txt
    ```

2. Run the main notebook:
    - Open `Project.ipynb` in Jupyter Notebook or VS Code.
    - Run all cells to reproduce the TDA workflow.
    - All figures will be saved to the `images/` directory.

## Dependencies

```bash
pip install -r requirements.txt
```

## References

- Protein structure data were obtained from the RCSB Protein Data Bank (PDB):
  https://www.rcsb.org/

  Berman, H. M., Westbrook, J., Feng, Z., Gilliland, G., Bhat, T. N., Weissig, H., ... & Bourne, P. E. (2000). The Protein Data Bank. *Nucleic Acids Research*, 28(1), 235–242. [https://doi.org/10.1093/nar/28.1.235](https://doi.org/10.1093/nar/28.1.235)

