The Hashed Feature design pattern addresses three possible problems associated with categorical features: incomplete vocabulary, model size due to cardinality, and cold start. It does so by grouping the categorical features and accepting the trade-off of collisions in the data representation. 

The Hashed Feature design pattern represents a categorical input variable by doing the following: 
* Converting the categorical input into a unique string. For the departure airport, we can use the three-letter IATA code for the airport. 
* Invoking a deterministic (no random seeds or salt) and portable (so that the same algorithm can be used in both training and serving) hashing algorithm on the string. 
* Taking the remainder when the hash result is divided by the desired number of buckets. Typically, the hashing algorithm returns an integer that can be negative and the modulo of a negative integer is negative. So, the absolute value of the result is taken. 

