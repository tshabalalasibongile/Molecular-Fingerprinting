# Molecular Fingerprinting
**Author:** Sibongile Tshabalala (2356121)

## Overview
This project demonstrates molecular fingerprinting and similarity analysis of statins using RDKit and PubChemPy. The workflow generates Morgan, RDKit Atom-Pair, and MACCS keys fingerprints, computes pairwise Tanimoto similarities, performs hierarchical clustering, and visualizes relationships via heatmaps and MDS plots.

## Tools & Libraries
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- RDKit, PubChemPy
- Scikit-learn (MDS)
- SciPy (linkage, dendrogram)

## Project Tasks
### 1. Import Libraries
- Loaded RDKit, PubChemPy, Pandas, NumPy, Seaborn, Matplotlib.
- Suppressed warnings for clean output.

### 2. Define SMILES and Molecules
- Defined SMILES strings for Simvastatin, Pravastatin, Atorvastatin, Fluvastatin.
- Created RDKit molecule objects.

### 3. Generate Fingerprints
- Morgan (ECFP4), RDKit Atom-Pair, and MACCS keys fingerprints were generated.
- Fingerprints encode structural and functional features of molecules.

### 4. Pairwise Similarity & Distance Matrices
- Computed Tanimoto similarity matrices for all fingerprints.
- Converted similarities to distances (1 - similarity) for clustering.

### 5. Heatmap Visualization
- Visualized similarity matrices using annotated heatmaps.
- Identified high, moderate, and low similarity relationships.

### 6. Hierarchical Clustering
- Generated dendrograms based on Morgan fingerprint distances.
- Confirmed two major structural groups: Simvastatin–Pravastatin (natural) and Atorvastatin–Fluvastatin (synthetic).

### 7. MDS 2D Projection
- Used multidimensional scaling (MDS) for 2D visualization.
- Reinforced clustering and similarity trends visually.

### 8. Summary of Findings
- **High similarity:** Simvastatin & Pravastatin (~0.85–0.90)
- **Moderate similarity:** Atorvastatin & Fluvastatin (~0.50–0.55)
- **Low similarity:** Natural vs synthetic statins (~0.25–0.35)
- Structural relationships align with pharmacological groupings.

## Challenges & Improvements
- Validating SMILES strings to avoid null molecules.
- Selecting optimal fingerprint methods for structural features.
- Potential improvements:
  - Extended dataset with more statins.
  - 3D conformer-based analysis.
  - Alternative similarity metrics (cosine, Dice).
  - Enhanced visualization (clustered heatmaps, 3D MDS).

## Conclusion
Molecular fingerprinting effectively reveals structural relationships among statins. Similarity matrices, clustering, and MDS confirm chemical groupings consistent with pharmacology, demonstrating a reproducible and interpretable computational workflow for drug similarity analysis.

