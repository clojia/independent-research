[Home](https://clojia.github.io/) | [Research](https://clojia.github.io/research/) | [Last](https://clojia.github.io/research/2018-08-IR-DL) | [Next](https://clojia.github.io/research/2018-08-IR-LIME)

## Index

Hassen, M., Chan, P.K.: Learning a neural-network-based representation for open set recognition. arXiv preprint arXiv:1802.04365 (2018)

## Motivation

Open set recognition problems exist in many domains such as identify malwares. It is normally difficult to build a classifier to identify those "unknowns" based on "unknown" labels. This paper uses malware identification as example, introduced a loss function for neural network to handle these "unknown unknowns".

## Approach

ii-loss function was propsed in order to maximize the distance between different classes (inter class separation) and minimize distance of an instance from its class mean (intra class spread). 

99% outlier score value was used as the outlier threshold (global) in the experiment.

The data was trained on n class labels while tested on (n+1) class labels (1 for unknown class), ii-loss function was implemented with convolution network, fully connected network and combined with cross entropy loss, evaluated on MNIST, Microsoft Malware Challenge Dataset and Android Genome Project Dataset. Results were compared under conditions of FPR below 100% and below 10%. In general, ii-loss function and its combination with cross entropy loss have achieved better performance than using cross entropy loss only in identify unknown classes.

## Limitation 

- Fancier outlier threshold could be designed

## Ideas
- For the case combining ii-loss with cross entropy loss, we may try using minimize intra distance rather than maximize the distance differences for cross entropy is sort of maximize classes distance, there may be no need to do it twice. 
