# MPO624 (University of Miami) triplet-trainer course

This repository contains material to work with the neural network model used in
[L Denby
(2020)](https://agupubs.onlinelibrary.wiley.com/doi/10.1029/2019GL085190) and
was created for class MPO624 at University of Miami Feb 2020.

Exercises are stored as jupyter notebooks in [notebooks/](notebooks/)

## Getting started

Clone this repository so that you have a local copy of the exercises

```bash
git clone https://github.com/leifdenby/MPO624_convml_tt
cd MPO624_convml_tt
```

Download and unpack the [tar-ball with
data](http://homepages.see.leeds.ac.uk/~earlcd/ml-datasets/Nx256_s200000.0_N500study_pretrained.tgz)
we'll be using for the exercises:

```bash
wget http://homepages.see.leeds.ac.uk/~earlcd/ml-datasets/Nx256_s200000.0_N500study_pretrained.tgz
tar zxvf Nx256_s200000.0_N500study_pretrained.tgz
```

The tar-ball contains:

- A trained model (the weights to load the model are stored in
  `train/models/fixednorm-stage-2.pkl`). The model was trained on 10000
  triplets of 200km x 200km image tiles (256x256 pixels) from the tropical
  Atlantic generated from [GOES-16](https://en.wikipedia.org/wiki/GOES-16)
  satellite obserations during the boreal winter Dec 1st 2018 to Feb 28th
   2019. The actual training images are not included here to save space.

- A *study* set of 1000 triplets, stored in `study/`. In practice we will only
  use the *anchor* tile from each study triplet, but are included here because
  tiles used in the *study* set are generated in the same way as the *training*
  set.

- Embedding vectors for the 1000 *anchor* tiles in the *study* set, stored in
  `fixednorm-stage-2.emb.nc` produced with the trained model mentioned above.

[install `convml_tt`](https://github.com/leifdenby/convml_tt#getting-started)
and its dependencies into a conda environment and activate the `convml_tt`
conda environment:

```bash
conda activate convml_tt
```

Open up a jupyter session and get going with the exercises:

```bash
jupyter notebook
```

## Exercises

Tuesday 18th Feb 2020:

1) **Dimensionality reduction**: Examine how the neural
   network has used the embedding space; are all 100 dimensions necessary? Can
   we identify what features the neural network has learnt by comparing tiles
   in different parts of the embedding space? notebook: [1a_Use_PCA_analysis_to_study_tile_embeddings.ipynb](notebooks/1a_Use_PCA_analysis_to_study_tile_embeddings.ipynb)

2) **High-dimensional clustering**: use different
   clustering methods to study the extent to which the neural network has
   formed distinct clusters in the embedding space.
   notebook: [1b_Exploring_embedding_space_with_clustering_methods.ipynb](notebooks/1b_Exploring_embedding_space_with_clustering_methods.ipynb)

Thursday 20th Feb 2020:

3) **Using your own input data**: either by generating synthetic input tiles or
   using your own data source you will work with the pre-trained model to study
   whether the trained neural network groups them together in the embedding
   space. notebook:
   [2_Working_with_your_own_data.ipynb](notebooks/2_Working_with_your_own_data.ipynb)
