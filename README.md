# Topological Data Analysis of Protein Structures via Persistent Homology

This repository contains code, figures, and documentation for the project:
**Topological Data Analysis of Protein Structures via Persistent Homology**  
by Jingman Wang (UCSD, DSC214).

---

## Overview

This project systematically applies **persistent homology**, a tool from topological data analysis (TDA), to compare and characterize the three-dimensional structures of three representative proteins:
- Hemoglobin (4HHB)
- Creatine Kinase (1CRK)
- Protein Kinase A (1ATP)

By extracting atomic point clouds from PDB structures and analyzing their topological features across multiple scales, the project uncovers both shared and distinct structural fingerprints that are robust to noise and geometric perturbations.

---

## Background & Motivation

Traditional geometric and statistical tools capture local motifs or global folding patterns of proteins, but often miss higher-order connectivity and multiscale cavities/loops. Persistent homology enables the quantification of such features (connected components, loops, voids) and provides **topological fingerprints** for robust protein comparison.

---

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

---

## File Structure

```bash
DSC214/                        # Main project folder
│
├── 1ATP.pdb                   # Protein structure: Protein Kinase A
├── 1CRK.pdb                   # Protein structure: Creatine Kinase
├── 4hhb.pdb                   # Protein structure: Hemoglobin
│
├── images/                    # All generated images/figures for report
│   ├── ... (plots, diagrams, etc.)
│
├── Project.ipynb              # Main Jupyter notebook for all analysis
├── TDA_statistics.txt         # Summary statistics (loops, persistences, etc.)
├── Wasserstein_distances.txt  # Wasserstein distance results (topological similarity)


## Install Dependencies

```bash
pip install -r requirements.txt
