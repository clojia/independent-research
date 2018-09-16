[Home](https://clojia.github.io/) | [Research](https://clojia.github.io/research/) | [Last](https://clojia.github.io/research/2018-08-IR-LIME)

## Index

A. Bendale and T. E. Boult. Towards open set deep networks.
In CVPR, 2016. 

[github](https://github.com/abhijitbendale/OSDN)

## Motivation

While deep networks have produced significant gains in computer vision field, it is easily fooled with images humans do not consider meaningful. i.e. It is normally difficult to recognize "unknown" aka. open set problem. This paper introduced a approach - OpenMax, which combined softmax layer with meta-recognition algorithm to identify those "unknown unknowns".

## Approach
OpenMax adapted EVT meta-recognition calibration in the penulimite layer of deep neural networks. For each instance, activation vector is revised to the sum of the product of its distance to the mean activation vectors (MAV) of each class. Then sent to softmax layer.

The experiment is based on ImageNet Large Scale Visual Recognition Competition 2012 dataset with 1000 visual categories to identify fooling images. The distance in this experiment is a weighted combination of nomralized Euclidean and coisine distance. The performances were measured by F-score (as it is not inflated by true negatives), and the results show that OpenMax consistently obtains higher F-measure on open set testing.

## Future
The experessiveness of the AV model could be increased aiming to better capture different contexts for the same object.
