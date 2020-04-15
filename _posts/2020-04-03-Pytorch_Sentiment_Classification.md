---
layout: post
title: Sentiment Classification using Pytorch
tags: [personal project, NLP]
image: /img/facial/firstCNNlayerFeatureMap.png
---
# Face-Landmark-Extraction-Pytorch
### Trained with NVIDIA P100 GPU

### NLP_Sentiment_Classification

* A review and its label whether the review is Positive or Negative


* In the review.txt the ratio of Positive and Negative words is following:
![Positive Negative Ratio](/img/sentiment/pos_neg_ratio.png)

* A trainig performance using these raw data is:
![Before Reduce Noise](/img/sentiment/b4_reduce.png)

* Looks like I am doing a redundant calculation when I udpate weights in a hidden layer. After I optimized this problem:
![First Noise Reduction](/img/sentiment/first_reduction.png)

* Still, the performance is not quite enough :confused:, Let's look at the distribution of words:
<img src="/img/sentiment/bokeh_plot_pos_neg_dist.png" width="350"/> 

* It looks like, there are too many vauge menaning words(which are close to the zero, or the middle values), let's trim them out.
After the trimming, the performance is:
![Last Noise Reduction](/img/sentiment/final_reduction.png)

* :stuck_out_tongue: The performance is boosted **from 200 to 6000**.

* After the training, let's look at the weights in the hidden layer. 
* Using the weights, we can find the similar meaning words!


<img src="/img/sentiment/similar_excellent.png" width="350"/> <img src="/img/sentiment/similar_terrible.png" width="350"/> 


* Let's take a loot its T-SNE.

<img src="/img/sentiment/T-SNE_most_polarized.png" width="450"/> 



* Okay, then what about the positive and negative words?


<img src="/img/sentiment/T-SNE_pos.png" width="350"/> <img src="/img/sentiment/T-SNE_neg.png" width="350"/> 

### Github
- [Link](https://github.com/JaeLee18/NLP_Sentiment_Classification)
