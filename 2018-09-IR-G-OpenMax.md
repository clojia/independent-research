[Home](https://clojia.github.io/) | [Independent Research](https://clojia.github.io/independent_research/) | [Last](https://clojia.github.io/independent_research/2018-09-IR-Look-and-Think-Twice) | [Next](https://clojia.github.io/independent_research/2018-09-IR-Neural-Machine-Translation)

## Index
Z. Ge, S. Demyanov, Z. Chen, and R. Garnavi, “Generative
openmax for multi-class open set classification,” arXiv preprint
arXiv:1707.07418, 2017.

## Motivation
The paper proposed a new model for openset problem, which "extends OpenMax by emoloying generative adversarial networks (GANs) for novel categoriy image synthesis". That is to say, the proposed method uses GANs genrating unknown labels then sends unknown labels to OpenMax as well as labeled ones, thus get an open set image classifier.

## Approach
The method proposed has two stages as well as OpenMax: Pre-Network training and score calibration.
During Pre-Network traning stage, different with openmax, it first generate some unknown class samples (synthetic samples) then sent them along with known samples into networks for training.
<img src="images/pre-network.png" width="500"> 

The generated unknown samples also score calibrations.
<img src="images/score-calibration.png" width="500"> 

The difference is it used K+1 classes instead of K classes in both stages. And the 1 (unknown class) was generated beforehand, whose objective function as:

<img src="images/G-OpenMax-Obj.png" width="500"> 

Being different from normal GANs,

<img src="images/gans_minmax.png" width="500"> 

The function has an extra variable: C, which denotes categories, which will be random selected as well: D(data, category).



## Limitation 
- Assume that the classes from unknown open space will share some common properties with known classes.
- Time/Effort consuming
