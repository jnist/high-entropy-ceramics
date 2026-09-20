# HEC figure reproduction

Reproduce paper figures from the released High-Entropy Ceramics package.

## Setup

```bash
python -m pip install -r requirements.txt
```

## Run

Open `reproduce_figures.ipynb` in Jupyter / VS Code and run all cells, or:

```bash
jupyter nbconvert --to notebook --execute reproduce_figures.ipynb --inplace
```

## Outputs

Figures are written to `outputs/`:

| File | Description |
|------|-------------|
| `pie_chart_anions_structure.png` | Anion and crystal-structure distributions |
| `O.png` | Element frequency in high-entropy oxides |
| `figure_distance_histogram.png` | Embedding-centroid dissimilarity distance histogram |
| `figure_tsne_outlier_142.png` | t-SNE map highlighting Ge as the top A-site outlier |
| `rdf_wasserstein_normalized_panel_c.png` | Normalized RDF distortion by structure prototype |

## Data

| Path | Role |
|------|------|
| `../Frontend/data/hec-dataset-v1.0.csv` | Curated composition database (717 entries) |
| `data/distance.csv` | Precomputed most-dissimilar element distances for equimolar compositions |
| `data/element-vectors.csv` | Element embedding vectors used for the t-SNE panel |
| `data/rdf-wasserstein-normalized.csv` | Precomputed RDF Wasserstein distortion metrics for relaxed supercells |

The distance, element-vector, and RDF files are released analysis intermediates required to regenerate the paper figures without re-running the full embedding or structure-relaxation stacks.
