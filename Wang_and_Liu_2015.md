# Deep Learning for Aspect-Based Sentiment Analysis

The author apply deep learning for ABSA on SemEval 2015 (competitive or best results).
Previous work used SVM, or CRF classifiers.

Because the distribution of the aspects is heavy-tail (80% among the 16 first over 254 in total), they keep only the 16 most used and classify all the others as "OTHER".

They use a simple feed-forward NN to compute the aspect distribution (while a linear model would have been sufficiant).

For the sentiment, they use a CNN.

Predicting sentiment of a sentence is easy. However, when a sentence express several sentiments, much harder !

Insights: Magnifitude of word vectors has a strong influcence on the behavior of the CNN. So we can rescale each word vector according to its relatedness to the given aspect efore senting it into the CNN.

When predicting the top-aspects for a sentence, keep all aspect values > theta, which is a parameter.

Better than the winner of SemEval 2015 for Slot 1 (finding aspects and entities). Second highest accuracy for Slot 3 (sentiment polarity). On the task 2 (out-of-domain ABSA), ends up third.
