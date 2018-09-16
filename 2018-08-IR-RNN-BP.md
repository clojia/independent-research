[Home](https://clojia.github.io/) | [Research](https://clojia.github.io/research/) | [Last](https://clojia.github.io/research/2018-08-IR-Open-Max) | [Next](https://clojia.github.io/research/2018-08-IR-Dist-Rep)

## Index

G. Chen, “A gentle tutorial of recurrent neural network with error backpropagation,” arXiv
preprint arXiv:1610.02583, 2016

## Motivation
Focus on basics of backpropagation in recurrent nerual networks (RNN) and long short-term memory (LSTM).

## Approach
- RNN

The paper introduced the objective function of RNN:

<img src="../images/rnn_objf.png" width="200">

Also three different types of parameters/weights: input layer to hidden layer (Wxh), hidden layer to output layer (Whz) and hidden layer between time sequences (Whh). Based on chain rule and total derivatives, using backpropagation to compute their derivatives:

Whz:

<img src="../images/rnn_hz.png" width="200">

Whh:

<img src="../images/rnn_hh.png" width="400">

Wxh:

<img src="../images/rnn_xh.png" width="400">


- LSTM

Based on RNN, the paper explained the structure of LSTM - including four gates: input modulation gate, input gate, forget gate and output gate along with their corresponding weights: 

  Gate | Xt | ht-1
  ----- | ---- |-----
  Input Modulation Gate | Wxc | Whc
  Input Gate | Wxi | Whi
  Forget Gate | Wxf | Whf
  Output Gate | Wxo | Who
  

Also introduces the memory information (cell) and be able to handle long sequential better. 

Using backpropagation, the derivatives of weights respect to X look like:

<img src="../images/lstm_wx.png" width="300">

the derivatives of weights respect to ht-1 look like:

<img src="../images/lstm_wh.png" width="300">

