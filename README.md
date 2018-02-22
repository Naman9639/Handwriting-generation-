# Handwriting-generation-
Generate Handwriting using RNN

Samples
--------
"turn down the Foot-Griffiths resolution"
![Sample output 1](static/style_0.png?raw=true)
"You know nothing Jon Snow" (print)
![Sample output 2](static/jon_print.png?raw=true)
"You know nothing Jon Snow" (cursive)
![Sample output 3](static/jon_cursive.png?raw=true)

About
--------
This model is trained on the [IAM handwriting dataset](http://www.fki.inf.unibe.ch/databases/iam-handwriting-database) and was inspired by the model described by the famous 2014 Alex Graves [paper](https://arxiv.org/abs/1308.0850). It consists of a three-layer recurrent neural network (LSTM cells) with a Gaussian Mixture Density Network (MDN) cap on top. We have also implemented the attention mechanism from the paper which allows the network to 'focus' on character at a time in a sequence as it draws them.
 
The backbone of the model is three LSTM cells (green). There is a custom attention mechanism (yellow) which digests a one-hot encoding of the sentence we want the model to write. The Mixture Density Network (red) on top choses apropriate Gaussian distributions from which to sample the next pen point, adding some natural randomness to the model. 

![Rolled model](static/model_rolled.png?raw=true)

Unrolling in time, we get
![Unrolled model](static/model_unrolled.png?raw=true)

 

