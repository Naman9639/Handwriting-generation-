# Handwriting-generation-
Generate Handwriting using RNN

About
--------
This model is trained on the [IAM handwriting dataset](http://www.fki.inf.unibe.ch/databases/iam-handwriting-database) and was inspired by the model described by the famous 2014 Alex Graves [paper](https://arxiv.org/abs/1308.0850). It consists of a three-layer recurrent neural network (LSTM cells) with a Gaussian Mixture Density Network (MDN) cap on top. We have also implemented the attention mechanism from the paper which allows the network to 'focus' on character at a time in a sequence as it draws them.

