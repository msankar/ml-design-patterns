* The Batch Serving design pattern uses a distributed data processing infrastructure (MapReduce, Apache Spark, BigQuery, Apache Beam, and so on) to carry out ML inference on a large number of instances asynchronously. 

* Even though batch serving is used when latency is not a concern, it is possible to incorporate precomputed results and periodic refreshing to use this in scenarios where the space of possible prediction inputs is limited. 

### Batch and Stream pipelines
* ApacheSpark or Apache Beam are useful when input needs preprocessing
* Apache Beam if client code needs to maintain state. (e.g. time windowed average)
* Cached results of batch serving
* Lambda architecture - supports both online serving and batch serving. Trade-off between latency and throughput. a Lambda architecture is supported by having separate systems for online serving and batch serving. 


