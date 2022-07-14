# Important Hyperparameters (Tensorflow NLP Course)


    EMBEDDING_DIM: Dimension of the dense embedding, will be used in the embedding layer of the model. Defaults to 100.

    MAXLEN: Maximum length of all sequences. Defaults to 16.

    TRUNCATING: Truncating strategy (truncate either before or after each sequence.). Defaults to 'post'.

    PADDING: Padding strategy (pad either before or after each sequence.). Defaults to 'post'.

    OOV_TOKEN: Token to replace out-of-vocabulary words during text_to_sequence calls. Defaults to "\".

    MAX_EXAMPLES: Max number of examples to use. Defaults to 160000 (10% of the original number of examples)

    TRAINING_SPLIT: Proportion of data used for training. Defaults to 0.9
    