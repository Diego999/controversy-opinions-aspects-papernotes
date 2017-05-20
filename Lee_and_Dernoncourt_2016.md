# Sequential Short-Text Classification with Recurrent and Convolutional Neural Networks

The authors present a model based on RNN and CNN which incorporates the preceding short texts. It achieves state-of-the-art results on 3 different datasets for dialog act precition.

Most existing ANN-based systems do not leverage the preceding short texts when classifying a subsquent one. Many short texts occur in sequences !

Short texts usually appear in sequence, therefore using information from preceding short texts may improve the classification accuracy.

The model is split in 2 parts :

1) Generate vector representation for each short text (either using RNN or CNN)
2) Classify short text based on the vector representations of the current as well as a few preceding short texts.

They hypothesize that short-text representations contain richer and more general information than class representations due to their larger dimensions