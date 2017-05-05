# UWB: Machine Learning Approach to Aspect-Based Sentiment Analysis

Participation in SemEval 2014 ABSA. Each participant coud submit two versions : constrained and unconstrained (without (but with lexicons for example) and with additional data).

4 Tasks :

- Aspect term extraction
- Aspect term polarity
- Aspect category detection
- Aspect category polarity

For 1), they used CRF. For the others, Maximum Entropy classifier.

Features : words, BoW, bigrams, BoB, tf-idf, Learned Dictionary, Suffixes, Sentiment Dictionary, Senti Wordnet, LDA, Word Clusters, BoC.

LDA and Word Clusters were runned of restaurant reviews containing 409k reviews.
Topic probabilities are directly used as new features to the classifier.
For Word Clusters, they keep the word vectors clustered into four different depths.

## Aspect term extraction

CRF (linear model) and BIO model for representating aspect terms.

## Aspect term polarity

Use context window of 10 words in both directions around the target aspect term. Weight each word and bigram taken from the Gaussian distribution according to the distance from the aspect term.

## Aspect Category Detection

n classifiers. Final decision simply assembled from decisions of individual classifiers.

## Aspect category polarity

3 classifiers for each polarity.



So so final performances.