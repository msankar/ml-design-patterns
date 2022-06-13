The Cascade design pattern addresses situations where a machine learning problem can be profitably broken into a series of ML problems. Such a cascade often requires careful design of the ML experiment. 

An intuitive way to address this problem is by using the Cascade design pattern. We break the problem into four parts: Predicting whether a specific transaction is by a reseller Training one model on sales to retail buyers Training the second model on sales to resellers In production, combining the output of the three separate models to predict return likelihood for every item purchased and the probability that the transaction is by a reseller 

