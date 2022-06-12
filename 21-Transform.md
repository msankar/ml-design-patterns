* The Transform design pattern makes moving an ML model to production much easier by keeping inputs, features, and transforms carefully separate. 

* Training-serving skew , caused by differences in any of these factors between the training and serving environments, is one of the key reasons why productionization of ML models is so hard. 

* insert the transformations into the model graph for serving. At the same time, because the model training happens on the transformed data, our training loop does not have to carry out these transformations during each epoch. 

* An alternative approach to solving the training-serving skew problem is to employ the Feature Store pattern. The feature store comprises a coordinated computation engine and repository of transformed feature data. The computation engine supports low-latency access for inference and batch creation of transformed features while the data repository provides quick access to transformed features for model training. 


