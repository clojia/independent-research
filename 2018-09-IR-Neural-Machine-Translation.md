[Home](https://clojia.github.io/) | [Independent Research](https://clojia.github.io/independent_research/) | [Last](https://clojia.github.io/independent_research/2018-09-IR-G-OpenMax) | [Next]()

## Index
 D. Bahdanau, K. Cho, and Y. Bengio. Neural machine translation by jointly learning to align and translate.
arXiv preprint arXiv:1409.0473, 2014.

## Motivation
The paper proposed a new architecture for machine translation model. Specifically, it added an alignment model to basic RNN Encoder-Decoder. 

## Approach
Just like traditional machine translation model, the proposed architecture consists of an encoder and a decoder. The encoder is a bidirectional RNN: 

<img src="images/translation_encoder.png" width="200"> 

And the decoder "emulates searching through a source sentece during decoding a translation", which consits of three networks: g(), f() and a():

output:
<img src="images/translation_g.png" width="300"> 

hidden states:
<img src="images/translation_f.png" width="150"> 

attentions:
<img src="images/translation_a.png" width="150"> 


The architecture of proposed neural machine translation model looks like 

<img src="images/translation-attention.png" width="300"> 

The attention weights are based on both input/output position and the values.
