# SENSE CDT (University of Leeds) triplet-trainer course

This repository contains material to work with the neural network model used in
[L Denby
(2020)](https://agupubs.onlinelibrary.wiley.com/doi/10.1029/2019GL085190)
and was created for SENSE CDT training at University of Leeds on 23rd
March 2022 (if you're looking for the 2021 training material [look
here](https://github.com/leifdenby/SENSE_convml_tt/tree/3167552a729d79af37f1c119fbe1753ee5445589)).

Exercises are stored as jupyter notebooks in [notebooks/](notebooks/)

## Getting started

To work through the exercises you will need two things:

1) A copy of the exercises (the repository you're looking at right now!)

2) A copy of the `convml-tt` python module installed into a conda
environment

If you are on Windows and are having trouble some more detailed notes are
given [here](README.windows.md).

### 1. Downloading the exercises

Choose a suitable parent directory (for example your desktop, `~/Desktop`)
and clone this repository so that you have a local copy of the exercises

```bash
git clone https://github.com/leifdenby/SENSE_convml_tt
cd SENSE_convml_tt
```

In the execises you will work with a dataset and trained model that comes
bundled with `convml-tt` and instructions for how to download these is
contained within the exercises.

### 2. Install `convml-tt` and its dependencies with `conda`

Instructions on how to create a conda environment and install `convml-tt`
into it are
[here](https://github.com/leifdenby/convml_tt#getting-started)). But it
essentially boils down to three steps: 1) install
[conda](https://docs.conda.io/en/latest/miniconda.html), 2) install
[pytorch](https://pytorch.org/get-started/locally/) using conda for GPU or CPU
use (depending on whether you have a GPU) and 3) install `convml-tt` with `pip.`

## Exercises

Once `convml-tt` is installed you can activate the `convml-tt` conda
environment:

```bash
conda activate convml-tt
```

Move to the path where you checked out the exercises (e.g.
`~/Desktop/SENSE_convml_tt`)

And start up a jupyter session and get going with the exercises:

```bash
jupyter notebook
```

The exercises are broken down as follows:

1130 - 1230:

1) **Dimensionality reduction**: Examine how the neural
   network has used the embedding space; are all 100 dimensions necessary? Can
   we identify what features the neural network has learnt by comparing tiles
   in different parts of the embedding space? notebook: [1a_Use_PCA_analysis_to_study_tile_embeddings.ipynb](notebooks/1a_Use_PCA_analysis_to_study_tile_embeddings.ipynb)

2) **High-dimensional clustering**: use different
   clustering methods to study the extent to which the neural network has
   formed distinct clusters in the embedding space.
   notebook: [1b_Exploring_embedding_space_with_clustering_methods.ipynb](notebooks/1b_Exploring_embedding_space_with_clustering_methods.ipynb)

1330 - 1500:

3) **Using your own input data**: either by generating synthetic input tiles or
   using your own data source you will work with the pre-trained model to study
   whether the trained neural network groups them together in the embedding
   space. notebook:
   [2_Working_with_your_own_data.ipynb](notebooks/2_Working_with_your_own_data.ipynb)
