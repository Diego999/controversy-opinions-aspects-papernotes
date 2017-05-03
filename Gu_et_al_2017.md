# Cascaded Convolutional Neural Networks for Aspect-Based Opinion Summary

This paper focuses on online reviews analysis.

Topic modeling is not suitable for summarizing reviews on particular products in many respects.

This paper takes a line different from prior work on aspect extraction: directly mapping each review sentence into pre-defined aspect categories.
Sentences has to be manually labelled with a set of aspects among predifined ones and sentiments.

Step:

- Crawled reviews & segment sentences
- Feed X CNN to find if a sentence has one of the aspect of X (each CNN detect a specific aspect)
- Determine sentiment polarity of the sentence

Why not investigate this kind of solutions of NN ?

Assumption: 1 aspect per sentence ! (not like D_and_Thakur 2016)