# Mining Opinion Features in Customer Reviews

This paper aims to summarize all the customer reviews of a product, especially mining opinion/product features that the reviewers have commented on.

The feature-based opinion summarization of customer reviews is split into 2 tasks :

- Identifying features of the product that customers have expressed opinons on and rank these according to their frequencies that they appear in the reviews
- For each feature, identify how many customer reviews have positive or negative opinions.

To accomplish such tasks, you can use two basic techniques: noun phrases (produces too many non-terms) and statistical approaches (reoccuring phrases misses many low frequency terms).
They propose an association mining based technique which doesn't have these problems.

In addition, they work doesn't need a training corpus to build a summary. However, they focus only on finding that features which appear explicitly as nouns or noun phrases.