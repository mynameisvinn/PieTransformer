# attention is all we need
a toy implementation of the popular [transformer architecture](https://ai.googleblog.com/2017/08/transformer-novel-neural-network.html).

for a given token in a sentence, a transformer modifies a given token's embedding so that it incorporates embeddings from other tokens (which might have high predictive value). as result, this modified embedding is often much more useful than the original embedding.