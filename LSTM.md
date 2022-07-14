
### Implementing LSTM in tensorflow
**tf.keras.layers.lstm(number_of_outputs_desired)**
- adds lstm. one directional.
**bidirectional(tf.keras.layers.lstm(number_of_outputs_desired))**
- makes cell state go in both directions
- output is double the number of outputs because it is bidirectional.
**Conv1D(128, 5, activation-'relu')**
- sequence make a large difference when determining semantics of language
- because the order in which words appear dictate their impact on the meaning of the sentence

