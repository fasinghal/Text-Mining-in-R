# Text-Mining-in-R
TM package :  CS 6301 R for Data Scientists Lecture 9 coursework - Text Mining in R (tm)

To compare text documents, we must gather the documents together and load them into R This is called a corpus There are two popular packages in R: tm and text2vec We’ll look at how to use these on a simple example, but first some background.

tf–idf: short for term frequency–inverse document frequency
◦ A numerical statistic that measures how important a word is to a document
◦ Basic idea: create a statistic for each word that is a combination of how frequently the word appears in a document and how rare or uncommon the word is
◦ The assumption is that important terms are more uncommon, while the more common terms (“is”, “the”, etc.) are not as important
The “tf” part is usually just a simple frequency count for the term, but it can also be scaled For the idf, use a log of the inverse fraction of the percentage of docs that contain the term
◦ IDF(t) = log(Total number of documents / Number of documents with term t in
it).
◦ So it the proportion of docs that contain the term is small, the inverse fraction
is large, and the log scales this
◦ There are other scalings as well
Multiply these together to get the tf-idf number for each term. Extension of idea – Bag of N-Grams, which considers phrases of
length n 

Text Mining in R
Not a huge field, since text problems tend to be Big Data problems(huge corpus)
There seem to be two popular packages, tm and text2vec
◦ The first is older, the second is more oriented towards vector processing (i.e. big data stored in distributed system), and hence is optimized for performance
◦ There have been performance enhancements in tm They have very different APIs
We will look at tm for now
