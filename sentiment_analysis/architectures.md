
# Architectures Examples for Sentiment Analysis
- all the architectures start with embedding layer taking the feature embedding vectors
- all the architectures end in a dense layer of 1 neuron because "sentiment" is either positive or negative

#### Averaging

    Embedding(vocab_size, embedding_dim. input_length)
    GlobalAveragePooling1D(),
    - average output of embedding
    Dense(24, activation='relu')
    Dense(1, activation='sigmoid')
- high accuracy
- fast accuracy
- loss decreases quickly
- flattens out

#### LSTM

    Embedding(vocab_size, embedding_dim. input_length)
    Bidirectional(tf.keras.layers.LSTM(32)),
    Dense(24, activation='relu')
    Dense(1, activation='sigmoid')
- slower accuracy
- highest accuracy
- loss decreased
- validation loss kept increasing
    - indicates some overfitting is needed 


#### Convolution

    Embedding(vocab_size, embedding_dim. input_length)
    Conv1D(128, 5, activation='relu')
    - params: convolutions you want to learn, their size, and activation function
    GlobalMaxPooling1D(),
    Dense(24, activation='relu')
    Dense(1, activation='sigmoid')

#### Flatten

    Embedding(vocab_size, embedding_dim. input_length)
    Flatten(),
    Dense(6, activation='relu')
    Dense(1, activation='sigmoid')
- fastest, but least accurate

#### GRU

    Embedding(vocab_size, embedding_dim. input_length)
    Bidirectional(tf.keras.layers.GRU(32)),
    Dense(6, activation='relu')
    Dense(1, activation='sigmoid')
- slower
- high parameters