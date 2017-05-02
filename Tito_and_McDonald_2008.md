# Modeling Online Reviews with Multi-grain Topic Models

This paper presents models based on extensions to standard topic modeling methods such as LDA and PLSA to induce multi-grain topics. The models not only extract ratable aspects but also cluster them into coherent topics.

LDA and PLSA do not model the appropriate aspects of user reviews. The proposed models generate terms from either a global topic or a local topic that is chosen based on a sliding window context over the text. The local topics more faithfully model aspects that are rated thorughout the review corpus. Furthermore, the number of quality topics is drastically improved over standard topic models that have a tendency to produce many useless topics in addition to a number of coherent topics.

## PLSA

Generation of a word in this model is defined as follows:
- choose document
- choose topic
- choose word

The main drawback is that PLSA is inherently transductive, i.e., there is no direct way to apply the learned model to new documents. Moreover, the need to combat overfitting is present.

LDA solves both problems

## LDA

Generation of a document in this model is defined as follows:

- choose distribution of topics
- for each word i in document d
	- choose topic
	- choose word

LDA has two parameters which prevents it from overfitting (alpha beta). Unfortunately, exact inference in such model is intractable and various approximations have been considered. Another approach is to use a Markov chain Monte Carlo algorithm for inference with LDA.

## Cons PLSA LDA

Both uses bag-of-words representation of documents, therefore they can only explore co-occurences at the document level. The infer topics corresponding to distinguishing properties of items. Though these are all valid topics, they do not represent ratable aspects.

Discovering topics that correlate with ratable aspects, such as cleanliness and location for hotels, is much more problematic with LDA or PLSA.

One way to address this problem would be to consider co-occurences at the sentence leven, i.e., apply LDA or PLSA to individual sentences. But in this case, we won't have a sufficient co-occurence domain, and it is known that LDA and PLSA behave badly when applied to very short documents. However, this problem can be addresse by explicitly modeling topic transitions but is computationnaly expensive.

## MG-LDA

MG-LDA models two distinct types of topics: global topics and local topics. As in PLSA and LDA, the distribution of global topics is fixed for a document. However, the distribution of local topics is allowed to vary across the document.

The hypothesis is that ratable aspects will be captured by local topics and global topics will capture properties of reviewed items. Local topics are expected to be reused between very different types of items, whereas global topics will correspond only to particular types of items. Finally, definition of multi-grain is simply for 2-levels of granualirty:global and local.

Importantly, the fact that the windows overlap, permits to exploit a larger co-occurence domain. These simple techniques are capable of modeling local topics without more expensive modeling of topics transitions.

