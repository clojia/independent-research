[Home](https://clojia.github.io/) | [Independent Research](https://clojia.github.io/independent_research/) | [Last](https://clojia.github.io/independent_research/2018-09-IR-Look-and-Think-Twice)

## Index
C. Cao, X. Liu, Y. Yang, Y. Yu, J. Wang, Z. Wang, Y. Huang,
L. Wang, C. Huang, W. Xu, et al. Look and think twice: Capturing
top-down visual attention with feedback convolutional
neural networks. In ICCV, 2015.

## Motivation
The proposed network archtecture is to develop a "develop a computational feedback mechanism" which can help "better visualized and understand how deep neural network work, and capture visual attention on expected objects, even in images with cluttered background and multiple objects". 
 
## Approach
A normal CNN archtecture includes:
- Convolutional Layer
<img src="images/conv.png" width="200"> 

- ReLU Layer
<img src="images/Relu.png" width="130"> 

- Max-Pooling Layer
<img src="images/maxPooling.png" width="300"> 

The work introduced a binary activation variable Z(0,1) instead of max() operation in ReLU layer and Max-Pooling layer, reinterpreting ReLU and Max-Pooling as

<img src="images/re-inter-relu.png" width="70"> 

<img src="images/re-inter-max.png" width="70"> 

The paper also introduced a feedback model and its inference process. The feedback layer is stacked upon each ReLU layer, which looks like

<img src="images/feedback.png" width="700"> 

And the hidden neurons in feedback loops would be updated as 

<img src="images/discrete_feedback.png" width="700"> 

Since this leads to an integer programming problem

## Limitation 

The feedback loops cannot prevent that two class share the same attention format.



