The Stateless Serving Function design pattern makes it possible for a production ML system to synchronously handle thousands to millions of prediction requests per second. 

The approach of exporting a model to a stateless function and deploying the stateless function in a web application framework works because web application frameworks offer autoscaling, can be fully managed, and are language neutral. They are also familiar to software and business development teams who may not have experience with machine learning. This also has benefits for agile development 

* Autoscaling

* Fully managed
* Language neutral
* Powerful ecosystem
* Custom serving function - e.g.return logits with sigmoid results
* Multiple signatures - servingdefault and expensiveresult API
* Online prediction - latency

* Prediction library vs REST API

