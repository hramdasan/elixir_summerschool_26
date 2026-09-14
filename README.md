# Introduction to deep learning

Practical notebooks on neural networks, convolutional models, attention and protein transformers. Each notebook contains its own imports, data preparation and model code. There are no shared Python modules.

| Notebook | Contents |
|---|---|
| 0-python-and-notebooks.ipynb | Python and Jupyter basics |
| 1-neural-networks.ipynb | Tensors, gradients, logistic regression and hidden layers |
| 2-training-and-regularization.ipynb | Learning rates, dropout and evaluation |
| 3-convolutional-neural-networks.ipynb | Image filters, synthetic nuclear-image classification, then DNA-motif classification |
| 4-self-attention.ipynb | Embeddings, attention calculations, padding and position |
| 5-transformers.ipynb | Download ESM-2, inspect tokens, mask residues, visualize attention and classify proteins |
| 6-pytorch-lightning-optional.ipynb | Optional Lightning example |

The CNN notebook starts with synthetic microscopy-like images of round and elongated nuclei, including learned feature maps, occlusion-sensitivity overlays and held-out image predictions, then transfers the convolution idea to DNA motifs. The overlays include image, class, patch-size and replacement controls, plus static examples for viewers without widgets. Both exercises run on CPU without a dataset download; their labels describe generated patterns, not experimentally measured biology.

Completed exercises with example outputs and plots are in `answers/`. Open a notebook and run its cells in order with Shift + Enter.

Install the packages in `requirements.txt` and open Jupyter Lab:

```bash
python -m pip install -r requirements.txt
python -m jupyter lab
```

Python 3.12 is recommended. Notebook 6 additionally needs `lightning==2.6.6`.

Notebook 5 downloads the approximately 30 MB ESM-2 weight file and its tokenizer on first use, and reuses them from `model_cache/` afterwards. It runs on CPU or an available CUDA GPU. Attention controls require a notebook frontend with ipywidgets support. A static heatmap and bar chart are also included; their function arguments can be edited if widgets are unavailable.

For Colab, upload an individual notebook. Notebook 5 also needs `data/proteins.csv` uploaded into a `data` folder in the Files panel. The other examples use installed datasets or generate their own data. Uncomment the installation cell in notebook 5 if necessary.

The material is adapted from [CompOmics/intro-to-deep-learning](https://github.com/CompOmics/intro-to-deep-learning). See `LICENSE` and `ATTRIBUTION.md` for attribution and data/model sources.

The student and answer notebooks were executed in fresh Python 3.12 CPU sessions, including the model download and attention controls. Other classroom environments should be checked before use.
