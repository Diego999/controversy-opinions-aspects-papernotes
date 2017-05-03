# Discovering Coherent Topics Using General Knowledge

They propose a framework to leverage the general knowledge in topic models while handing wrong knowledge (words have multi-senses!). Their model GK-LDA is able to effectively exploit the knowledge of lexical relations in dictionaries.

Their approach leverage lexical knowledge about words and their relationships available in online dictionaries or other sources that can be exploited in a model to generate more coherent topics.

They model the lexical relations (called LR-sets) as {synonyms, antonyms and adjective-attributes} for each sense in WordNet ! 
LR-sets are domain independent and automatically extracted from the sources. Thus, contain much more noise and demanding additional mechansims to explicitly deal with it. (where a method is integrated within GK-LDA).

Very detailed ... should read it later