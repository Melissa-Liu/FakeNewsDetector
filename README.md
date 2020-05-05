# FakeNewsDetector


## Introduction

Here, we explore a method of fake news detection using natural language processing techniques. Analyzing body text of over 13,000 online news articles, we apply n-gram bag-of-words techniques and word embeddings. The resulting features were used with a number of classification algorithms including Naïve-Bayes, SVM, and LSTM networks. We follow up with an analysis of the effects that varying degrees of imbalanced datasets have on the model to imitate the reality of fake news detection. Accuracies upwards of 90% were observed in the most successful model (LSTM), but training on less balanced sources resulted in a degradation of F1 scores.

## Methods
A number of NLP approaches involve analyzing the frequency of certain words or phrases in a body of text. The simplest is the bag-of-words model, where text is represented as a set of word-frequency pairs. By using word frequency and occurrence, features can be identified for use in document classification. The n-gram is a more complex variant of the model, where contiguous sequences of words of length n are collected from a text corpus. Unigram and bigram methods were used, but better results were observed with the former.

Both bag-of-words and its n-gram derivative disregard word order or relations. Contrarily, word embeddings map words into N-dimensional vectors, with semantically similar words having comparable values. In essence, embeddings attempt to capture the relationship between words. An example of one such model is GloVe, an unsupervised model that uses co-occurrence relations between words to derive meaning.

Because fake news is a relatively recent phenomenon, research into its detection is in its infancy. However, initial attempts at linguistic analysis of news reliability yield promising results, with greater uses of repetitive content, stopwords, and decreased punctuation seen in misleading news. The stopwords used during feature extraction was the default list of English stopwords in addition to words identifying the source URL, such as “CNN, guardian, …”.
