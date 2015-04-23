# Lecture 4: Setting

## Anatomy of the Corpus

Isolated, Categorized, Tagged, Temporal

## Tokens
```
import nltk

nltk.download()

from nltk.book import *

# Token (word)
tokens = text1.tokens
len(text1)

# Type (vocab)
words = text1.vocab()
len(words)
words?

types = words.keys()
types?

%who

# Lets build our own stemmer
stems = []
suffixes = ['ed','ly','s']

for suffix in suffixes:
    for type in types:
        if type.endswith(suffix):
            stems.append(type[:-len(suffix)])
