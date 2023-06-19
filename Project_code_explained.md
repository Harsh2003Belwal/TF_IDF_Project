# TF_IDF_Project
Term Frequency: This summarizes how often a given word appears within a document. Inverse Document Frequency: This downscales words that appear a lot across documents.

**TF-IDF Code Explained**

TF-IDF stands for Term Frequency Inverse Document Frequency of records. It can be defined as the calculation of how relevant a word in a series or corpus is to a text. The meaning increases proportionally to the number of times in the text a word appears but is compensated by the word frequency in the corpus (data-set).

- **Libraries and Modules used:**

1. *sys* : It is a module in Python's standard library that provides
access to system-specific parameters and functions. In this
code, it is used to retrieve command line arguments.

2. *math* : It is another module in Python's standard library that
provides mathematical functions and operations. It is used here
to calculate the logarithm for IDF calculations.

3. *defaultdict* : It is a class from the collections module in
Python's standard library. It is a subclass of the built-in dict
class and provides a default value for missing keys. It is used to
store the frequency values for words.

- **Variables:**
1. *document* : This variable stores the file path of the document
provided as a command line argument (first argument after the
script name).

2. *words* : This variable is a list that stores the words provided as
command line arguments (starting from the second argument
after the script name).

3. *tf* : It is a defaultdict that will store the term frequency values
for the words in the document.

4. *idf* : It is a defaultdict that will store the inverse document
frequency values for the words in the document.

5. *tfidf* : It is a defaultdict that will store the TF-IDF values for the
words in the document.

- **Functions:**

1. *calculate_tf(document*) : This function calculates the term
frequency (TF) for each word in the document. It reads the
document line by line, splits each line into words, and updates
the TF values in the tf defaultdict. The TF values are
normalized by dividing them by the total number of words in the
document. The function returns the TF values as a defaultdict.

2. *calculate_idf(document, words)* : This function calculates the
inverse document frequency (IDF) for each word in the
document. It reads the document line by line and checks if each
word is present in the set of words provided as an argument. If
a word is found, the IDF value for that word is incremented in
the idf defaultdict. Finally, the IDF values are calculated by
taking the logarithm of the total number of documents divided
by the number of documents containing the word. The function
returns the IDF values as a defaultdict.

- **Main Code Execution:**

1. The code starts by retrieving the command line arguments
using sys.argv and assigns the values to the document and
words variables.
2. The calculate_tf function is called with the document as an
argument, and the returned TF values are stored in the tf
variable.
3. The TF values for the specified words are printed to the
console.
4. The calculate_idf function is called with the document and
words as arguments, and the returned IDF values are stored in
the idf variable.
5. The IDF values for the specified words are printed to the
console.
6. The TF-IDF values are calculated by multiplying the TF and IDF
values for each word and stored in the tfidf defaultdict.
7.The TF-IDF values along with TF and IDF values for each word
are written to an output file named "output.txt".

**This code performs the following steps: it reads a document, calculates
the TF and IDF values for the specified words in the document, prints the
TF and IDF values to the console, and writes the TF-IDF values along
with TF and IDF values to an output file**
