* The Continued Model Evaluation design pattern handles the common problem of needing to detect and take action when a deployed model is no longer fit-for-purpose. 

* Concept drift occurs whenever the relationship between the model inputs and target have changed. 

* Data drift refers to any change that has occurred to the data being fed to your model for prediction as compared to the data that was used for training. 

* direct way to identify model deterioration is to continuously monitor your model’s predictive performance over time, and assess that performance with the same evaluation metrics you used during development. 

* Sample a % of the number of input requests
* Capture ground-truth through HITL or users interactions
