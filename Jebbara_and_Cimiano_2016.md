# Aspect-Based Relational Sentiment Analysis Using a Stacked Neural Network Architecture

Propose systems based on neural networks to solve 3 tasks:

- Identification of aspect and opinion terms. They use joint model which takes as input word embeddings, POS.
- Labeling of opinion terms with a sentiment. RNN which uses word embeddings, POS and distance embedding features.
- Extraction of relations between opinion terms and aspects. RNN which uses word embeddings, POS, relative distances to the aspect and relative distances to the opinion term.

Using joint model improves theperformances by 1% for aspect and 5% for opinion terms.

Use SemEval 2015 Task 12 and USAGE dataset.

Not state of the art for 1) (0.659 vs 0.701 for EliXa)