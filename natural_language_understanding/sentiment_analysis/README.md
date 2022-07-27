# Sentiment Anaylsis

- A Simple NLP problem where you want to try and find if text, sentences, phrases have a particular sentiment
- Generally this problem is a Supervised Learning problem

# Feature Extraction
- NLP Models need inputs (sentences) to be converted to Feature Vectors.
- A simple way of creating this vector is by counting the number of times each word appeared in either the postive classe or negative class (from the labeled training data). You end up with a feature vector as long as the input.
- To condence the feature vectors


# Terms
- logistic regression
    - sigmoid function
- cost function
- bayes thereom
    - laplacian smoothing
    - log likelihood
    - naiive bayes
    - training naiive bayes
    - error analysis


# Python Libraries

    from utils import process_tweet, lookup
    import pdb
    from nltk.corpus import stopwords, twitter_samples
    import numpy as np
    import pandas as pd
    import nltk
    import string
    from nltk.tokenize import TweetTokenizer
    from os import getcwd
    import w2_unittest