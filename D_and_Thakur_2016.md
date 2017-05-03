# Aspect-based Sentiment Summarization with Deep Neural Networks

This paper proposes an elegant solution for ASBA for the challenge SemEval 2014. They are able to extract multi-aspects (not like Gu_et_al_2017) per sentences and classify the polarity of each of them.

They also claim that LDA (such methods) doesn't work well for specific prodouts.

Two ways to tackle the problem:

- Making aspects and sentiments independent (2 classifiers)
- Aspect and its sentiment are modelled as pairs


They propose a model decomposed in two steps:

- 1 first RNN tag each word to an aspect. If a sentence express multiple aspects, they analyse the constituency parse tree and separate each aspect from the sentence (producing sub-sentences).
- 1 CNN which determines the sentiment polarity of the (sub-)sentence.

Finally, they perform "only" 76 as F1-Score compared to 83 for the best.
