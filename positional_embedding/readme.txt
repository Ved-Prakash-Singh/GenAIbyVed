Imagine reading a sentence. Even though you can see most of the words at once, your brain instinctively understands the order in which to process them, allowing you to grasp the meaning. Transformers operate in a similar way: they process entire sequences of data at once, unlike traditional models like RNNs or LSTMs that go word by word.

Transformers have revolutionized the way we process sequential data in AI. Unlike RNNs or LSTMs, which process token by token, transformers process the entire sequence at once, making computations faster and more efficient.

Yet, despite their non-sequential processing, transformers still excel at handling sequential data. So, you might be curious: how exactly do transformers capture and preserve the essence of sequence in the data?

Transformers use a clever mechanism called positional encoding. As the name suggests, each word at a specific position is assigned unique positional information, which is represented as a vector of the same dimension as the word embeddings. This positional information is then added to the word embedding before being passed to the attention layer.

Consider the sentence,” The transformer.” Suppose it uses a 2-dimensional
word embedding: ”The” is embedded as [0.4, 0.6] and, ”transformer” is embedded as [0.9, 0.7]. 

The positional embeddings will also be 2-dimensional vector. For the first position, assume it is [0, 1] and for the second position, it is [0.84, 0.54].

In the transformer architecture, the ”positional embedding” is added to the
”word embedding” before being passed to the attention layer. Therefore, the
vectors that will be passed to the attention layer are as follows:
• For ”The”: [0.4 + 0, 0.6 + 1] = [0.4, 1.6]
• For ”transformer”: [0.9 + 0.84, 0.7 + 0.54] = [1.74, 1.24]

In the attention layer, using learned query and key vectors, the transformer
has the ability to understand the sequence and the relationships among the
words.

Please refer to the attached document for more details, including visual charts and mathematical calculations on word embeddings in transformers.
