# Adversarial Training Methods For Semi-Supervised Text Classification

The authors provide a promising way to regularize and improve the generalization of models on various semi-supervised and purely supervised tasks related to NLP.

They add perturbations to the word embeddings by using adversarial training and/or virtual adversarial training.

They show the the word embeddings train with their methods have better nearest neighbors (who shares better semantic meaning) and also perform state of the art on sentiment/topic classification.

They used as datasets a book corpus of 80 million sentences and ArXiv dataset with 5 million sentences.

They show the expectation of 900 features from synthetic sentences which matches well with the feature expectation from the real sentences.

They also show an interesting transition path between two points in the latent space.
