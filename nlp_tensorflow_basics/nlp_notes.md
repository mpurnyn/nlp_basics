NLP is Natural Language Processing.
It is a method of understanding text.

### Concepts
**Word based encodings or "tokenizing"**
Encoding in this context is converting the text into an encoded form (a number)
Individual Letters could be encoded with ASCII, but trying to make sense of the encoding can be quiet difficult because letters dont correlate with the meaning of the overall sencence as words do. Create word based encodings to input into a Neural Network.

**Embedding Dimension**
- the number of dimensions for the vector representing the word encoding

### Input Data preperation
1. generate tokens for all words in the input data
2. create token for unknown tokens for future data
3. generate sequences of tokens for every input sentence
4. pad sequences so they are the same length for input into a neural network


### Tensorflow Library Elements
#### Basic Tokenizer
**Tokenizer** initialize this class to tokenize sentences (create encoding from a collection of words)
**fit_on_texts(sentences)** Tokenizer class function tokenizes a list of sentences
- optional parameter **num_words=n** specifies the maximum number of words to be tokenized, and picks the most common ‘n-1’ words
**texts_to_sequences(sentences)** is used to encode a list of sentences to use those tokens
**oov_token=<Token>** specifies a token to use for unknown words
- if no token is given they are skipped in the sequence
**pad_sequences()** from the tensorflow.keras.preprocessing.sequence namespace is used to pad sequences of different lengths so they can be fed into a neural network
- the longest sequence by adding zeros to the beginning of shorter ones
- Pass padding=’post’ to pad_sequences when initializing it to add zeroes to the end
#### Embedding and Neural Networks
**tf.keras.layers.Embedding** import to use the word embeddings layer in TensorFlow as a sequential layer.
**Binary crossentropy** a loss function that works on data that needs has a binary output (0 or 1).


### Useful Tools

**TensorFlow Datasets**
- TensorFlow library containing common data that you can use to train and test neural networks
