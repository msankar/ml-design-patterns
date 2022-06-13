The Multilabel design pattern refers to problems where we can assign more than one label to a given training example. For neural networks, this design requires changing the activation function used in the final output layer of the model and choosing how our application will parse model output. Note that this is different from multiclass classification problems, where a single example is assigned exactly one label from a group of many (> 1) possible classes. You may also hear the Multilabel design pattern referred to as multilabel, multiclass classification since it involves choosing more than one label from a group of more than one possible class. When discussing this pattern, we’ll focus primarily on neural networks. 

The less-common scenario is when each training example can be assigned more than one label, which is what this pattern addresses. 
The solution for building models that can assign more than one label to a given training example is to use the sigmoid activation function in our final output layer. Rather than generating an array where all values sum to 1 (as in softmax), each individual value in a sigmoid array is a float between 0 and 1. 

To summarize, use the Multilabel design pattern when your data falls into any of the following classification scenarios: 
A single training example can be associated with mutually exclusive labels. 
A single training example can have many hierarchical labels. 
Labelers describe the same item in different ways, and each interpretation is accurate. 


