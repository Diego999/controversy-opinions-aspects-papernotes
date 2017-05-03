# An Unsupervised Aspect-Sentiment Model for Online Reviews

They present an unsupervised system for extracting aspects and determining sentiment in review text. Why such methods is preferrable in this context ?

- Due to the wide range and variety of products and services being reviewd, the framework must be robust and easily transferable between domains.
- Online reviews are often short and unstructured, and my contain many spelling and grammatical errors. Unsupervised methods are not influenced by lexical form and can handle unknown words, provided they occur frequently enough.

They have interestings data with restaurant reviews and amazon netbook reviews (four laptopts) where some are manually annotated.

There are six manually defined aspect labels. They used only sentences with ONE label.


Methodology:

- Local LDA (without any special tuning of LDA) where each sentence represents a document.
- Definition of the number of topics for the previous point
- Determining representative words with a score based on their mutual information with regard to that aspect. They select for each aspect the top k ranking words, such that they cover 75% of the word instances labeled by LDA.
- Inferred Aspects. The system identifies important aspects relevant to our data (in addition to the manually defined ones). This demonstrates that our method can be used to produce customized comparisons for the user.
- Then the whole pipeline for sentiment analysis.
