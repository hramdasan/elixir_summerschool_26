# Introduction to deep learning

Practical notebooks on neural networks, convolutional models, attention and protein transformers. Each notebook contains its own imports, data preparation and model code. There are no shared Python modules.

| Notebook | Contents | Student notebook | Answers |
|---|---|---|---|
| 0-python-and-notebooks.ipynb | Python and Jupyter basics | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hramdasan/elixir_summerschool_26/blob/main/notebooks/0-python-and-notebooks.ipynb) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hramdasan/elixir_summerschool_26/blob/main/answers/0-python-and-notebooks.ipynb) |
| 1-neural-networks.ipynb | Tensors, gradients, logistic regression and hidden layers | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hramdasan/elixir_summerschool_26/blob/main/notebooks/1-neural-networks.ipynb) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hramdasan/elixir_summerschool_26/blob/main/answers/1-neural-networks.ipynb) |
| 2-training-and-regularization.ipynb | Learning rates, dropout and evaluation | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hramdasan/elixir_summerschool_26/blob/main/notebooks/2-training-and-regularization.ipynb) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hramdasan/elixir_summerschool_26/blob/main/answers/2-training-and-regularization.ipynb) |
| 3-convolutional-neural-networks.ipynb | Image filters, synthetic nuclear-image classification, then DNA-motif classification | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hramdasan/elixir_summerschool_26/blob/main/notebooks/3-convolutional-neural-networks.ipynb) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hramdasan/elixir_summerschool_26/blob/main/answers/3-convolutional-neural-networks.ipynb) |
| 4-self-attention.ipynb | Embeddings, attention calculations, padding and position | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hramdasan/elixir_summerschool_26/blob/main/notebooks/4-self-attention.ipynb) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hramdasan/elixir_summerschool_26/blob/main/answers/4-self-attention.ipynb) |
| 5-transformers.ipynb | Download ESM-2, inspect tokens, mask residues, visualize attention and classify proteins | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hramdasan/elixir_summerschool_26/blob/main/notebooks/5-transformers.ipynb) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hramdasan/elixir_summerschool_26/blob/main/answers/5-transformers.ipynb) |
| 6-pytorch-lightning-optional.ipynb | Optional Lightning example | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hramdasan/elixir_summerschool_26/blob/main/notebooks/6-pytorch-lightning-optional.ipynb) | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/hramdasan/elixir_summerschool_26/blob/main/answers/6-pytorch-lightning-optional.ipynb) |

The CNN notebook starts with synthetic microscopy-like images of round and elongated nuclei, including learned feature maps, occlusion-sensitivity overlays and held-out image predictions, then transfers the convolution idea to DNA motifs. The overlays include image, class, patch-size and replacement controls, plus static examples for viewers without widgets. Both exercises run on CPU without a dataset download; their labels describe generated patterns, not experimentally measured biology.

Completed exercises with example outputs and plots are in `answers/`. Open a notebook and run its cells in order with Shift + Enter.

## Run in Colab

1. Click **Open in Colab** in the student column above. Each notebook also has its own launch button at the top; the answers column opens the completed version.
2. Choose **File → Save a copy in Drive** to keep your work.
3. Run the **Colab setup** cell first, then work through the notebook from top to bottom with **Shift + Enter**. If installation requests a session restart, restart and run from the setup cell again.

A standard CPU runtime is sufficient for these exercises. The setup cells install each notebook's required packages, including Transformers for notebook 5 and Lightning for notebook 6. Notebooks 3 and 5 also enable Colab's widget manager for the overlays and attention controls; static plots remain available.

Notebook 5 downloads its model weights and fetches `data/proteins.csv` from a fixed revision of this repository when no local copy exists. You do not need to upload files or mount Google Drive. Colab's runtime files are temporary; a new runtime may need to download them again.

## Run locally

Install the packages in `requirements.txt` and open Jupyter Lab:

```bash
python -m pip install -r requirements.txt
python -m jupyter lab
```

Python 3.12 is recommended. Notebook 6 additionally needs `lightning==2.6.6`.

Notebook 5 downloads the approximately 30 MB ESM-2 weight file and its tokenizer on first use, and reuses them from `model_cache/` afterwards. It runs on CPU or an available CUDA GPU. Attention controls require a notebook frontend with ipywidgets support. A static heatmap and bar chart are also included; their function arguments can be edited if widgets are unavailable.

The material is adapted from [CompOmics/intro-to-deep-learning](https://github.com/CompOmics/intro-to-deep-learning). See `LICENSE` and `ATTRIBUTION.md` for attribution and data/model sources.

The student and answer notebooks were executed in fresh Python 3.12 CPU sessions, including the model download and attention controls. Other classroom environments should be checked before use.
