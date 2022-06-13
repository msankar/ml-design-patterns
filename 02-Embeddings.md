Embeddings are a learnable data representation that map high-cardinality data into a lower-dimensional space in such a way that the information relevant to the learning problem is preserved. Embeddings are at the heart of modern-day machine learning and have various incarnations throughout the field. 

Because embeddings capture closeness relationships in the input data in a lower-dimensional representation, we can use an embedding layer as a replacement for clustering techniques (e.g., customer segmentation) and dimensionality reduction methods like principal components analysis (PCA). Embedding weights are determined in the main model training loop, thus saving the need to cluster or do PCA beforehand. 

The embedding layer is just another hidden layer of the neural network. The weights are then associated to each of the high-cardinality dimensions, and the output is passed through the rest of the network. Therefore, the weights to create the embedding are learned through the process of gradient descent just like any other weights in the neural network. This means that the resulting vector embeddings represent the most efficient low-dimensional representation of those feature values with respect to the learning task. 



