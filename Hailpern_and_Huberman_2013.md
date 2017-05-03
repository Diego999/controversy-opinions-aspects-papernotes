# Echo: The Editor's Wisdom with the Elegance of a Magazine

Echo traverses a corpus of documents and sitill crucial opinions from the collective intelligence of the crowd (=corpus). It does opinion alignment. Echo placecs individual opinions in document context and crowd context, allowing users to quickly find those opinions. Echo visually distorts the text of a document, bringing to the user's attention the key opinions in each document.

Echo identifies the most important aspects discussed in a news corpus and computes the consensus opnion for each one. The consensus opinion was then used as context to individual opinions found in the news texts.

Methodology:

- Content extraction and reconstruction
- Topic model and keyword identification. Identify what the articles within a corpus are talking about. Limit to nouns. Feed LDA with filtered documents to extract topics and associated keywords across all documents. Then compute word rank which is topic independent. Provides the most important subjects of dicussion in the corpus.
- Subject Modifiers and sentiment detection. Similar to Odin (uncover which modifiers were applied to any sentence). Then do sentimient analysis.
- Cross-Document Aggragation. Compute the crowd's opinion on a given subject.
- Visual distortion of crucial opinions

