
#  IRS Search Engine Project

A web-based **Information Retrieval System** (IRS) that crawls websites, preprocesses content, builds advanced indexes (TF-IDF and positional inverted index), and allows intelligent search by words and phrases.

---

##  Project Overview

This search engine is composed of three major components:

- **Crawler**: Gathers HTML content from websites and extracts all links.
- **Preprocessor**: Cleans and prepares raw text by normalizing, tokenizing, removing stopwords, and stemming.
- **Indexer**:
  - Builds a **TF-IDF index** for ranking documents by relevance.
  - Constructs a **positional inverted index** for precise phrase searching.

---

##  Features

###  Crawler
- Fetches web pages and extracts all valid URLs.
- Avoids re-visiting pages.
- Crawls up to a specified depth.

###  Preprocessing
- Converts text to lowercase.
- Tokenizes into words.
- Removes stop words.
- Applies stemming using the Porter Stemmer.

###  Indexer
- **TF-IDF Index**:
  - Computes term frequency and inverse document frequency.
  - Ranks documents based on relevance.

- **Positional Inverted Index**:
  - Stores the positions of terms in documents.
  - Enables phrase-level search.

---

## System Architecture

1. **Crawl Phase**: Start from a root URL → Fetch content → Extract and follow links.
2. **Indexing Phase**: Preprocess text → Build TF-IDF & Positional Inverted Index.
3. **Search Phase**:
   - Word Search (TF-IDF)
   - Phrase Search (Positional Matching)

---

##  How to Use

###  Execution Steps

1. Run the program.
2. Input the root URL and crawl depth.
3. Choose one of the search options:
   - Search for a **word** (TF-IDF ranked).
   - Search for a **phrase** (exact match via positional index).

###  Example

```
Crawl: https://en.wikipedia.org/wiki/Web_search_engine (depth=3)
Search: "machine learning"
Results: List of ranked URLs based on relevance.
```

---

##  Dependencies

- `requests` – for fetching HTML pages
- `nltk` – for NLP tasks (tokenization, stopwords, stemming)
- `re` – for link extraction
- `collections.defaultdict` – for efficient indexing

> Don't forget to run:
```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

---

##  Algorithms Used

- **TF-IDF**: Weights terms based on frequency and document relevance.
- **Cosine Similarity**: Used to measure similarity between query and documents.
- **Phrase Matching**: Based on positions of terms in documents.

---

##  Author

**Hamza al Aedi**  
[LinkedIn](https://www.linkedin.com/in/hamza-alaedi-395669366)  

