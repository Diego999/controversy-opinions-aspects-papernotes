# Topic Significance Ranking of LDA Generative Models

Using LDA on a corpus generates a certain number of topics where some are irrelevant or represent insignificant themes. Current approaches to tpoic modeling perform manual examination of their output to find meaningful and important topics.

They propose a basic idea consisting of measuring the distance between a topic distribution and a junk distribution.

To identify Junk and Insignificant (J/I) topics, the approach is to define a decision criterion C as the distance D of the topic from a common J/I topic descrpition Omega. If the distance is large, then this would provide a fair indication of the topic significance. However, if the distance of a topic to the J/I distribution is small, then the topic is more likely to be irrelelvant to the domain structure.

The authors defined 3 types of J/I topics distribution and measure for each topic its distance to all of them and then do a simpled weighted linear ocmbination. This phase is split into 4 parts:

- standardization procedures to have a measure for the same scale (among KL, cosine and correlation coefficient)
- intra-criterion phase to merge the standardized measurements of each topic within each J/I definition
- (inter-criterion) two different techniques of weighted combination are performed to combine the J/I scores to constrcut a weight and a total score for each topic from which the final rank of the topic significance is computed.
- final rank is computed.
