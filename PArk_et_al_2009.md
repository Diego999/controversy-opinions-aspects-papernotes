# NewsCube: Delivering Multiple Aspects of News to Mitigate Media Bias

NewsCube automatically creates and promptly provides readers with multiple classified viewpoints on a news event of interests. It helps readers easily discover rich facts and compare diverse biased views of the event.
The core of NewsCube is aspect-level browsing, a new method to provide readers with a classified view of a set of articles with different aspects.

Media bias can be alleviated using aspect-level browsing. However, two articles can discuss the same aspects and still have different, even opposite conclusions.

Methodology:

- Collection
- Classification: Use clustering. Aspects of news articles have to be extracted and articles have to be grouped regarding the similarity of the extracted aspects. They leverage the structure of news writing rules "inverted pyramid style of news writing". Using this scheme, they can get conclusive hints for aspect extraction: where the semantically meaningful keywords are located and how much they are importantly addressed. For keyword selction, they basically extract keywords from the core parts of an article (head, sub-head and lead). Their weights are calcultaed based on the main text (number of occurences and locations of occurences). To create aspect group, they use hierarchical agglomerative clustering method (HAC) starting by considering each article as an individual cluster, the method merges the most similar pair of clusters.
- Presentation

There is no opinion there ! So it shows only aspects related to a specific topic.