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

Similar to figures 1 and 2 in the paper, the following plots show the popularity (left) and ratings (right) distribution on Yahoo!R3 dataset.

<img src="https://github.com/masoudmansoury/Unfairness_MultifactorialBias/blob/main/results/yahooR3/longtail_dist.jpg" width="300"/> <img src="https://github.com/masoudmansoury/Unfairness_MultifactorialBias/blob/main/results/yahooR3/rating_dist.jpg" width="300"/>

While popularity bias is evident in these plots, positivity bias seems less problematic as the distribution is not highly skewed. Unlike four datasets reported in the paper that the rating values were skewed toward the hih rating values, the rating distribution in Yahoo!R3 exhibit even skewness toward the low rating values. We also examined these distributions in Coat dataset (another unbiased dataset), while not reported here, and observed similar patterns.

To understand the degree of multifactorial bias on this dataset, similar to figures 3 and 6 in the paper, the following plots present the relationship between items' popularity and average rating on the original rating values (left) and the transformed percentile values (right).

<img src="https://github.com/masoudmansoury/Unfairness_MultifactorialBias/blob/main/results/yahooR3/yahoounbiased_pop_rating.jpg" width="300"/> <img src="https://github.com/masoudmansoury/Unfairness_MultifactorialBias/blob/main/results/yahooR3/yahoounbiased_pop_percentile.jpg" width="300"/>

First, the left plot, the relationship between average rating and popularity of items in original rating values, does not exhibit a high degree of multifactorial bias in Yahoo!R3. Hence, as shown in right plot (the relationship between average rating and popularity of items in percentile values), applying the proposed percentile transformation method makes the distribution skewed toward low rating values which is not desirable.

The following plots show the performance of six recommendation models trained with original rating values and percentile values. The performance are evaluated with respect to various item-side and user-side metrics as well as accuracy metrics.

<img src="https://github.com/masoudmansoury/Unfairness_MultifactorialBias/blob/main/results/yahooR3/yahoounbiased_per_biasedmf.jpg" width="200"/> <img src="https://github.com/masoudmansoury/Unfairness_MultifactorialBias/blob/main/results/yahooR3/yahoounbiased_per_listrankmf.jpg" width="200"/> <img src="https://github.com/masoudmansoury/Unfairness_MultifactorialBias/blob/main/results/yahooR3/yahoounbiased_per_svdpp.jpg" width="200"/> <img src="https://github.com/masoudmansoury/Unfairness_MultifactorialBias/blob/main/results/yahooR3/yahoounbiased_per_wrmf.jpg" width="200"/> <img src="https://github.com/masoudmansoury/Unfairness_MultifactorialBias/blob/main/results/yahooR3/yahoounbiased_per_userknn.jpg" width="200"/> <img src="https://github.com/masoudmansoury/Unfairness_MultifactorialBias/blob/main/results/yahooR3/yahoounbiased_per_itemknn.jpg" width="200"/>

