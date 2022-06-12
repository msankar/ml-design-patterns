* To ensure that sampling is repeatable and reproducible, it is necessary to use a well-distributed column and a deterministic hash function to split the available data into training, validation, and test datasets. 

* we want lightweight, repeatable splitting of the data that works regardless of programming language or random seeds. We also want to ensure that correlated rows fall into the same split. For example, we do not want flights on January 2, 2019 in the test dataset if flights on that day are in the training dataset. 

* Is data correlated? data leakage
* If not correlated random split - hash (FARM_FINGERPRINT)
* Sequential split - time series models
* Stratified split - Examples of all seasons in train, test, validation data
