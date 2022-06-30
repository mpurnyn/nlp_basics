
### Implementing LSTM in tensorflow
**tf.keras.layers.lstm(number_of_outputs_desired)**
- adds lstm. one directional.
**bidirectional(tf.keras.layers.lstm(number_of_outputs_desired))**
- makes cell state go in both directions
- output is double the number of outputs because it is bidirectional.
**Conv1D(128, 5, activation-'relu')**
- sequence make a large difference when determining semantics of language
- because the order in which words appear dictate their impact on the meaning of the sentence

### important hyperparameters


    EMBEDDING_DIM: Dimension of the dense embedding, will be used in the embedding layer of the model. Defaults to 100.

    MAXLEN: Maximum length of all sequences. Defaults to 16.

    TRUNCATING: Truncating strategy (truncate either before or after each sequence.). Defaults to 'post'.

    PADDING: Padding strategy (pad either before or after each sequence.). Defaults to 'post'.

    OOV_TOKEN: Token to replace out-of-vocabulary words during text_to_sequence calls. Defaults to "\".

    MAX_EXAMPLES: Max number of examples to use. Defaults to 160000 (10% of the original number of examples)

    TRAINING_SPLIT: Proportion of data used for training. Defaults to 0.9


### Methods in NLP course

#### Method 1 - Averaging

    Embedding(vocab_size, embedding_dim. input_length)
    GlobalAveragePooling1D(),
    - average output of embedding
    Dense(24, activation='relu')
    Dense(1, activation='sigmoid')
- high accuracy
- fast accuracy
- loss decreases quickly
- flattens out

#### Method 2 - LSTM

    Embedding(vocab_size, embedding_dim. input_length)
    Bidirectional(tf.keras.layers.LSTM(32)),
    Dense(24, activation='relu')
    Dense(1, activation='sigmoid')
- slower accuracy
- highest accuracy
- loss decreased
- validation loss kept increasing
    - indicates some overfitting is needed 


#### Method 3 - Convolution

    Embedding(vocab_size, embedding_dim. input_length)
    Conv1D(128, 5, activation='relu')
    - params: convolutions you want to learn, their size, and activation function
    GlobalMaxPooling1D(),
    Dense(24, activation='relu')
    Dense(1, activation='sigmoid')

#### Method 4 - Flatten

    Embedding(vocab_size, embedding_dim. input_length)
    Flatten(),
    Dense(6, activation='relu')
    Dense(1, activation='sigmoid')
- fastest, but least accurate

#### Method 5 - GRU

    Embedding(vocab_size, embedding_dim. input_length)
    Bidirectional(tf.keras.layers.GRU(32)),
    Dense(6, activation='relu')
    Dense(1, activation='sigmoid')

- slower
- high parameters