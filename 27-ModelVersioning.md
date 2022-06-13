In the Model Versioning design pattern, backward compatibility is achieved by deploying a changed model as a microservice with a different REST endpoint. 

* Deploying model updates to production will inevitably affect the way models behave on new data, which presents a challenge we need an approach for keeping production models up to date while still ensuring backward compatibility for existing model users. 
* To gracefully handle updates to a model, deploy multiple model versions with different REST endpoints. This ensures backward compatibility by keeping multiple versions of a model deployed at a given time, those users relying on older versions will still be able to use the service. Versioning also allows for fine-grained performance monitoring and analytics tracking across versions. We can compare accuracy and usage statistics, and use this to determine when to take a particular version offline. If we have a model update that we want to test with only a small subset of users, the Model Versioning design pattern makes it possible to perform A/B testing. 
 


