[Home](https://clojia.github.io/) | [Independent Research](https://clojia.github.io/independent_research/) | [Last](https://clojia.github.io/independent_research/2018-09-IR-GloVe) 

## Index
Luong, M.-T., Pham, H., and Manning, C. D. Effective approaches to attention-based neural
machine translation. In Conference on Empirical Methods in Natural Language Processing (2015).

## Motivation
The paper examined two classes of attentional mechanism: global attention model and local attention model in order to better improve neural machine translation (NMT), which is attention-based NMT. 

## Approach

The proposed model is of objective function:

<img src="images/att-obj.png" width="200"> 

Based on LSTM, they introduced a variable-length alignment vector at for two kinds of attentional mechanism:

- The structure for global attention model (based on global context):

<img src="images/global-attention.png" width="300"> 

where the size of alignment vector "equals the number of time steps on the source side":

<img src="images/attention.png" width="250"> 


- The structure of local attention model (based on a window context)

<img src="images/local-attention.png" width="280"> 

where the size of at equals to window size. 

Also, the paper introduced two variants for the local attention model: monotonic alignment (local-m) and predictive alignment (local-p), specifically, the alighments weights of local-p looks like:

<img src="images/att-local-weights.png" width="300"> 


The score of both global and local attention model is "referred as a content-based function":

<img src="images/score.png" width="300"> 

The paper also proposed an input-feeding approach, in order to take past alignment information into account in alignment decisions, and the structure looks like:

<img src="images/input-feeding.png" width="300"> 


## Limitation 
- The paper proved that the alignment function is more powerful in English-German Results. I wonder if English-French or English-Spanish would be the same.
