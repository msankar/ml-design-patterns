The Feature Store design pattern simplifies the management and reuse of features across projects by decoupling the feature creation process from the development of models using those features. 

* Ad hoc features aren’t easily reused. Features are re-created over and over again, either by individual users or within teams, or never leave the pipelines (or notebooks) in which they are created. This is particularly problematic for higher-level features that are complex to calculate. 
* Data governance is made difficult if each ML project computes features from sensitive data differently. 
* Ad hoc features aren’t easily shared between teams or across projects. In many organizations, the same raw data is used by multiple teams, but separate teams may define features differently and there is no easy access to feature documentation. This also hinders effective cross-collaboration of teams, leading to siloed work and unnecessarily duplicated effort. 
* Ad hoc features used for training and serving are inconsistent i.e., training–serving skew. 
* Productionizing features is difficult. 
* feature creation is inconsistent between training and inference, running the risk of training–serving skew or data leakage by accidentally introducing label information into the model input pipeline. 

Feature stores work because they decouple feature engineering from feature usage, allowing feature development and creation to occur independently from the consumption of features during model development. As features are added to the feature store, they become available immediately for both training and serving and are stored in a single location. This ensures consistency between model training and serving. 


the primary components of the feature store are the same:
* A tool to process large feature engineering jobs quickly, such as Spark, Flink or Beam. 
* A storage component for housing the feature sets that are created, such as Hive, cloud storage (Amazon S3, Google Cloud Storage), BigQuery, Redis, BigTable, and/or Cassandra. The combination that Feast uses (BigQuery and Redis) is optimized for offline versus online (low-latency) feature retrieval. 
* A metadata layer to record feature version information, documentation, and feature registry to simplify discovery and sharing of feature sets. 
* An API for ingesting and retrieving features to/from the feature store. 







