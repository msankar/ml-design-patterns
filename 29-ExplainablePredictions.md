The Explainable Predictions design pattern increases user trust in ML systems by providing users with an understanding of how and why models make certain predictions. While models such as decision trees are interpretable by design, the architecture of deep neural networks makes them inherently difficult to explain. 

In addition to model end users, another group of stakeholders are those involved with regulatory and compliance standards for ML models, since models in certain industries may require auditing or additional transparency. 

Instance-level feature attributions - In an image model, an instance-level attribution might highlight the pixels in an image that caused it to predict it contained a cat. 

Global feature attributions - Global feature attributions analyze the model’s behavior across an aggregate to draw conclusions about how the model is behaving as a whole. Typically this is done by averaging instance-level feature attributions from a test dataset. In a model predicting whether a flight will be delayed, global attributions might tell us that overall, extreme weather is the most significant feature when predicting delays. 


* Sampled Shapley
* Integrated Gradients
* XRAI

Data selection bias
Counterfactual analysis and example-based explanations

