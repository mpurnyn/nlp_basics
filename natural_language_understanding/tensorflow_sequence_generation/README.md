# Sequence Generation

- can be thought of as a prediction problem.

- with NN trained on a large enough corpus of words and phrase and a prediction you can do sophisticated sequence generation. 

1. split text by delimeters to get words
2. tokenize words
3. create token sequences
    - generate subphrases
    - pad to same length
4. turn sequences into inputs and labels
5. convert labels to a 1-hot encoding using **tf.keras.utils.to_categorical(labels, num_classes=total_words)**

6. **Creating a model for sequence generation of poem/song**
embedding layer
    - want it to handle all our words
    - dimension to plot vector of word
    - input is length of longest sequence -1
lstm
    - their cell state carries context along. not just next door neighbors. specify 20 units
dense
    - one nueron per word so that each word lights up
compile
    - categorial classification so categorical crossentropy
    - adam classifier
fit
    - train for 500 epochs

### Hyper Parameters to try tuning
- dimentionality of embedding
- LSTM units and directionality
- learning rate for adam optimizer
- epocs

**Running the model**
pass a "seed" to the model and get a token.
covert token to word.
over time the words should become nonsense

**Notebook1**


**Notebook2**

**Lab**


# Takeaways
- as more text is generated, it is more likely to become gibirish because the probability that a word matches the whole phrase goes down as you add more words.
- there are more words in a corpus than there are characters in a language so it increases the memory needed for a word-based neural network
- it is critical to generate subphrases of a corpus of text and padd the sequences so they are the same length
- to_categorical is used to create one_hot matrixes