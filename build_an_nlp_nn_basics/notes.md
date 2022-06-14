# Embedding words
words that have similar meanings should be grouped together
use a higher dimension vector for storing the meaning of a sentence
compare these vectors.

- embedding into vectors
- build a classifier for vectors
- clustering

## IMBD Movie Reviews Dataset
http://ai.stanford.edu/~amaas/data/sentiment/

## Tensorflow Datasets
https://www.tensorflow.org/datasets

## Displaying Embedding Vectors
https://projector.tensorflow.org/

### Preparing Data
same as the previous step
1. download and import data
2. split data into trainign and testing
3. extract sentences and labels from training
4. tokenize sentences
5. fit on sentences
6. convert to sequences
7. pad sequences

### Training Neural Network

Question 1

What is the name of the TensorFlow library containing common data that you can use to train and test neural networks?

Question 2

How many reviews are there in the IMDB dataset and how are they split?

Question 3

How are the labels for the IMDB dataset encoded?

Question 4

What is the purpose of the embedding dimension?

Question 5

When tokenizing a corpus, what does the num_words=n parameter do?

Question 6

To use word embeddings in TensorFlow, in a sequential layer, what is the name of the class?

Question 7

IMDB Reviews are either positive or negative. What type of loss function should be used in this scenario?

Question 8

When using IMDB Sub Words dataset, our results in classification were poor. Why?