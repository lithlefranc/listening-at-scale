# Listening at Scale

Code for 'Listening at Scale. Word Embeddings as Historical Domain Knowledge for LLM-assisted Annotation in a Large Corpus of Police Records (Antwerp, 1876–1939)', *Computational Humanities Research Conference* 2027.

## Notebooks

Run in order. Figures are written to `fig/`, tables to `tab/`.

| Notebook | Paper |
|---|---|
| `01_corpus_and_embeddings` | §3 corpus statistics; §4.1 Table 2, term frequencies, Figure 4 |
| `02_embedding_robustness` | §4.1 robustness across random seeds |
| `03_clustering` | §4.1 UMAP + HDBSCAN, Figure 3, sensitivity (footnote), Appendix A |
| `04_variant_list` | §4.3 variant list; §5.3 deployment |
| `05_llm_evaluation` | §4.2 annotation counts; §5.1 Table 3 |
| `06_cross_validation` | §5.2 cross-validation, threshold (footnote); §6 coverage by period |
| `07_zero_shot_comparison` | §5.1 zero-shot comparison, Appendix C |

`src/prompts/` holds the two prompts of the zero-shot comparison.

## Data

The data are not included in this repo. The raw data are on Zenodo: https://zenodo.org/records/12805005. For the processed datasets and models, contact Lith.Lefranc@UAntwerpen.be. Place them in `data/`.

## Notes

- Python 3.11: `pip install -r requirements.txt`.
- The LLM runs (`claude-haiku-4-5-20251001`) are not repeated; notebook 07 reads the stored responses (`RUN = False`).
- UMAP results can differ slightly between machines, which may change the exact cluster count.
