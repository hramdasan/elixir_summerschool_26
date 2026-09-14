# Protein data

`proteins.csv` contains 120 reviewed UniProt entries from E. coli K-12: 60 annotated as cytoplasmic (label 0) and 60 as membrane-associated (label 1). Only sequence-derived features enter the models. Names and annotation text are retained for inspection, not used as predictors.

Sequences contain the standard 20 amino acids and have lengths 50–300. The two location queries exclude one another. Labels reflect database annotations with varying evidence; “membrane” does not mean exclusively integral transmembrane proteins.

Exact query filters, sampling and model revision are in `provenance.json`. Exact duplicate sequences were excluded. Local alignments used BLOSUM62, gap opening -10 and extension -0.5. Pairs with at least 30% identity among aligned residue pairs and at least 80% paired-residue coverage of each sequence were connected into groups. `similarity_pairs.csv` lists the detected pairs. Groups were split into 72 training, 24 validation and 24 test examples, balanced within each partition.

This grouping reduces detected sequence overlap but does not comprehensively separate remote homologues. ESM-2 pretraining may include these proteins or relatives. This small annotation-derived selection is a teaching dataset, not a representative benchmark.

No precomputed model outputs are included. Notebook 5 downloads the model and calculates embeddings and attention weights. Data were retrieved from UniProt on 13 September 2026; attribution and licensing are in `../ATTRIBUTION.md`.
