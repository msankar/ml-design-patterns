The Fairness Lens design pattern suggests the use of preprocessing and postprocessing techniques to ensure that model predictions are fair and equitable for different groups of users and scenarios. Fairness in machine learning is a continuously evolving area of research, and there is no single catch-all solution or definition to making a model “fair.” Evaluating an entire end-to-end ML workflow from data collection to model deployment through a fairness lens is essential to building successful, high-quality models. 

Bias becomes harmful when it affects different groups of people differently. This is known as problematic bias , 
The Fairness Lens design pattern provides approaches for building datasets and models that treat all groups of users equally. We’ll demonstrate techniques for both types of analysis using the What-If Tool , an open source tool for dataset and model evaluation that can be run from many Python notebook environments.  

* Reporting Bias
* Implicit or proxy bias - Removing obvious features with potential bias like race and gender can often be worse than leaving them in, since it makes it harder to identify and correct instances of bias in the model. 
* experimenter bias 
* data distribution bias
* data representation bias
* data collection bias

From the Fairness Indicators Python package , TFMA can also be used as a standalone tool that works with both TensorFlow and non-TensorFlow models. 

Data augmentation - data is changed before training with the goal of removing potential sources of bias. One specific type of data augmentation is known as ablation, 
Another data augmentation approach involves generating new data, and it was used by Google Translate to minimize gender bias when translating text to and from gender-neutral and gender-specific languages. The solution involved rewriting translation data such that when applicable, a provided translation would be offered in both the feminine and masculine form. For example, the gender-neutral English sentence “We are doctors” would yield two results when being translated to Spanish, as seen in Figure 7-16 . In Spanish, the word “we” can have both a feminine and masculine form. 

Model cards - The goal of Model Cards is to improve model transparency by providing details on scenarios where a model should and should not be used, since mitigating problematic bias only works if a model is used in the way it was intended. 

Fairness versus explainability - The concepts of fairness and explainability in ML are sometimes confused since they are often used together and are both part of the larger initiative of Responsible AI. Fairness applies specifically to identifying and removing bias from models, and explainability is one approach for diagnosing the presence of bias. 

Explainability can also be used outside the context of fairness to reveal things like why a model is flagging particular fraudulent transactions, or the pixels that caused a model to predict “diseased” in a medical image. Explainability, therefore, is a method for improving model transparency. Sometimes transparency can reveal areas where a model is treating certain groups unfairly, but it can also provide higher-level insight into a model’s decision-making process. 



