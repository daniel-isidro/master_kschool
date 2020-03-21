# Natural Language Processing
## Víctor Peinado, Reply.ai (ex-Google)

* **Transfer Learning** Knowledge acquired during model training can be transferred to other models

* **2 tasks in NLP:** Natural language understanding (NLU) and Natural language generation (NLG)

* Graphs are used to represent the dependencies between the words in a text when doing NLP

* Stop words were usually removed from texts in NLP (preposiciones, conjunciones, determinantes). Not anymore in modern techniques

* With ```scikit.learn``` we can give weight to the words so stop words don't have more importance for being more frequent in texts

* NLP when translating works very well with well written texts, not so well with coloquial texts or slang.

* ```NaiveBayesAnalyzer``` included in ```textblob.sentiments``` gives probability of positive sentiment and probability of negative sentiment in whole sentences

* **Data in the training set always have to be representative of the test data** . Using trained models of movie reviews for predicting sentiments in hotel reviews is not very useful nor accurate

* ```spacy``` model es_core_news_md: Spanish-based on news-medium size (there are larger and smaller models)

* **Word vectors** have revolutionized NLP in the last years. Big companies have been training models, competing amongst them, and offer the models for free. We can use those models and fine-tune them for adjusting them to your problem. For example, you can use BERT (from Google) and fine tune it (supervised learning withtags, with just hundreds of examples) for the fashion industry. Semantic similarity between words has benefited from this.

* GloVe (Global Vectors for Word Representation) is an unsupervised (in reality self-supervised) algorithm for obtaining vector representation for words. Similarity in GloVe varies from -1 (dissimilar) to 1 (similar)

* ```gensim```: topic modelling for humans

* ```fasText```: word vectors models trained by Facebook 
