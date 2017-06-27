# Project-Youtube-Recommendation-prediction
Training data contains 26901 videos' top 20 recommended videos. Testing data are constructed by removing portion of training data and adding fake pairs. The performance of the model is evaluated by area under the ROC curve.

There are 218344 videos (nodes), 466970 edges in traning data and 100000 edges in test data.

Project approaches:
* Collect and visualize graph properties.
* Assume the top 20 recommended videos would have shorter path to the parent videos than other nodes. The prediction is done by setting a threshold the shortest path between test pairs.
* Bench mark by using undirected graph constructed from the training data, and calculate the shortest path bewteen each testing pairs.
* Seperate 26901 parent nodes into three clusters by spectral clustering and treat the rest of the nodes as chirldren nodes. Using the result to further filter the benchmark result.
* Divide the parent node using kmeans clustering on the feaure vectors instead. 
* Perform spectral clustering on the entire graph and perform local search.
* Set edges between cluster and perform global search.

