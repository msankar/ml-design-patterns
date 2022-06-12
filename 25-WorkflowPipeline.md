In the Workflow Pipeline design pattern, we address the problem of creating an end-to-end reproducible pipeline by containerizing and orchestrating the steps in our machine learning process. The containerization might be done explicitly, or using a framework that simplifies the process. 

To handle the problems that come with scaling machine learning processes, we can make each step in our ML workflow a separate, containerized service. 

* Data collection: run a query to get the hurricane data from BigQuery. 
* Data validation: use the ExampleValidator component to identify anomalies and check for data drift. 
* Data analysis and preprocessing: generate some statistics on the data and define the schema. 
* Model training: train a tf.keras model on AI Platform. 
* Model deployment: deploy the trained model to AI Platform Prediction. 

with each pipeline component in its own container, different team members can build and test separate pieces of a pipeline in parallel. This allows for faster development and minimizes the risks associated with a more monolithic ML process where steps are inextricably linked to one another. The package dependencies and code required to build out the data preprocessing step, for example, may be significantly different than those for model deployment. By building these steps as part of a pipeline, each piece can be built in a separate container with its own dependencies and incorporated into a larger pipeline when completed. 


Lineage tracking in ML pipelines

One additional feature of pipelines is using them for tracking model metadata and artifacts, also known as lineage tracking . Each time we invoke a pipeline, a series of artifacts is generated. These artifacts could include dataset summaries, exported models, model evaluation results, metadata on specific pipeline invocations, and more. Lineage tracking lets us visualize the history of our model versions along with other associated model artifacts. 







