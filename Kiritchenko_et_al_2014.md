# NRC-Canada-2014: Detecting Aspects and Sentiment in Customer Reviews

End up in SemEval 2014 competition : 1,1,3,1/2.

Use large corpora of reviews for restaurants and laptops that were not labeled for aspect terms, aspect categories or sentiment. They generated lexicons from these corpora and used them as a source of additional features.
They used : Yelp restaurant reviews corpus, Amazon laptop reviews corpus.

For the Sentiment Lexicons, they compure a sentiment score for each term in the corpus such thaht PMI(w, pos) - PMI(w,neg).
Also used in additions word clusters on both datasets.

## Aspect Term Extraction

Use in-house NER similar to Bruijn et al 2011.

## Aspect Term Polarity

Use linear SVM with various NLP features.

## Aspect Category Detection

5 binary SVM.

## Aspect Category Polarity

One multi-class SVM.
A sentence can reer to more than one aspect category with different sentiment. If these terms do not appear in the training set, their polarities can still be inferred from sentiment lexicons.