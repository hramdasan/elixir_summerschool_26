# Attribution and licenses

## Teaching material

Adapted from [CompOmics/intro-to-deep-learning](https://github.com/CompOmics/intro-to-deep-learning), accessed 13 September 2026, commit `3941186443b804e596317725807deb7e6139366e`. The repository's Creative Commons Attribution 4.0 International license is reproduced in `LICENSE`.

The rewrite changes the explanations, exercises, workflow and code; replaces the recurrent-model practical; adds attention, protein-transformer and preparatory notebooks; and supplies separate instructor solutions. Attribution to CompOmics does not imply their endorsement of this adaptation. Adapted teaching material is distributed under the same CC BY 4.0 terms. Preserve attribution and identify further changes when redistributing.

## Breast-cancer dataset

Wisconsin Diagnostic Breast Cancer dataset, distributed with scikit-learn, originally provided by the University of Wisconsin and available through the [UCI dataset record](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic). See [scikit-learn's loader documentation](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_breast_cancer.html) for feature descriptions and source references. This package does not redistribute the raw dataset separately; notebooks load the copy included with the installed library. Labels are explicitly remapped to 1 = malignant.

## Protein data

Protein sequences and location annotations are a small snapshot from [UniProtKB](https://www.uniprot.org/), downloaded through the [REST API](https://rest.uniprot.org/) on 13 September 2026. UniProt data are available under [CC BY 4.0](https://www.uniprot.org/help/license). The bundled data retain accessions and annotations; queries and processing are recorded in `data/provenance.json`. Cite UniProt when using or extending the dataset.

## Model and embeddings

The transformer notebook downloads and runs Meta's [facebook/esm2_t6_8M_UR50D](https://huggingface.co/facebook/esm2_t6_8M_UR50D), revision `c731040fcd8d73dceaa04b0a8e6329b345b0f5df`, whose model card specifies the MIT license. Model weights are not included in the teaching archive. See [the ESM repository](https://github.com/facebookresearch/esm) and Lin et al., *Evolutionary-scale prediction of atomic-level protein structure with a language model*, Science (2023), for the model's research context. Representations and attention weights are computed during notebook execution.

## Synthetic examples and software

Notebook 03's DNA strings and image are synthetic teaching examples, not experimental data. Notebook 04's hand-written attention values and randomly initialized transformer are not biological models. Third-party packages retain their own licenses; requirements files do not relicense them.
