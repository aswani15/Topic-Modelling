# Topic-Modelling
Abstract:
Topic modelling is a text mining approach where we process of extracting the summaries that are
available in a given text corpus is possible. The number of topics that are to be extracted depends on the
prior knowledge of the user or the through interpretability of the results for the given number of topics.
Data collection, Data exploration, Data cleaning:
We are interested in finding the major motivations that drove the deals from the deal rationale that is
provided from the given data source.

There are in total 2815 deals which have corresponding deal rationales that happened across 5
industries for 3 years.
Data was cleaned by removing all the common stop words from English language also called the fillers,
the numbers, punctuations and symbols.

Analytical methods and Technology:

There are 2 major techniques that are used to find the latent topics for the text, NMF and LDA. The
mathematical derivations how the topics were derived for NMF and LDA were quite different. LDA is
based on probabilistic graphical modelling and NMF relies on Linear algebra. Both algorithms take as
input a bag-of-words matrix (i.e., each document represented as a row, with each columns containing
the count of words in the corpus). The aim of each algorithm is then to produce 2 smaller matrices; a
document to topic matrix and a word to topic matrix that when multiplied together reproduce the bag
of words matrix with the lowest error.

A tf-idf (Term Frequency – Inverse Document Frequency) transformer is applied to the bag of words
matrix that NMF must process with the TfidfVectorizer. LDA on the other hand, being a probabilistic
graphical model (i.e. dealing with probabilities) only requires raw counts, so a CountVectorizer is used.

Interpretation of Output/Visualization:

After preprocessing the all the deal rationales they are made into bag of words, We sort all the words
according to their frequency’s and filter out the top 1000 word frequencies, these will help us to remove
the noise in the data results in better interpretation of results. These bag-of-words are used as features
and each feature takes the values as the count of number of occurrences of each word in a given
document.

For 5 industries we took the number of latent topics to be 6. For each topic we can see the major words or 
say terms that are occurring in that topic which will help us to label the given topic. The labelling of the 
topics has to be done manually form the resultant output. After analyzing the outputs from the two models,
we can interpret the NMF model output more easily than the resultant output. The 6 resultant topics are not 
ordered in terms of importance and are independent of each other.

The interpreted topic for NMF output is:
Topic – 1: Expand presence Geographically.
Topic – 2: Expand Customer Base.
Topic – 3: Network Expansion.
Topic – 4: Expand Market Share
Topic – 5: Expand Customer Base.
Topic – 6: New Product Acquisition
