# Deep Learning Basics

Stuff that doesnt fit into NLP or CV applications goes here until I create its own repository for it.

Deep Learning tasks break down into two categories.
- Supervised Learning
    - where you have some labeled data to create a model off of
- Unsupervised Learning
    - where the data is not labeled and the algorithm has to come up with the labels itself.

## Supervised Learning
- **training_data** is a vector of data you want to create a model off of
- **labels** is a same-shape vector with labels for the data X
- **model** - a neural network function made up of layers arcitectures with random weights.
- **cost/loss** - a function used to compare your models results to the data
- **optimizer** - a function used to "guess" how to improve the weights in the model to reduce cost.