# Aspect extraction for opinion ming with a deep convolutional neural network

Most of previous works in aspect term extraction have used CRFs or linguistic patterns (LP). CRF is a linear model an so needs a large number of features to work well. Linguistic patterns need to be crafted by hand and they crucially depend on the grammatical accuracy of the sentences.

The author propose a CNN to overcome both limitations. In addition, they use also LP. They use a special training algorithm suitable for sequential data.

Use two datasets : SemEval 2014 and Qiu et al 2011.

As feature they use special WE trained on Amazon reviews, LP and also POS. LP help the CNN to have a better recall.

Two potential reasons to be state of the art are : 1) Using a non-linear classifier 2) Use special pre-trained word embedding (3 also LP and POS).

