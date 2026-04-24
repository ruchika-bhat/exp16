
## Lab Report: NLP Techniques on Text Data
**Student Name:** Riya Latkar
**PRN:** 25070123092
**Experiment No:** 16

### 1. Aim
To implement fundamental Natural Language Processing (NLP) techniques such as Tokenization, Stop Word Removal, Stemming, Lemmatization, and POS Tagging using the `nltk` library in Python.

### 2. Theory
Natural Language Processing is a branch of AI that deals with the interaction between computers and human languages. Key preprocessing steps include:
* **Tokenization:** Breaking text into smaller units like words (Word Tokenization) or sentences (Sentence Tokenization). 
* **Stop Word Removal:** Filtering out common words (e.g., "is", "the", "a") that carry little unique meaning to reduce data noise.
* **Stemming:** Reducing words to their root form by chopping off suffixes (e.g., "running" $\rightarrow$ "run"). It is fast but can sometimes result in non-dictionary words (e.g., "studies" $\rightarrow$ "studi").
* **Lemmatization:** A more sophisticated way of finding the root (lemma) using a dictionary. It ensures the root is a valid word (e.g., "studies" $\rightarrow$ "study"). 
* **POS Tagging:** Assigning grammatical categories (Noun, Verb, Adjective) to each word in a sentence.

### 3. Logic
The logic of text preprocessing follows a "Refining" pipeline:
1.  **Download Resources:** Accessing pre-trained models and linguistic databases (like WordNet).
2.  **Breakdown:** Splitting raw paragraphs into manageable tokens.
3.  **Cleanse:** Removing the "glue" words (Stop Words) that don't help in understanding the topic.
4.  **Normalize:** Bringing different forms of the same word to a single base form (Stemming/Lemmatization).
5.  **Contextualize:** Identifying the role of each word (POS Tagging) to understand the sentence structure.
6.  **Analyze:** Calculating the frequency of words to find the most important terms.

### 4. One-Liner Explanations
**Libraries & Commands:**
* `import nltk`: Imports the Natural Language Toolkit library for text processing.
* `nltk.download('punkt')`: Downloads the data required for the tokenizer to recognize punctuation/boundaries.
* `word_tokenize(text)`: Splits a string into a list of individual words and punctuation.
* `sent_tokenize(text)`: Splits a paragraph into a list of individual sentences.
* `stopwords.words('english')`: Loads a list of common English words to be ignored during analysis.
* `PorterStemmer()`: Initializes the algorithm that chops off word endings to find the root.
* `WordNetLemmatizer()`: Initializes the tool that uses a dictionary to find the meaningful base of a word.
* `pos_tag(words)`: Labels each word with its part of speech (e.g., 'NNP' for Proper Noun).
* `FreqDist(word)`: Computes the frequency distribution of words to see which ones appear most often.

### 5. Algorithm
1.  **Import** the `nltk` library and download necessary sub-packages (`punkt`, `stopwords`, `wordnet`).
2.  **Tokenize** the input text into words or sentences using `word_tokenize` or `sent_tokenize`.
3.  **Filter** the word list by checking against the `nltk` stopwords list.
4.  **Stem** the words using `PorterStemmer` to see the "chopped" root versions.
5.  **Lemmatize** the words using `WordNetLemmatizer` for a more accurate dictionary-based root.
6.  **Tag** the tokens with their parts of speech using `pos_tag`.
7.  **Calculate** word frequencies using `FreqDist` and display the most common tokens.

### 6. Conclusion
In this experiment, I successfully performed several NLP preprocessing steps. I observed that while **Stemming** is faster, **Lemmatization** provides more accurate results for linguistic analysis. Furthermore, **POS Tagging** and **Frequency Distribution** allowed me to understand the structural and statistical importance of words in a dataset. These techniques are the essential first steps for building sentiment analysis models or chatbots.
