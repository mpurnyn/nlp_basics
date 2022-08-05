# Vector Space Models

**Vector Spaces** are fundamental in NLP. 
When you encode words you encode them as vectors
The vector space contain information about the words relationship to other words in the source **corpus**.
The vector space helps you idenfify relationships between words.

"You shall know a word by the company it keeps" - Firth

#### Common usage of Vector Space Models
information extraction
machine translation
chatbots

# Designing Vector Spaces
## Co-ocurrance (word to word) Matrix
- A 2D matrix i,j that shows many times word_i with word_j apears in a window of size k.

## Word to Document Matrix
- same as above but
- a matrix that shows how often a word_i appears in document_j

# Comparing Vector Spaces

## Euclidian Distance
- a similarity metric for vectors
- it is the distance between two points
- but it can be misleading if the relative sizes of the vectors you are comparing is large. You want a metric that represents similarity only.s
- so instead of raw distance between the vectors, compare the angle between them with Cosine similarity.

## Cosine Similarity
- similar vectors - the angle between them is 0 so cosine is 1.
- orthogonal/dissimilar vectors
  - the angle between them is 90. Cosine is 0.
- you want something in between
- main advantage is that it is not biased by vector size


## Manipulating Word Vectors

If vectors of words capture the meaning of the word you can perform math to capture similar relationships
    moscow:russia as ankara:turkey
    moscow-russia+turkey=ankara


# Visualizing Large Vectors

## Dimensionality Reduction
### Principal Component Analysis / PCA
- an unsupervised learning algorithm for reducing the dimensions of a matrix to 2 for easy plotting.
- results in clusters of similar words.

**Eigenvectors** 
- the direction of uncorrelated features
**Eigenvalues** 
- the amount of information retained by each feature.
- the variance of new features

#### Steps
1. Mean Normalize Data
2. Get Covariance Matrix
3. perfom Singular Value Decomposition
- results in a set of three matrices. eigenvectors, eigenvalues
4. Dot Product between Word Embeddings and the first N colums of matrix. N is the number of dimensions you want at the end.
5. Percentage of Retained Variance retained in new vector space. The quotient of the sum of the i values of eigenvectors in the matrix over the sum of the j values of the eigenvector matrix.