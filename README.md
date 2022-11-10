# Boolean Retrieval System

The objective of the project is to build a Boolean Retrieval System that takes in boolean queries as the input from the user and returns the relevant documents from the corpus.

The document corpus used in this project consists of 42 Shakespear Plays in text file format.

The boolean queries consist of terms in the vocabulary joined using 'and', 'or' or 'not'.




## Model Building
**Pre-processing**
* Removal of punctuation and stop words
* Normalization using Porter stemmer

NLTK Library was used for the above tasks.

**Boolean Retrieval**

* An inverted index data structure was constructed as a Python Dictionary.
* The data structure consists of all the unique words in the vocabluary of the corpus as the keys and the indices of the documents which contain the respective words as the values for each of the keys.
* Upon passing a query, the dictionaru is searched for the words in the query and the documents consisting of the words are taken into consideration.


## Additional Features
**Spelling Correction**

* Levenshtein Distance Method was used for the Spelling Correction task.
* This feature maps an incorrectly spelled word in the input query to the nearest word in the vocabulary using the above method.

**Wildcard Queries**

* Permuterm Indices method was used.
* This feature performs Boolean Retrieval for even those queries consisting of incompletely spelled words by considering all the possible completely spelled words from the given incompletely spelled word.

The above two features make the Retrieval System more user-friendly.
