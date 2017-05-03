# Odin: Contextual Document Opinions On The Go

Uses opinionated aspects to help users navigate through a collection of articles. Aspects are ranked according to their importance and so are the articles dicussing them

Odin users can quickly find opinions and documents that are Aligned or Divergent from the corpus' consensus or those that are the most Relevant given the overall corpus' of opinions. It is not a summarization tool.

The goal is to find the "best documents" which matches a time constraint.

Methodology:

- Extract Content
- Identify Discussion Subjects. Removed all words which are not nouns, then these are lemmatized and feed withint LDA (**I don't think this is a good idea because unsupervised model need to have the whole context**). After the LDA steps, they compute a rank for each word that is topic independent which gives a weight for how important or central each subject is in the corpus (only consisdered top 500 words).
- Detect Opinion Sentiment. Consider each sentences tonainting one subjects in them. They use the dependency tree and uncover the modifiers that were applied to any subject (and any negations). Compute the set of opinions acress every sentence of every document where the subject occurs.
- Calculate Corpus' Opinions. Compute mean pos and mean neg for the corpus by using the whole set of documents.
- Instance Alignment and Divergence. Alignment should gros as distance from the corpus'opinion shrinks while Divergence should shrink. Both Alignment and Divergence grow as importance of the subject increases.
- Sentence Alignment, Divergence and Relevance.
