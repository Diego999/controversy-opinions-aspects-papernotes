# A Structured Self-Attentive Sentence Embedding

New model for extracting an interpretable sentence embedding by introducing self-attention. They use a 2-D matrix to represent the embeddings with a self-attention mechanism and regularization term.

This allows to have embeddings with easier way of visualizing what specific parts of the sentence are encoded into the embedding.

They evaluate the model on 3 tasks : author profiling, sentiment classification and textual entailment. Results shows significant performance gain compared to other sentence embedding methods.

They hypothesize that carrying the semantics along all imte steps of a RN is relatively hard and not necessary. They propose a self-attention mechanism for these sequential models to replace the max pooling/averaging step.

The proposed self-attention mechanism allows extracting different aspects of the sentence into multiple vector representations. It is performed on top of an LSTM in the sentence embedding model.

The model is a BiLSTM followed concatenation of the hidden vector multiplied with an attention matrix with a special designed penalization term !

The current training method heavily relies on downstream applications, thus not possible to train it in an unsupervised way. The major obstacle is during the decoding.
We can still do unsupervised learning on the proposed model by using a sequential decoder on top of the sentence embedding, it merits more to find some other structures as a decoder.