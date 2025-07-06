# One4All

Let's try and create our own, **TRUE** Multimodal Embedding model.

This will not be an easy challenge, but one we need to undertake, for the good of the community.

## But How Tho?
It is not that complicated, on a high level, we take advantage of existing architectures such as **sentence-transformers/clip-ViT-B-16**, which, as the ViT suggests is a Vision Transformer. 

The idea is to continue training the pre-trained model on audio input, which will be converted into a mel-spectogram, which can be tought of as a visual representation of the waveform, with axis $X$ corresponding to the time and axis $Y$ attending to the real sound information.

This would be implemented by feeding into the model either pairs/triplets of data of various formats, such as Audio/Text or Audio/Image, etc... and then calculate standard losses such as InfoNCE or Contrastive Loss.

At first, the model has no idea about what those spectorgrams represent, therefore we have to continue pre-training the model before feeding him these pairs and improve his embedding capabilities.

The continuous pre-training step would be executed with 


## Challenges
Two main challenges come immediately to mind:

1. Where do find enough data in order to train the model?