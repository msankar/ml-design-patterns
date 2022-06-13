The Ensembles design pattern refers to techniques in machine learning that combine multiple machine learning models and aggregate their results to make predictions. Ensembles can be an effective means to improve performance and produce predictions that are better than any single model. 

Bagging (short for bootstrap aggregating) is a type of parallel ensembling method and is used to address high variance in machine learning models. The bootstrap part of bagging refers to the datasets used for training the ensemble members. Specifically, if there are k submodels, then there are k separate datasets used for training each submodel of the ensemble. Each dataset is constructed by randomly sampling (with replacement) from the original training dataset. This means there is a high probability that any of the k datasets will be missing some training examples, but also any dataset will likely have repeated training examples. The aggregation takes place on the output of the multiple ensemble model members either an average in the case of a regression task or a majority vote in the case of classification. 

Boosting Boosting is another Ensemble technique. However, unlike bagging, boosting ultimately constructs an ensemble model with more capacity than the individual member models. For this reason, boosting provides a more effective means of reducing bias than variance. The idea behind boosting is to iteratively build an ensemble of models where each successive model focuses on learning the examples the previous model got wrong. In short, boosting iteratively improves upon a sequence of weak learners taking a weighted average to ultimately yield a strong learner. 

Stacking Stacking is an ensemble method that combines the outputs of a collection of models to make a prediction. The initial models, which are typically of different model types, are trained to completion on the full training dataset. Then, a secondary meta-model is trained using the initial model outputs as features. This second meta-model learns how to best combine the outcomes of the initial models to decrease the training error and can be any type of machine learning model. To implement a stacking ensemble, we first train all the members of the ensemble on the training dataset. The following code calls a function, fit_model , that takes as arguments a model and the training dataset inputs X_train and label Y_train . This way members is a list containing all the trained models in our ensemble. 

Dropout as bagging Techniques like dropout provide a powerful and effective alternative. Dropout is known as a regularization technique in deep learning but can be also understood as an approximation to bagging. Dropout in a neural network randomly (with a prescribed probability) “turns off” neurons of the network for each mini-batch of training, essentially evaluating a bagged ensemble of exponentially many neural networks. 
Decreased model interpretability - Another point to keep in mind is model interpretability. Already in deep learning, effectively explaining why our model makes the predictions it does can be difficult. 




 

