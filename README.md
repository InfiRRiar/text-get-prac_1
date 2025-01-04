# Text generation

I've completed SHAD tesks from the week 3. It shows a few base ways to generate new texts based on a huge corpus.

### NGram

The entire text corpus splits into tokens (words). Basically, it just finds the probabilities for the every word in the dictionary to appear after given n words. These probabilities are calculated using the given dataset.

So yeah, not very interesting, but it is what it is.

### Convolutional and Recurrent nets

These two are more complicated a bit. Every token is represented as unique token. After tokenezation lines assemble into a batch in the from of a matrix. The structure of a nets is simple:

- Embeddings to code;
- Main part (either the Conv1d or LSTM layer);
- Linear layer to transform the output into a vector of probabilities for every symbol to appear next.

**Loss function**: cross-entropy.

## Results: 

On the same dataset with the same (when it possible) hyperparameters:

- Conv1d: 43.785 dev loss;
- LSTM: 27.848 dev loss.

Not a wonderful results, but as soon as architectures I use there are really simple, it's not an awful start neither. Will be going towards better solutions pretty much soon.
