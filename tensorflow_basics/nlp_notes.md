NLP is Natural Language Processing.
It is a method of understanding text.

#### Word based encodings

Letters can be encoded with ASCII, but trying to make sense of the encoding can be quiet difficult because letters dont have as much meaning as words in a sentence

Create word based encodings to input into a Neural Network.

### Input Data preperation
1. generate tokens for all words in the input data
2. create token for unknown tokens for future data
3. generate sequences of tokens for every input sentence
4. pad sequences so they are the same length for input into a neural network


### Tools
Tokenizer is used to tokenize sentences
fit_on_texts(sentences) is used to tokenize a list of sentences
texts_to_sequences(sentences) is used to encode a list of sentences to use those tokens
oov_token=<Token> specifies a token to use for unknown words
- if no token is given they are skipped in the sequence
pad_sequences function from the tensorflow.keras.preprocessing.sequence namespace is used to pad sequences of different lengtsh so they can be fed into a neural network
- the longest sequence by adding zeros to the beginning of shorter ones
- Pass padding=’post’ to pad_sequences when initializing it to add zeroes to the end