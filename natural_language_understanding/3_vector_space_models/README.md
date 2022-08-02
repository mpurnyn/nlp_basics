# Vector Spaces 
- represent any kind of text by encoding it as a vector. 
- vectors used for 
    - information extraction 
    - machine translation 
    - chatbots. 
    - relationships between words as follows

## Neighboring words
- cluster word vectors together to find similar words
- similarity can be due to
    - type of word (noun, verb, adj)
    - synonym/antonym (due to place in sentence) 

**one possible implementation**
you could create a matrix where each cell is the number of times the other word apears in the neighboring words. you could create a threshold for this neighborhood and call it K.