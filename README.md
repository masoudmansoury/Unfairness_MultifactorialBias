# **The Unfairness of Multifactorial Bias in Recommendation**    
This repository contains the code and datasets for the paper "**The Unfairness of Multifactorial Bias in Recommendation**". In particular, the code relates to the simulation study conducted in the paper. For the rest of analysis, follow the steps below.

## Datasets

Four datasets used in the paper are available in the folder `./datasets`. 

## Percentile transformation

For tranforming the rating data into percentile values, we used the code in this repository: https://github.com/masoudmansoury/percentile.

## Recommendation tool

For running experiments with recommendation models, we used [Librec-Auto](https://github.com/that-recsys-lab/librec-auto).

## Additional results

In this part, we present our additional results not reported in the paper.

**Results on an unbiased dataset**

We additionally performed experiments on Yahoo!R3 dataset which contains an unbiased test set. In this dataset, the training data contains 15,400 users who provided 311,704 ratings on 1,000 items (density of 0.02).

The following plots show the popularity (left) and ratings (right) distribution of Yahoo!R3 dataset.

<img src="https://github.com/masoudmansoury/Unfairness_MultifactorialBias/blob/main/results/longtail_dist.jpg" width="400"/> <img src="https://github.com/masoudmansoury/Unfairness_MultifactorialBias/blob/main/results/rating_dist.jpg" width="400"/>