# Browsing News According to Subjects and Opinions

ObViz is an automated news delivery system that balances the opinions shown to readers. It separates a stream of news articles into different subjects and for each subject, it identifies articles holding opposing views with respect to that subject. By balancing the opinions shown to the users, they counter the individual article bias and also the reader's selective exposure.

(example aspect and opinion: "The economy is growing.", aspect:economy and opinion:positive (growing)).

Difference with NewsCube (Park_et_al_2009):Newscube organize news articles around the discussed aspects however, textual opinions are the keys to understand controversy (which is not handled by NewsCube).
assume that articles related to a certain subject are already given and the key words are extracted manually

Difference with Odin: Odin merges all the topics in one set.

Such tools have been shown to be useful when a clear consensus exists, for controversial subjects it will be difficult to reliably extract a correct consensus opinion.

Methodology:
- Generate a representation of the subjects that are present in current news, using topic modeling. Use LDA to automatically detect topics and their keywords. However, some obtained topics are coherent while others not at all. Use the insight of Topic Significance Ranking of LDA Generative Models (AlSumait_et_al_2009) to find the appropriate number of topics and try to decrease uncoherent topics. After topics are found, they eliminate topics that resemble the others too muche by ranking topics by their "uniqueness" (defined as the inverse of the number of words shared with other topics) and remove half of the topics. **Still noise afterwards !**
- A subject consists of the topic keywords and a selection of relevant articles.
- Determine aspects associated with opinions within each subject. Because **LDA topics cannot be directly used as aspects** in opinion mining because the syntactic relations between words are lost ! Thus, they use double propagation algorithm. At the end, they have a aspects set for each topic.
- For each article among a given topic, they search for opinions attached to aspects of the topics. They compute the polarity of words that is in a direct syntactic relation with the aspect a. The subjectivity of an aspect occurence is the sum of the polarities of the associated words. (remove irrelevant relations such that prep).
- Opposing articles. For each article, they aggregate (sum) the subjectivities found towards the given aspect into a single subjectivity value of tje article words its topic. With this, they obtain the most positive articles and the most negative articles.
- Finally, to compute the perspective balancing, they have a simple formula.


