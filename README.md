# attention is all we need
a toy implementation of the popular [transformer architecture](https://ai.googleblog.com/2017/08/transformer-novel-neural-network.html).

for a given token in a sentence, a transformer modifies that token's embedding in such a way to incorporate the embeddings of other tokens that have high predictive value. this modified embedding is often much more useful than the original embedding.