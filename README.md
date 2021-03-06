# attention is all we need
a toy implementation of the popular [transformer architecture](https://ai.googleblog.com/2017/08/transformer-novel-neural-network.html).

for each token in a sentence, a transformer modifies its embedding to incorporate embeddings from other tokens (which might contain relevant, discriminating information). as result, modified embedding often contains more information and is therefore more useful for various tasks.

## example
in this [example](https://github.com/mynameisvinn/PieTransformer/blob/master/Transformer.ipynb), we randomly generate 4-token sentences. each token is represented by a 3-dim embedding. finally, for each sentence, the corresponding label is the xor of `embedding1` and `embedding4`. 

because `embedding2` has no correlation with the label, it should have zero predictive value. a neural net learning from (`embedding2`, `label`) should do no better than random chance.

we can increase the predictive value of `embedding2` with a transformer. a transformer "mixes in" other embeddings (eg from `token1` and `token4`, which have predictive value, but also `token3`, which does not) so that the modified `embedding2` contains predictive information. 

training a neural net off (modified `embedding2`, `label`) should do better than random chance.